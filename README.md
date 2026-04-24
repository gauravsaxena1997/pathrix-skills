# Pathrix Skills

Open-source Claude Code skills extracted from [Pathrix](https://github.com/gauravsaxena-dev/pathrix), a personal Career OS.

## What this repo is

A collection of Claude Code skills built while using Claude as a daily operating partner. Each skill is a focused, reusable unit of knowledge that Claude can load when the context calls for it : no plugin install, no runtime, just Markdown + conventions that ship with the model.

Skills here started as private `~/.claude/skills/` tooling. They get promoted to this repo once they are stable enough that other people might want them.

## Belief behind the skills

1. **Distilled over exhaustive.** A skill is a signal-dense playbook, not a wiki. If a skill file can't be read end-to-end in ten minutes, it is too big.
2. **Knowledge on disk, state in the user's system.** A skill captures timeless playbooks. User-specific state (pillars, goals, voice, past content) lives wherever the user keeps it. The skill reads from that source at runtime; it never hardcodes personal data.
3. **Single source of truth.** Knowledge exists in exactly one place. Pointer notes elsewhere reference it; they don't duplicate it. Duplication rots fast.
4. **Self-learning by default.** Skills are alive. When a new pattern, algorithm shift, or banned-word tell shows up in conversation, the skill proposes an update in a structured format. Updates happen only with explicit approval, never silently.
5. **Brain not hands.** Skills advise, decide, and draft. Execution (posting, scheduling, OAuth, API calls) belongs in separate MCP servers. Keep them decoupled.
6. **No AI-speak.** Skills avoid em-dashes, filler words, guru-tone, and AI-tell vocabulary. Voice rules are enforced at the skill level.

## Skills in this repo

### `universal-content-architect`

Content creation brain for solo creators. Distilled playbooks for Instagram, Reddit, X, YouTube, Threads : hooks, funnels, voice, anti-patterns, and a cross-platform derivation algorithm that turns any content source (topic, mistake, win, R&D moment, observation) into 3 to 5 platform-native variants without hardcoded templates.

Knowledge structure:
- `01-hooks-and-psychology.md` : hook formulas, caption structure, CTA patterns
- `02-funnels-tofu-mofu-bofu.md` : funnel stages, content mix, pillar mapping
- `03-repurposing-matrix.md` : one piece to many platforms, cadence, refresh cycle
- `04-voice-and-tone.md` : universal voice rules, banned words, em-dash rule
- `05-anti-patterns.md` : platform traps, algorithm-damage patterns, pre-publish checklist
- `06-cross-platform-derivation.md` : 4-step adaptive algorithm with worked examples
- `platforms/*.md` : per-platform blueprints (Instagram, Reddit, X, YouTube, Threads)

Reads the user's pillars, profile, and content state at runtime from Pathrix MCP (or any equivalent source of truth). LinkedIn and AI-persona content are intentionally out of scope for v1.

## How to install

```bash
git clone https://github.com/<your-handle>/pathrix-skills.git
cp -R pathrix-skills/skills/universal-content-architect ~/.claude/skills/
```

Then in any Claude Code session, the skill loads automatically when the conversation touches content creation.

## Contributing

These skills are opinionated and tuned to one creator's voice. Forks and variants are encouraged; PRs that change voice rules or platform opinions will usually be asked to fork. PRs that fix bugs, typos, or outdated platform rules (e.g. new algorithm signals, API quota changes) are welcome.

## License

MIT : see [LICENSE](LICENSE).
