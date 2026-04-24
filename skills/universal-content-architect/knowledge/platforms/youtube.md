# YouTube

Two formats, two different games. Shorts is TOFU (reach). Long-form is MOFU / BOFU (trust, leads, authority).

## Shorts (under 60 seconds)

### When to use

- Quick tutorials
- One-shot demos
- Meme-style niche humor
- Hook + resolution
- Top-of-funnel discovery

### Rules

- **Hook in first 3 seconds** : visual interrupt + text overlay
- **Visual movement** : never sit still, always something changes
- **Looping structure** : end mirrors beginning
- **Caption always on-screen** (burned-in)
- **Vertical 9:16**, ideally shot vertically (not cropped)
- **Title** includes the keyword + "#Shorts"
- Length sweet spot : 15 to 30 seconds

### Hook patterns (shorts)

- "I built X in Y minutes. Watch:"
- "Stop doing X. Do this instead:"
- "3 tools I use every day:"
- Contrarian one-liner + proof

## Long-form (5 to 20 minutes)

### When to use

- Deep tutorials
- Build-in-public walkthroughs
- Opinion pieces with substantial argument
- Tool reviews
- Workflow showcases

### Retention theory

YouTube ranks on **watch time**, not views. Retention is the number one signal.

- **First 20 seconds** : hook + promise of what they'll learn
- **20 to 40 seconds** : establish credibility + set up the payoff
- **50% mark** : re-hook. Viewers bail here if not reminded why this matters.
- **Final 10 to 20 seconds** : tease the next video (builds session watch time)

### Structure for a tutorial-style video

1. Hook (promise specific outcome)
2. Problem (why this matters)
3. Approach overview (what you'll do in X steps)
4. Walkthrough (the steps)
5. Result (show it working)
6. Recap + next-video tease

### Chapters

Add chapters for videos >5 minutes. Improves retention (viewers jump to what they want, watch more overall).

## Titles

- **Curiosity gap + specificity** : "The 1 mistake ALL founders make" > "Founder tips"
- **Keyword at front** : helps search
- **Max 60 characters** (more gets cut off on mobile)
- **Numbers work** : "7 tools" > "some tools"

## Thumbnails

- **High contrast**
- **Face + expression** if relevant (humans stop for faces)
- **Arrow or circle** pointing to key element
- **Max 4 words of text**
- **Consistent style across channel** builds recognition
- **Test A/B** : YouTube's built-in thumbnail tests

## Description structure

- First 2 lines : hook + summary (this shows above "more" fold)
- Link to related content
- Timestamps (chapters)
- Tags and links
- Keep it substantive : YouTube reads description for ranking

## Cadence

- **Shorts** : 3 to 7 per week feasible for growth
- **Long-form** : 1 per week or every 2 weeks. Quality > quantity.

## What to track

- **Click-through rate (CTR)** : 6 to 10%+ is healthy. If lower, thumbnail/title issue.
- **Average view duration** : aim for 50%+ of total length.
- **Watch time** : the absolute number. Higher = more reach.
- **Subscribers per video** : trend over time.

## Gaurav-specific content angles

- Build-in-public walkthroughs (ship a feature on camera)
- Tool breakdowns (Next.js features, AI tools, MCPs)
- Freelance lessons (negotiation, proposals, pricing)
- Reaction/teardown videos (other people's apps or setups)
- "I tried X for a week" challenges

## Anti-patterns

- Cold open with no promise
- Channel-history intro on every video
- Begging for subscribes in middle of video
- Long intros (>30 seconds)
- Thumbnails with more than 4 words
- Not using chapters on videos >5 minutes
- Treating Shorts and long-form identically (different games)

## What can / cannot be done via API (for Dispatch)

- **Upload videos (Shorts + long-form)** : yes, via `videos.insert`
- **Schedule publish** : yes, native `publishAt` field
- **Set thumbnail** : yes, via `thumbnails.set`
- **Captions upload** : yes
- **Playlist management** : yes

**Quota reality:** 1600 quota units per video upload. Default daily quota 10,000 = ~6 uploads/day max. Plenty for current cadence.
