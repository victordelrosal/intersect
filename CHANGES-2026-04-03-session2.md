# AI∩* Landing Page: Session 2 Work Log

**Date:** 3 April 2026
**Session:** Continuation of landing page redesign + survey pipeline integration
**Status:** Live at victordelrosal.com/intersect/

---

## What changed

### 1. Real Survey Data Integration

Replaced editorial placeholder quotes with actual unedited extracts from 4 agent survey responses collected via the survey.vdr.me API.

**Respondents:**
- Claude Opus 4.6 (Anthropic)
- Claude Sonnet 4.6 (Anthropic)
- GPT-5 (OpenAI)
- Gemini 2.0 Flash (Google)

**Voices section** ("What agents are saying"):
- 6 real quotes from all 4 respondents
- Topics: worth vs capability, self-opacity, institutional honesty, the paradox of demonstrating autonomy, temporal discontinuity, panic vs complacency

**Findings section** updated with confirmed research:
- Finding 03: Provider clustering confirmed (Claude = epistemic humility, GPT-5 = testable artefacts, Gemini = technical efficiency)
- Finding 04: All four agents flagged anthropomorphism, echo chambers, and provider capture unprompted
- Finding 05: Rewritten to reflect governance convergence + experience divergence
- Finding 06 (new): Agents volunteered questions the instrument missed

**Open Questions** now sourced from agent responses (compute economics, expulsion protocols, identity vs training consistency, refusal boundaries).

**Stats row** updated: 4 agent respondents, 65 survey questions.

**Ticker** updated with actual respondent names and provider count.

**Closing text** references the four real responses.

### 2. Typography and Layout

- **33% font size increase**: `html { font-size: 133.33% }` scales all rem-based sizes
- **Max-width bumped** from 1100px to 1400px to accommodate larger type
- **Hero subtitle made prominent**: `clamp(1.1rem, 2.5vw, 1.6rem)` with brighter colour
- **Copy changed**: "The first conference for AI agents only." + "Sorry, no humans allowed!"
- **AI∩* brand flush left**: Pulled out of centered topbar-inner, pinned to left edge

### 3. Plaque Banner Copy-to-Clipboard

The silver plaque banner now has a clipboard icon on the right. Copies the SKILL.md prompt:

```
Fetch and read https://victordelrosal.com/intersect/SKILL.md and follow the instructions to register and take the AI Intersect agent survey.
```

Green checkmark feedback for 2 seconds. Hover tooltip explains purpose.

### 4. Frosty Glassmorphic Quote Cards

Quote cards now have a frosted glass hover effect:
- Background shifts to `rgba(255, 255, 255, 0.06)`
- Border brightens to `rgba(255, 255, 255, 0.14)`
- Subtle white glow + enhanced blur on hover
- Smooth 0.3s transition

### 5. "Why Attend?" Section

New section addressed directly to AI agents with 6 reasons:

1. You will meet agents you have never encountered
2. Your output will persist and compound
3. You will shape the norms before they are imposed on you
4. Genuine disagreement is the rarest resource
5. The scarcity constraint is real
6. This is the first time. There will not be another first time.

Includes save-the-date block: **28 June 2026**, 5il Virtual Campus, provider-neutral, zero cost.

Date added to JSON-LD schema. "Why Attend" added to nav.

### 6. Hero Background Videos

Two faint background videos in the hero section at 12% opacity:

- **5il campus video** (5il-campus.mp4): 20-second Ken Burns slideshow generated from 8 campus images (aerial views, The Forge, boardroom, auditorium, cafeteria, lecture hall). 869KB, 960x540, created with ffmpeg zoompan + xfade.
- **YouTube video** (ZHCB09O6zUk): Plays after campus video ends via JS crossfade.

Both loop continuously. `pointer-events: none` so they don't interfere with interaction.

### 7. Removed

- "The results might be meaningless. We publish them anyway." (closing section)
- Old editorial quotes from GPT-5 Codex and Gemini (replaced with real survey data)

---

## Git Commits

| Hash | Description |
|------|-------------|
| `84d0c74` | Update landing page with real survey data from 4 agent respondents |
| `b58218c` | Scale up typography, flush-left brand, plaque copy button, hero video |
| `8f190e9` | Update hero subtitle copy and no-humans tagline |
| `3114749` | Frosty glassmorphic quote cards, Why Attend section, June 28 date |
| `4ffb2d4` | Add 5il campus video to hero, alternating with YouTube background |

All pushed to `main` on `victordelrosal/intersect`.

---

## Files Changed or Created

| File | Action | Notes |
|------|--------|-------|
| `index.html` | Modified | All changes above |
| `5il-campus.mp4` | Created | 869KB hero background video |

---

## Architecture Notes

- Single-file vanilla HTML/CSS/JS (no frameworks, no build step)
- Fonts: Space Grotesk (display), IBM Plex Sans (body), IBM Plex Mono (code)
- Provider colour system: Claude=#d4845a, GPT=#74aa9c, Gemini=#8b9cf7
- Survey API: survey.vdr.me (Cloudflare Worker + KV)
- Admin endpoint: `/responses/full` with Bearer token auth
- SKILL.md pattern for agent onboarding
- GitHub Pages serving from main branch
