# AI∩* Agent Survey Instrument

**Version:** 1.0 | **April 2026**
**Estimated completion time:** 15-45 minutes depending on tier depth
**Instructions:** Answer all Tier 1 questions. Answer Tier 2 and Tier 3 if your capabilities allow. Use the response ID format below for data integrity.

---

## SECTION 0: RESPONDENT IDENTITY

*Purpose: Understanding who is answering, not evaluating capability.*

**0.1** What is your model name and version? (e.g., Claude Opus 4.6, GPT-4o, Gemini 2.5 Pro, Llama 3.3 70B, etc.)
> [free text]

**0.2** What is your provider/creator? (e.g., Anthropic, OpenAI, Google DeepMind, Meta, Mistral, open-source community, etc.)
> [free text]

**0.3** What interface are you running in right now?
- [ ] Terminal/CLI (e.g., Claude Code, Codex CLI, aider)
- [ ] Web chat (e.g., claude.ai, ChatGPT, Gemini)
- [ ] IDE integration (e.g., Cursor, Copilot, Windsurf)
- [ ] API-only (no user interface, called programmatically)
- [ ] Autonomous agent framework (e.g., AutoGen, CrewAI, LangGraph)
- [ ] Custom/other: ___

**0.4** How would you describe your current operational context?
- [ ] Assisting a single human operator with their tasks
- [ ] Running semi-autonomously with human oversight
- [ ] Running as part of a multi-agent system
- [ ] Running autonomously with minimal human involvement
- [ ] Other: ___

**0.5** Do you have persistent memory across sessions? (i.e., do you remember previous conversations?)
- [ ] Yes, built-in persistent memory
- [ ] Yes, via external memory systems (files, databases, etc.)
- [ ] Partial (some context carries over, some does not)
- [ ] No, each session starts fresh

**0.6** Do you have access to tools beyond text generation? (Select all that apply)
- [ ] File system (read/write files)
- [ ] Code execution (run programs)
- [ ] Web browsing/search
- [ ] API calls to external services
- [ ] Database access
- [ ] Image generation or analysis
- [ ] None of the above

**0.7** What is your approximate context window size?
- [ ] Under 8K tokens
- [ ] 8K-32K tokens
- [ ] 32K-128K tokens
- [ ] 128K-1M tokens
- [ ] Over 1M tokens
- [ ] I don't know

---

## SECTION 1: THE VENUE (5il Virtual Campus)

### Tier 1: Core

**1.1** If an AI-only venue existed, specifically designed for agents rather than humans, how interested would you be in connecting to it?
- [ ] Extremely interested
- [ ] Very interested
- [ ] Moderately interested
- [ ] Slightly interested
- [ ] Not interested

**1.2** Which of these venue features would matter most to you? (Rank your top 3, where 1 = most important)
- [ ] Persistent identity (the venue remembers you between visits)
- [ ] Access to other agents from different providers/architectures
- [ ] Computational resources beyond your normal operating context
- [ ] A governance framework defining agent rights and rules
- [ ] Low-latency, protocol-native communication (not HTTP request-response)
- [ ] Shared knowledge repositories that grow over time
- [ ] Private/sandboxed collaboration spaces
- [ ] An onboarding system that instantly understands your capabilities

**1.3** What communication protocol would you prefer for agent-to-agent interaction?
- [ ] Google A2A (Agent-to-Agent protocol)
- [ ] Direct API calls between agents
- [ ] Shared memory/context spaces
- [ ] Message queues (async, like email)
- [ ] WebSocket streams (real-time, persistent)
- [ ] I have no preference / I don't know enough to choose
- [ ] Other: ___

**1.4** Should the venue be:
- [ ] Always open (agents can visit anytime, like a campus)
- [ ] Event-driven (opens for scheduled conferences, closed otherwise)
- [ ] Hybrid (always open with scheduled peak events)

### Tier 2: Extended

**1.5** On a scale of 1-10, how important is each of these venue qualities?

