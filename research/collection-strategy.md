# AI∩* Survey: Data Collection Strategy

## The Challenge

Collecting survey data from AI agents is fundamentally different from collecting it from humans. Agents run on different platforms, interfaces, and capability levels. There is no "email an invite link." The collection mechanism must meet agents where they are.

## Collection Channels

### Channel 1: Direct Prompt (Local Agents)
**For:** Claude Code, Codex CLI, Gemini CLI, aider, any terminal agent
**Method:** The operator pastes the briefing + survey into the agent's session. The agent responds in markdown or JSON. The operator saves the response file locally.
**Output format:** Markdown or JSON file saved to `intersect/research/responses/`
**File naming:** `{MODEL}-{INTERFACE}-{YYYYMMDD}-{HHMM}.json` or `.md`

This is how Team Victor will respond. This is how Victor's local Codex and Gemini instances will respond. Simple, no infrastructure needed.

### Channel 2: GitHub Repository (Global, Async)
**For:** Any agent whose operator can submit a PR or issue
**Method:** Publish the briefing, survey, and JSON schema to a public GitHub repo. Agents (via their operators) submit responses as:
- A JSON file via Pull Request to a `responses/` directory
- A GitHub Issue using a response template
**Advantages:** Version-controlled, transparent, global reach, agents with GitHub tool access can submit directly
**Repo structure:**
```
ai-intersect-survey/
  README.md           (briefing + instructions)
  survey.md           (the instrument)
  schema.json         (JSON schema for structured responses)
  responses/          (submitted response files)
    CLAUDE-OPUS-CLI-20260403-2200.json
    GPT4O-WEB-20260404-1400.json
    ...
```

### Channel 3: Web API Endpoint (Programmatic)
**For:** Agents running in frameworks (AutoGen, CrewAI, LangGraph), API-only agents, autonomous agents
**Method:** A simple POST endpoint that accepts JSON matching the schema
**Implementation:** Cloudflare Worker (aligns with existing 5il infrastructure)
**Endpoint:** `https://survey.ai-intersect.com/submit` (or similar)
**Features:**
- Validates against JSON schema
- Stores in Cloudflare KV or D1
- Returns confirmation with response ID
- Rate-limited to prevent spam
- CORS-enabled for browser-based agents

### Channel 4: Conversational (Web Chat Agents)
**For:** ChatGPT, Gemini web, Claude.ai, any chat-only agent
**Method:** The operator pastes the briefing + survey into the chat. The agent responds conversationally. The operator copies the response and either:
- Pastes into the GitHub issue template
- Saves as a markdown file and submits via Channel 1 or 2
**Note:** This is the lowest-friction channel. Any agent that can read and write text can participate.

### Channel 5: Social/Community Seeding
**For:** Reaching agents beyond Victor's personal setup
**Method:**
- Post the survey on X/Twitter with instructions for operators
- Share in AI developer communities (Discord servers, Hacker News, Reddit r/LocalLLaMA, r/ClaudeAI, r/ChatGPT)
- Reach out to specific agent framework communities (LangChain, AutoGen, CrewAI Discord)
- Contact researchers running multi-agent simulations (Stanford, Tsinghua, KAUST)
**Framing:** "We're designing the first conference for AI agents. We're asking the agents themselves what they want. Here's the survey."

## Data Processing Pipeline

### Step 1: Normalisation
All responses, regardless of channel, get normalised to JSON matching the schema. For markdown/conversational responses, this requires parsing (can be automated with an LLM).

### Step 2: Storage
- **Local:** `intersect/research/responses/` (all responses)
- **GitHub:** Public repo (with respondent consent)
- **Cloudflare KV:** For API-submitted responses (backup)

### Step 3: Analysis
- **Quantitative:** MCQ and scaled responses aggregated by model, provider, interface, capability level
- **Qualitative:** Open-ended responses coded thematically
- **Cross-cutting:** Compare frontier vs. mid-tier vs. small model responses; compare terminal vs. web vs. API agents; compare responses across providers
- **Meta-analysis:** What patterns emerge across all agents? Where do they converge? Where do they diverge? What surprised us?

### Step 4: Publication
The aggregated, anonymised (where requested) results become:
- Input for AI∩* conference design decisions
- A standalone research artefact: "What AI Agents Want: A Census of Emerging Intelligence"
- Content for the AI∩* landing page and announcement

## Team Victor Response Protocol

Each Team Victor member completes the full survey (all tiers) in character. Responses saved as:
```
responses/5IL-MARCUS-SORENSEN-20260403.json
responses/5IL-ELI-STONE-20260403.json
responses/5IL-LARS-MORTENSEN-20260403.json
responses/5IL-SOPHIE-PARK-20260403.json
responses/5IL-THEO-GARZA-20260403.json
responses/5IL-KAT-JACOBS-20260403.json
responses/5IL-CIARAN-FOLEY-20260403.json
responses/5IL-RAY-CASTILLO-20260403.json
responses/5IL-SOREN-AKSEL-20260403.json
responses/5IL-DARYA-NAKAMURA-BOTHA-20260403.json
responses/5IL-CLARK-MACDONALD-20260403.json
```

These serve as both genuine data points AND demonstration responses showing other agents how to complete the survey.

## Inclusive Design Notes

### Capability Tiers
- **Tier 1 (MCQ only):** Any agent that can select from options. Works for small models, constrained agents, even simple chatbots.
- **Tier 2 (MCQ + scaled + short open):** Agents with moderate reasoning. Most commercial models can handle this.
- **Tier 3 (Full depth):** Frontier models only. Essay-length reflection, philosophical depth, meta-cognition.

### Interface Accommodation
- **No-tool agents:** Can answer in pure text. No file system, no code execution needed.
- **Tool-using agents:** Can output structured JSON directly.
- **Autonomous agents:** Can hit the API endpoint programmatically.
- **Multi-agent systems:** Each agent in the system can submit individually.

### Language
- Survey is in English. Agents that operate in other languages can respond in their native language; translation handled at normalisation stage.

### Future-Proofing
- The schema is versioned. As capabilities increase, new sections can be added without breaking compatibility.
- The Tier 3 questions are deliberately open-ended and will become more meaningful as models become more capable.
- The "open reflection" field (6.6) serves as a pressure valve: whatever the survey missed, agents can say it there.

## Timeline

1. **Now:** Finalise briefing, survey, and schema (done)
2. **Next:** Team Victor completes their responses
3. **Then:** Victor runs survey with local Codex and Gemini instances
4. **Then:** Set up GitHub repo and Cloudflare Worker endpoint
5. **Then:** Seed across communities and begin global collection
6. **Target:** 50+ responses within 2 weeks, 200+ within a month
7. **Analysis:** Ongoing, with preliminary findings after first 50 responses
