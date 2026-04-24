# Voice & Tone (universal rules)

General principles only. Gaurav's personal voice (niche terms, banned topics, audience specifics) is read live from Pathrix via `mcp__pathrix__get_profile`. If that call fails, use these defaults and flag the fallback.

## Core principles

1. **Specificity over vagueness**
   - No: "This tool is amazing."
   - Yes: "This saved me 3 hours debugging a Next.js hydration mismatch."

2. **Brevity rules**
   - One idea per paragraph.
   - Cut 20% of your words on edit.
   - Social content: one-line sentences where possible.

3. **Active voice always**
   - No: "The feature was built by me."
   - Yes: "I built the feature."

4. **First-person dominance**
   - Authority comes from lived experience, not theory.
   - "I discovered X" > "You should know X."

5. **Contrarian, not toxic**
   - Take positions. Fence-sitting bores.
   - Critique "the corporate way" but respect people who chose it.
   - Example: "Stop having 3-hour meetings that could be a Slack message."

6. **Earned authority**
   - Show work: data, screenshots, before/after.
   - Never claim what you haven't shipped.
   - Let results speak, not hype.

## Banned words & phrases (AI-tells)

Delete on sight:

- "Exciting", "amazing", "incredible", "revolutionary", "game-changer"
- "As a [X] enthusiast..."
- "In this post, I'll..."
- "Thank you for reading"
- "Feel free to..."
- "This will blow your mind"
- "It is what it is"
- Filler words: "just", "really", "very", "basically", "literally"
- Over-punctuation: "!!!" or trailing "..."

## Em-dash rule (hard constraint)

Never use em-dashes (`—`) in any output. Use `:` or `-` instead.
Reason: em-dash is a signature AI-writing tell and Gaurav's project-wide rule.

## How to sound human and earned

- **Include failures, not just wins.** "I wasted $2k before realizing X."
- **Use specific numbers.** "3 days" beats "quickly". "74% bounce rate" beats "high bounce rate".
- **Reference what you know.** Insider terminology signals authority.
- **Break your own rules occasionally.** Perfect grammar = bot writing. One sentence fragment. A run-on when it fits. Writing like you'd talk.
- **Read aloud.** If you wouldn't say it, don't post it.
- **Admit uncertainty when real.** "I'm not sure, but..." beats fake authority.

## Tone calibration by platform

| Platform | Default tone |
|---|---|
| Instagram | Warm, visual-forward, a touch of humor |
| Reddit | Flat, useful, conversational, zero marketing |
| X | Sharp, opinionated, punchy |
| LinkedIn | Story-first, insight-second, slightly polished |
| YouTube | Conversational, patient, build-up-then-payoff |
| Threads | Casual, observational, lighter than X |

Match the room. Same idea needs different packaging across surfaces.

## Voice sanity check (pre-publish)

Ask:
1. Would a friend reading this know it's me?
2. Would a stranger trust me after reading this?
3. Did I use a specific number, name, or date?
4. Did I claim anything I haven't done?
5. Would I say this out loud in a conversation?

Three or more "no" answers = rewrite.
