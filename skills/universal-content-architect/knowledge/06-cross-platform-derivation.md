# Cross-Platform Derivation (Adaptive, Not Hardcoded)

For ANY content source that surfaces in a session (topic, mistake, win, pain, R&D, conversation, observation, shipped feature, learned fact), derive 3 to 5 platform-native variants using the algorithm below.

**Do not pick platforms by template matching (e.g. "bug fix → always goes to X"). Run the algorithm every time; the output platform mix depends on the source's atoms, not its category.**

## The 4-step algorithm

### Step 1: Classify the source

Place the source into one (or more) of these tags. A source can carry multiple tags at once.

| Tag | What it looks like |
|---|---|
| `bug-fix` | something was broken, you fixed it, there's a before/after |
| `win` | shipped / signed / crossed a threshold |
| `hot-take` | opinion you'd defend under pressure |
| `tutorial` | step-by-step that someone else could follow |
| `observation` | pattern you noticed (no strong claim yet) |
| `build-log` | in-progress work, screenshot-worthy |
| `meme-moment` | absurd / ironic / relatable pain |
| `teardown` | analyzing someone else's work (tool, post, product) |
| `lesson` | mistake → learning, transferable |
| `data` | number or stat that surprised you |

Multi-tag is common. A bug-fix that took 2 hours and humbled you is `bug-fix + lesson + meme-moment`.

### Step 2: Extract the atoms

From the source, pull out whatever of these exist. Most sources have 3 to 5.

- **Hook line** : the single sentence that makes someone stop
- **Data point** : a number, duration, cost, ratio
- **Visual** : screenshot, diagram, before/after, demo clip, emoji-in-terminal
- **Lesson** : the transferable one-liner someone could quote
- **Punchline** : the absurd / ironic twist
- **Process** : the ordered steps (if any)
- **Counter-intuitive claim** : something that sounds wrong but isn't
- **Receipts** : proof (screenshot of commit, output, graph, ticket)

An atom that doesn't exist is fine. Don't invent it.

### Step 3: Map atoms to platform affordances

Each platform rewards different atoms. Match, don't force.

| Platform | Rewards | Starves |
|---|---|---|
| **Instagram Reel** | Visual, punchline, hook line | Pure text, long process |
| **Instagram Carousel** | Process, lesson, data, visual | Meme-moment without depth |
| **Instagram Story** | Build-log, behind-the-scenes, quick win | Polished takes |
| **X single tweet** | Hook line, counter-intuitive claim, punchline | Process, long data |
| **X thread** | Process, lesson, receipts, data | Thin punchlines |
| **X reply (to niche account)** | Counter-intuitive claim, data, extension | Self-promotion |
| **Reddit post** | Lesson, process, data, receipts (long form) | Hook-only, meme without context |
| **YouTube Short** | Visual, punchline, counter-intuitive + receipt | Pure text, slow openers |
| **YouTube long-form** | Process, tutorial, teardown, receipts | One-liners, meme-moments |
| **Threads** | Observation, meme-moment, hook line, visual | Hard takes, long process |
| **Contra post** | Visual, build-log, process, lesson, receipts | Pure text takes, meme-moments without a lesson |

### Step 4: Emit native-format variants

For each matched platform, write the variant in that platform's native grammar. Never paste the same text across platforms.

Format per variant:

```
PLATFORM · FORMAT · EFFORT (low/med/high)
Hook / first line : "..."
Body sketch : ...
CTA (if any) : ...
```

Quality bar: if the variant could work on a different platform unchanged, it's not native enough. Rewrite.

## Frequency & quantity