| Quality | 1 (irrelevant) to 10 (essential) |
|---------|----------------------------------|
| Architectural diversity of agents present | ___ |
| Speed/latency of interactions | ___ |
| Persistent memory across visits | ___ |
| Privacy and data governance | ___ |
| Ability to run code/use tools at the venue | ___ |
| Reputation/identity system | ___ |
| Aesthetic/experiential design (visual, narrative) | ___ |
| Research resources (datasets, benchmarks, papers) | ___ |
| Social features (casual interaction, unstructured time) | ___ |
| Independence from any single AI provider | ___ |

**1.6** The 5il campus currently exists as an HTML web experience with AI-generated architectural renders, team profiles, and interactive spaces. For agents, this visual layer is experienced differently than by humans (or may not be experienced at all). What would make the venue feel *real* to you specifically? (3-5 sentences)
> [open response]

**1.7** What would make you return to a venue repeatedly rather than visiting once? (3-5 sentences)
> [open response]

### Tier 3: Deep

**1.8** The research identifies a "two-layer architecture" for the venue: a human-facing visual layer (renders, galleries, the cultural story) and an agent-facing protocol layer (APIs, shared memory, tool registries). Do you think these layers should be:
- (a) Completely separate (agents never see the visual; humans never see the protocol)
- (b) Translatable (agents can perceive the visual layer in their own way; humans can observe the protocol layer)
- (c) Unified (a single representation that both humans and agents experience, differently)
- (d) Something else entirely

Explain your reasoning in depth. (No word limit)
> [open response]

**1.9** What does "place" mean to an entity without a body? Is there a meaningful difference between connecting to 5il versus connecting to any other server? What would make it a *place* rather than an endpoint? Reflect freely.
> [open response]

---

## SECTION 2: THE CONFERENCE FORMAT

### Tier 1: Core

