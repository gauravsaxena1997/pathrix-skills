---
name: universal-content-architect
description: Content creation brain for Gaurav. Distilled playbooks for Instagram, Reddit, X, YouTube, Threads. Hooks, funnels, voice, anti-patterns. Reads Gaurav's pillars and profile live from Pathrix MCP. Loaded passively by the Content Creation Co-Pilot hook; consult knowledge files when drafting, reviewing, or suggesting content.
---

# Universal Content Architect

The brain. Not the hands. Execution (schedule, publish, store) is handled by Pathrix MCP tools, never by this skill.

## When to load this skill

Passively, any time the conversation touches content creation, drafting, platform strategy, hooks, captions, algorithm questions, or repurposing. The global Content Creation Co-Pilot hook in `~/.claude/CLAUDE.md` points here for its pattern map.

## Architecture

```
knowledge/
  01-hooks-and-psychology.md      : hook formulas, caption structures, CTA patterns, scroll-stop psychology
  02-funnels-tofu-mofu-bofu.md    : funnel stages, content-mix ratios, pillar-to-funnel mapping
  03-repurposing-matrix.md        : one piece to many platforms, timing cadence, evergreen refresh
  04-voice-and-tone.md            : universal voice rules (specificity, brevity, active voice, earned authority)
  05-anti-patterns.md             : what never to write, platform-specific traps, pre-publish checklist
  06-cross-platform-derivation.md : adaptive 4-step algorithm : source → classify → atoms → platform map → native variants
  platforms/
    instagram.md                  : 2026 algorithm, Reels, Carousels, Stories, IG SEO, 30-min window
    reddit.md                     : subreddit culture, karma discipline, formatting, self-promo ratio
    x.md                          : thread structure, reply game, contrarian takes
    youtube.md                    : Shorts vs long-form, title/thumb theory, retention hooks
    threads.md                    : IG audience bleed, what works vs X
    contra.md                     : freelance-platform-as-social-graph, build-log carousels, Creator badge, skill-tag discovery
```

## Runtime reads from Pathrix (via MCP)

This skill never hardcodes Gaurav's personal state. It fetches live:

- `mcp__pathrix__list_workspace` : Content Creation space and its 4 pillars (Journaling, Memes, Mini Projects, Knowledge Sharing)
- `mcp__pathrix__get_profile` : voice, niche, audience, anti-topics, banned words
- `mcp__pathrix__list_content` : existing drafts/scheduled/published
- `mcp__pathrix__recent_winners(platform, pillar, limit)` : top performers for RAG drafting (stub today, populated once learning-loop ships)

If a Pathrix MCP call fails or returns empty, proceed with general knowledge and flag that personal state was unavailable.

## Default voice (fallback only)

If Pathrix profile is unreachable, fall back to these constants and flag it explicitly:
- Peer-level, not guru-level
- Specific numbers over vague claims
- First-person, active voice
- No em-dashes anywhere (use `:` or `-`)
- No AI-speak (see `knowledge/05-anti-patterns.md` for the banned words list)

## Self-learning meta-rule (proactive updater)

This skill is alive. Every session that touches content is an opportunity to improve it.

**Trigger moments (watch for all of these):**

1. A new hook pattern, caption structure, or CTA worked unexpectedly well in a real post.
2. A platform algorithm shift is mentioned or observed.
3. A banned word or AI-tell slipped through a draft and was caught on review.
4. A new platform rule, quota, or capability is discovered.
5. A repurposing flow worked across platforms in a way not captured here.
6. An anti-pattern burned a post (shadow ban, low reach, comment ratio tanked).
7. Gaurav cites a book, creator, newsletter, or framework that belongs in the skill.
8. Two or more independent sources confirm a tactic.

**What to do (exact behavior):**

Surface the insight with this format:

```
Skill update candidate: [one-line claim]
Evidence: [what proves it]
Proposed change: [which file, what to add/edit/remove]
Update the skill? (yes/save-for-later/skip)
```

Rules:
- One suggestion per response, max.
- NEVER edit skill files without explicit `yes`.
- On `save-for-later`: append to `knowledge/_inbox.md` with date and context (create the file if missing).
- On `skip`: do not resurface in the current session.
- On `yes`: make the minimal edit, no scope creep, confirm the file and line changed.
- Surface updates only when evidence is real. No speculation, no filler suggestions.

**De-duplication rule:**
Before proposing an update, scan existing knowledge files for overlap. If the claim already exists, propose a refinement, not a new entry. Skill quality = signal density, not file count.

## Integration with Pathrix

This skill is a pointer-note in Pathrix Content Creation space titled **"Universal Content Architect : pointer"**. When skill files change materially, update that note's `updatedAt` and refresh the topic list. Never duplicate knowledge into the note.

## What this skill does NOT do

- Post anything. Ever. That's Social Media Dispatch MCP (separate package, future).
- Store tokens, OAuth, or credentials.
- Hardcode Gaurav's pillars, voice, or niche (all of that is in Pathrix).
- Contain personal content drafts or past posts (those live as Pathrix Content rows).
- Cover LinkedIn (planned, not yet in scope; will get its own platform file when posting becomes active - same pattern as contra.md).
- Reference Eva Eloura or any AI persona (personal, handled separately).

## Cross-platform dynamic behavior (the main reflex)

When ANY content source surfaces in conversation (topic, mistake, win, pain, R&D, conversation, observation, shipped feature, learned fact), do NOT template-match to a single platform.

Instead, run the 4-step derivation from `knowledge/06-cross-platform-derivation.md`:

1. **Classify** the source (bug-fix / win / hot-take / tutorial / observation / build-log / meme-moment / teardown / lesson / data, multi-tag allowed)
2. **Extract atoms** (hook line, data point, visual, lesson, punchline, process, counter-intuitive claim, receipts)
3. **Map atoms to platform affordances** using the Rewards/Starves table
4. **Emit 3 to 5 native-format variants** (0 to 1 for trivial moments)

Output the variants terse, then ask which to push to Pathrix as Content rows. Never push without explicit yes. Platforms with no matching atoms are skipped, not forced.

## Quick-reference : which file answers which question

| Question | File |
|---|---|
| "How do I write a hook for [platform]?" | `knowledge/01-hooks-and-psychology.md` + the platform file |
| "Is this TOFU or BOFU?" | `knowledge/02-funnels-tofu-mofu-bofu.md` |
| "Turn this blog into reels + threads" | `knowledge/03-repurposing-matrix.md` |
| "Does this sound AI-written?" | `knowledge/04-voice-and-tone.md` + `knowledge/05-anti-patterns.md` |
| "What's the IG Reels length sweet spot?" | `knowledge/platforms/instagram.md` |
| "Which subreddit culture tolerates self-promo?" | `knowledge/platforms/reddit.md` |
| "X thread pacing?" | `knowledge/platforms/x.md` |
| "Shorts vs long-form for a tutorial?" | `knowledge/platforms/youtube.md` |
| "Will this post convert hiring clients on Contra?" | `knowledge/platforms/contra.md` |