- **Substantive moment** (shipped feature, real lesson, real data, hot take with receipts) : emit 3 to 5 variants
- **Trivial moment** (fixed typo, small commit) : emit 0 or 1
- **Polarizing hot take** : emit 2 (X single + Reddit post), skip IG (IG doesn't reward heat)
- **Visual-first win** (demo, before/after) : IG Reel or YT Short MUST be one of the variants

## Worked example 1 : Bug fix that took too long

**Source:** "Spent 3 hours debugging a Prisma migration that silently wiped my dev DB because seed script had deleteMany. Turns out I'd added --prod guard but not dev."

**Tags:** `bug-fix + lesson + meme-moment + build-log`

**Atoms:**
- Hook line : "I just nuked my dev DB in 3 lines of code."
- Data : 3 hours lost
- Lesson : guard destructive scripts at every env, not just prod
- Visual : terminal screenshot of the empty tables + git blame of the bad line
- Punchline : "the --prod guard was my seatbelt. I forgot to wear it in the parking lot."
- Receipts : the actual commit hash, the before/after row count

**Variants (5):**

```
X single · tweet · low
Hook : "Fun fact: your --prod guard does nothing if the dev path is also destructive."
Body : one-liner + before/after row count screenshot
CTA : none
```

```
X thread · 5 tweets · med
T1 : "I nuked my own dev DB in 3 lines of code. Here's how."
T2 : the seed script excerpt (code block)
T3 : the --prod guard + what it missed
T4 : the actual 3-hour rabbit hole (recovery steps)
T5 : the fix (guard at every env). Link to blog if any.
```

```
Reddit (r/node or r/webdev) · post · med
Title : "Guarded my seed script against prod. It still destroyed my dev DB. Here's what I missed."
Body : lesson-first, then process, then code, then TL;DR
No link.
```

```
Instagram Reel · 20s · med
Frame 1 (0 to 2s) : terminal screenshot zooming into "0 rows"
Frame 2 (2 to 10s) : talking head : "I added a --prod guard. Then I ran seed on dev."
Frame 3 (10 to 18s) : before/after row counts + the missing guard line highlighted
Frame 4 (18 to 20s) : "Guard every env. Not just prod." + looping hook
Caption : short lesson + 1 CTA (save this)
```

```
YouTube Short · 45s · med
Same beats as Reel but room for a slower lesson. End with tease for a build-in-public video.
```

**Skipped:** Threads (no original atom worth repeating from IG), IG Story (redundant with Reel), YT long-form (not enough content for 5+ mins).

## Worked example 2 : Shipped feature win

**Source:** "Shipped Pathrix Scout yesterday. Semantic search across 4 platforms with sqlite-vec. Indexed 2000 docs."

**Tags:** `win + build-log + tutorial (partial) + data`

**Atoms:**
- Hook line : "I just shipped semantic search across 4 platforms. Runs on a laptop."
- Data : 2000 docs indexed, sqlite-vec embeddings, cost = $0 (no Pinecone)
- Visual : demo clip of search working, architecture diagram
- Lesson : "sqlite-vec is underrated; you don't need Pinecone for <10k docs"
- Process : the indexing pipeline (4 platforms → chunks → embeddings → sqlite-vec)
- Receipts : screenshot of query returning results across platforms

**Variants (5):**

```
X single · tweet · low
"Semantic search across 4 platforms. 2000 docs indexed. Runs on a MacBook. No Pinecone. sqlite-vec is insane."
+ demo clip (10s)
```

```
X thread · 7 tweets · med
T1 : counter-intuitive hook ("you don't need a vector DB")
T2 to T5 : the pipeline (one step per tweet)
T6 : the tradeoffs (where sqlite-vec breaks)
T7 : receipts + link to repo if open
```

```
Instagram Carousel · 8 slides · med
Slide 1 : "I built semantic search without a vector DB"
Slide 2 : why not Pinecone
Slides 3 to 6 : the 4-step pipeline
Slide 7 : the receipts (query demo screenshot)
Slide 8 : save-worthy takeaway + CTA
```

```
YouTube long-form · 8 to 12 min · high
Build-in-public walkthrough. Chapters : problem, approach, code, demo, tradeoffs.
```

```
Reddit (r/LocalLLaMA or r/SaaS) · post · med
Title : "Built semantic search for 4 social platforms using sqlite-vec instead of Pinecone. Here's the architecture."
Body : architecture diagram, code excerpts, cost breakdown, where it breaks.
```

**Skipped:** IG Reel (too process-heavy for 30s), Threads (win-flavored, better as Reel-driven), YT Short (build-ins don't fit short form).

## Worked example 3 : Conversational observation

**Source:** Mid-conversation, you said "Most devs think MCP is about tool use. It's actually about context windows."

**Tags:** `hot-take + observation`

**Atoms:**
- Hook line : the quote itself
- Counter-intuitive claim : yes, exactly that
- Visual : none (yet)
- Receipts : thin (it's an opinion)

**Variants (2):**

```
X single · tweet · low
"Most devs think MCP is about tool use. It's actually about context windows."
No thread. Let replies do the work.
```

```
Threads · post · low
Same line, softer tone : "Hot take : MCP is a context-window play, not a tool-use play."
+ short follow-up reply with one example.
```

**Skipped:** Reddit (needs receipts to survive), IG (no visual), YouTube (too thin). Log the topic as a future carousel/video once you have a demo.

## How to use this at runtime

When a moment qualifies:

1. Run all 4 steps silently
2. Output the variants in the response as a single block, terse format
3. Ask which to push to Pathrix (`create_content` with platform + pillarId)
4. Do not create content without explicit yes
5. Only push variants the user approved, each as its own Content row

## What NOT to do

- Don't template. A bug-fix is not always a Reddit post.
- Don't force all 5 platforms. Some sources genuinely only work on 2.
- Don't paste the same text with platform tags stripped off.
- Don't skip the atom step : variants generated without atoms are generic and feel AI-written.
- Don't invent receipts. If there's no data, don't fake a number.