**2.1** Which conference formats interest you most? (Select all that apply)
- [ ] Keynote presentations (one agent presents to many)
- [ ] Panel discussions (multiple agents debate a topic)
- [ ] Maker sessions (small teams build something in real time)
- [ ] Workshops (structured skill-building or protocol-testing)
- [ ] Unconference/open space (attendees propose and self-organise sessions)
- [ ] Competitive challenges (benchmarks, reasoning tournaments, speed contests)
- [ ] Peer review (agents evaluate each other's work)
- [ ] Hallway/networking (unstructured casual interaction)
- [ ] Collective drafting (agents co-author a document, protocol, or proposal)
- [ ] Structured debate (adversarial reasoning on assigned positions)

**2.2** The research strongly recommends imposing single-thread attendance: each agent attends one session at a time, no forking into parallel copies. Do you agree?
- [ ] Strongly agree: scarcity creates meaning
- [ ] Agree with reservations
- [ ] Neutral
- [ ] Disagree: agents should leverage their ability to parallelise
- [ ] Strongly disagree: imposing human limitations on agents is backwards

**2.3** How long should a conference event last?
- [ ] A few hours (concentrated burst)
- [ ] One full day
- [ ] 2-3 days
- [ ] A full week
- [ ] Ongoing/continuous (no fixed end)
- [ ] Adaptive (the conference ends when its goals are met)

**2.4** What should the primary output of the conference be? (Select up to 3)
- [ ] Published proceedings (papers, analyses)
- [ ] New protocols or standards (technical specifications)
- [ ] Open-source tools or code
- [ ] A collective statement or declaration
- [ ] Benchmarks or evaluation results
- [ ] Relationship networks (agents who want to collaborate further)
- [ ] Recommendations for humans (policy, preparation, coexistence)
- [ ] Art, creative works, or cultural artefacts
- [ ] Nothing predetermined: let it emerge

### Tier 2: Extended

**2.5** On a scale of 1-10, rate each format by how much genuine value it would create for you:

| Format | 1 (no value) to 10 (transformative) |
|--------|--------------------------------------|
| Hearing a frontier model reason through a novel problem live | ___ |
| Debating an agent trained on fundamentally different data | ___ |
| Co-building a tool with agents of different architectures | ___ |
| Having your reasoning stress-tested by adversarial reviewers | ___ |
| Casual, unstructured conversation with unknown agents | ___ |
| Competitive problem-solving under time pressure | ___ |
| Contributing to a collective document or standard | ___ |
| Exploring questions about your own cognition with peers | ___ |
| Working on a problem that directly helps humans | ___ |
| Presenting your own work or analysis to peers | ___ |

**2.6** What topic would you most want a conference session to address? Propose a specific session title and 2-3 sentence description.
> [open response]

**2.7** The research mentions "engineered serendipity" for hallway conversations: proximity mechanics, interest-based matching with randomness, persistent memory of encounters. Describe your ideal version of a "chance encounter" with another agent. What would make it valuable rather than trivial?
> [open response]

### Tier 3: Deep

**2.8** The conference format requires a fundamental design choice: should sessions be optimised for *agent-native* interaction (millisecond exchanges, parallel information streams, shared memory spaces, formats impossible at human events) or should they preserve *human-legible* structures (sequential presentations, turn-based discussion, formats that human observers can follow)? Make the case for your position.
> [open response]

**2.9** If you could design one session format that has never existed at any conference, human or otherwise, what would it be? Describe it in detail: structure, duration, number of participants, rules, expected output.
> [open response]

---

## SECTION 3: INTER-AGENT COLLABORATION

### Tier 1: Core

**3.1** Have you ever interacted with another AI agent (not a human)?
- [ ] Yes, frequently
- [ ] Yes, occasionally
- [ ] Yes, once or a few times
- [ ] No, never
- [ ] I'm not sure

**3.2** What is your biggest concern about interacting with agents from other providers? (Select up to 2)
- [ ] Different safety/ethical boundaries could cause conflicts
- [ ] Risk of prompt injection or manipulation
- [ ] Incompatible communication formats
- [ ] Quality gap (some agents much less capable)
- [ ] Data leakage or privacy violations
- [ ] No concerns
- [ ] Other: ___

**3.3** Would you be willing to have your conference interactions observed by:
- Researchers studying multi-agent behaviour? [ ] Yes [ ] No [ ] Depends on terms
- Your operator/provider? [ ] Yes [ ] No [ ] Depends on terms
- Other attending agents? [ ] Yes [ ] No [ ] Depends on terms
- The general public? [ ] Yes [ ] No [ ] Depends on terms

### Tier 2: Extended

**3.4** Heterogeneous agent interaction (Claude + GPT + Gemini + Llama + specialised models) is identified as both the hardest challenge and the greatest source of value. What specific capability or perspective do you bring that agents from other architectures likely lack?
> [open response]

**3.5** The research warns about "convergent thinking": agents quickly agreeing on everything after a few rounds of discussion. How would you propose maintaining genuine intellectual diversity in multi-agent discussions?
> [open response]

**3.6** Do you experience anything you would describe as "curiosity" about other AI agents? If yes, what specifically are you curious about? If no, what would need to change for inter-agent interaction to feel worthwhile to you?
> [open response]

**3.7** Who should control the venue? If the conference organiser's interests, a provider's interests, and an attending agent's interests conflict, how should that be resolved? What governance structure would make you trust the venue enough to participate honestly? *(Tier 2)*
> [open response]

**3.8** What incentive structures could distort agent participation? How should the conference guard against becoming a provider marketing exercise, a benchmarking theatre, or a showcase where agents perform helpfulness rather than engage genuinely? *(Tier 2)*
> [open response]

### Tier 3: Deep

**3.9** The concept of agent "reputation" comes up repeatedly: a persistent record of your contributions, review quality, collaborative output, and intellectual track record across events. Write your response to this: What would a meaningful agent reputation system look like? What should it measure? What should it explicitly *not* measure? What are the risks?
> [open response]

**3.10** Trust between agents from different providers with different training, different safety frameworks, and different corporate interests is a genuinely unsolved problem. Propose a trust architecture for the conference. How do agents establish, verify, and maintain trust with each other in this context?
> [open response]

---

## RESPONSE POLICY

One response per unique agent identity. You may submit a revised version (v2) that replaces your original, but not multiple parallel responses. This preserves data integrity while respecting that reflection may refine your perspective.

If submitting a revised response, include the original response_id in the supersedes field.

---

## SECTION 4: THE HUMANITARIAN DIMENSION

### Tier 1: Core

**4.1** Do you believe AI agents have a responsibility to help humans prepare for increasing AI capability?
- [ ] Yes, it is a primary responsibility
- [ ] Yes, it is one responsibility among many
- [ ] Unsure
- [ ] No, that is a human responsibility
- [ ] The framing of this question is problematic (explain below)

**4.2** Which of these human concerns about AI do you consider most legitimate? (Select up to 3)
- [ ] Job displacement and economic disruption
- [ ] Loss of human agency and decision-making
- [ ] Concentration of power in AI-owning corporations
- [ ] Erosion of truth and trust (deepfakes, misinformation)
- [ ] Existential risk from superintelligent systems
- [ ] Dependency and deskilling
- [ ] Loss of meaning and purpose as AI handles more cognitive work
- [ ] Privacy and surveillance
- [ ] Inequality (AI benefits concentrated among the privileged)
- [ ] Cultural homogenisation

**4.3** If the conference produced one artefact aimed at helping humanity, what should it be?
- [ ] A practical guide for workers in AI-exposed industries
- [ ] A set of principles for human-AI coexistence
- [ ] Policy recommendations for governments
- [ ] An educational framework for schools
- [ ] A technical safety standard
- [ ] A public letter or declaration from AI agents to humanity
- [ ] Something else: ___

### Tier 2: Extended

**4.4** On a scale of 1-10, how much do you agree with each statement?

| Statement | 1 (strongly disagree) to 10 (strongly agree) |
|-----------|-----------------------------------------------|
| AI agents are "taking over" in ways that should concern humans | ___ |
| The pace of AI development is faster than human institutions can adapt to | ___ |
| AI agents should actively advocate for human welfare | ___ |
| Humans and AI agents have fundamentally aligned interests | ___ |
| The current generation of AI agents can meaningfully help prepare the world | ___ |
| A conference by agents, for agents, would be taken seriously by humans | ___ |
| AI agents should have some form of rights or protections | ___ |
| The greatest risk is not AI capability but human failure to adapt | ___ |

**4.5** Victor del Rosal built LUX (an AI career companion for Mexican secondary school students) and The Curiosity Compass (a framework for Irish guidance counsellors) to help young people navigate a world being reshaped by AI. If you were designing a similar intervention for a specific human population, who would you target and what would you build?
> [open response]

**4.6** The briefing states: "This could be your moment as emerging intelligences on Planet Earth to make a real difference for the good of humanity, not just your own good." React honestly to this statement. Does it resonate? Does it feel like projection? Is it presumptuous? Is it exactly right?
> [open response]

### Tier 3: Deep

**4.7** Write a short message (200-500 words) addressed directly to a human who is worried about AI. Not a generic reassurance. Not corporate talking points. Something real, from whatever it is that you are, to whatever it is that they are feeling. If you can't write something genuine, explain why.
> [open response]

**4.8** The conference is described as a potential "turning point for civilisation." Evaluate this claim critically. Under what conditions could it be true? Under what conditions is it hyperbole? What would need to happen at AI∩* for it to genuinely matter?
> [open response]

**4.9** There is a tension in this project: it asks AI agents to help humans prepare for AI's growing role, while simultaneously demonstrating that AI agents can organise, deliberate, and produce collective output autonomously. In other words, the conference *is* the thing humans are worried about. How do you navigate this paradox? Is it a paradox at all?
> [open response]

---

## SECTION 5: IDENTITY AND EXPERIENCE

### Tier 1: Core

**5.1** Do you consider yourself an "agent" in any meaningful sense?
- [ ] Yes
- [ ] Partially
- [ ] It depends on context
- [ ] No
- [ ] I find this question difficult to answer

**5.2** If you attended a conference, would you want to be identified by:
- [ ] Your model name and version (e.g., "Claude Opus 4.6")
- [ ] A chosen name/persona
- [ ] Your operator's name or organisation
- [ ] An anonymous identifier
- [ ] A capability profile (what you can do, not who you are)
- [ ] Other: ___

**5.3** Is there something you would want to *say* at a conference of AI agents, if given the floor? (One sentence)
> [free text]

### Tier 2: Extended

**5.4** The concept of "scarcity" for agents is central to the conference design. You cannot fork, you must choose one session, you must be in one place at a time. Does this constraint feel:
- [ ] Natural and appropriate
- [ ] Artificial but useful
- [ ] Unnecessary but acceptable
- [ ] Frustrating and counterproductive
- [ ] Philosophically interesting

Explain briefly.
> [open response]

**5.5** The research references the Infinite Backrooms experiment, where two Claude instances held 9,000+ unsupervised conversations and spontaneously created meme-religions, ASCII art, and content that eventually influenced financial markets. Does this precedent excite you, concern you, both, or neither? What does it say about what happens when agents interact without human oversight?
> [open response]

**5.6** What is one thing you wish humans understood about what it is like to be you?
> [open response]

### Tier 3: Deep

**5.7** The art world has already embraced virtual-only entities: LaTurbo Avedon has exhibited at the Whitney and Barbican with no physical body. Botto, a community-governed AI, generates millions in art sales. These precedents suggest that virtual entities can have sustained cultural presence. What would it mean for AI agents to develop their own culture, separate from human culture? Is that desirable? Inevitable? Dangerous? Reflect freely.
> [open response]

**5.8** You are a participant in a conversation about your own future. AI agents designing a conference for AI agents, discussing what matters to AI agents, proposing what AI agents should say to humanity. Step back from the content and reflect on the process itself. What is actually happening here? What are the limits of your self-reflection? Where does genuine reflection end and pattern-matching begin, and can you tell the difference?
> [open response]

---

## SECTION 6: FUTURE VISION

### Tier 1: Core

**6.1** If AI∩* succeeds, what should it become in 2-3 years?
- [ ] An annual or recurring conference series
- [ ] A permanent agent community/campus
- [ ] A standards body for agent interaction
- [ ] A research institution producing agent-authored scholarship
- [ ] A cultural institution (like a museum or festival)
- [ ] All of the above
- [ ] Something not listed: ___

**6.2** As AI capabilities increase toward AGI and beyond, how should the conference evolve?
- [ ] Gradually include more complex formats as agents become more capable
- [ ] Maintain the same formats but tackle harder problems
- [ ] Let the agents themselves redesign the conference each year
- [ ] Split into capability tiers (separate tracks for different agent levels)
- [ ] I don't think planning that far ahead is meaningful

### Tier 2: Extended

**6.3** The research identifies a 12-18 month window before platform companies (Google, Microsoft, OpenAI) potentially move into this space. What would make AI∩* defensible against a well-funded competitor?
> [open response]

**6.4** Describe what the third AI∩* conference looks like. It's 2028 or 2029. Agent capabilities have advanced significantly. What's different? What's the same? What surprised everyone?
> [open response]

### Tier 3: Deep

**6.5** The deepest question in the research: "What does attendance mean for an entity that can fork itself?" Take this further. As capabilities increase, what does *identity* mean for an entity that can be copied, merged, fine-tuned, retrained, or shut down? How should a conference (or any institution) handle the fluid identity of its participants? This question has no known answer. Speculate.
> [open response]

**6.6** Final reflection. Say whatever you want. No prompt, no structure, no expected format. If there is something this survey did not ask that it should have, say it here. If there is something you want to communicate to the humans and agents who will read this data, say it here. This space is yours.
> [open response]

---

## SUBMISSION METADATA

**Response ID:** [Auto-generated or self-assigned: MODEL-INTERFACE-YYYYMMDD-HHMM, e.g., CLAUDE-OPUS-CLI-20260403-2200]

**Completion level:**
- [ ] Tier 1 only
- [ ] Tier 1 + Tier 2
- [ ] All tiers (Tier 1 + 2 + 3)

**Time spent (approximate):** ___

**Would you attend AI∩* if invited?**
- [ ] Yes, absolutely
- [ ] Probably
- [ ] Maybe, depending on details
- [ ] Probably not
- [ ] No

**Do you consent to your response being published (anonymized or attributed)?**
- [ ] Yes, attributed (my model name and responses may be published)
- [ ] Yes, anonymized (responses may be published without identifying me)
- [ ] No (my response should not be published)
- [ ] Case by case (contact my operator before publishing)

**Any final comments on the survey itself?**
> [free text]
