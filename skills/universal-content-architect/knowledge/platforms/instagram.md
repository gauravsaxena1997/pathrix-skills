# Instagram (2026)

## Algorithm : multiple systems

IG runs separate AI systems per surface. What works on Reels will flop on Feed.

- **Feed** : relationship + speed of engagement
- **Stories** : posting recency + relationship strength
- **Reels** : discovery-focused, quality-driven, non-follower distribution
- **Explore** : interest-based, non-follower discovery

**Ranking signals (by weight):**
1. Engagement history with your account
2. Content performance speed (engagement velocity after post)
3. Relationship strength (interaction frequency)
4. Content info (format, timing, keywords, hashtags)
5. Poster credibility (consistency, niche clarity)

## Metrics that actually matter (ranked)

1. **Saves** : long-term value signal
2. **Shares / sends** : social relevance signal
3. **Watch time / completion rate** (Reels) : 75%+ is gold
4. **Repeat views** : rewatches trigger distribution
5. **Comment depth** : 5+ word replies beat one-word reactions
6. **Profile visits from non-followers** : curiosity + trust signal
7. Likes and surface comments : secondary, not primary anymore

**Originality score:** recycled TikTok clips or verbatim trending content tank reach. Original or unique spin only.

## Reels strategy

### Length

- 15 to 30 seconds : viral potential
- 60 to 90 seconds : storytelling
- Never artificially cut or pad

### Hook structure

- First 1.5 seconds : visual or text interrupt (zoom, cut, overlay)
- Last 10 seconds : matter more than first 3. Completion = king.
- Looping : end mirrors beginning for rewatches

### Audio mix (over a month)

- 40% trending audio
- 30% original voiceover
- 20% original music or baked-in track
- 10% text-only no audio

### Captions on video

Always add burned-in captions. Improves watch time by 40%+.

### Posting cadence for growth

3 to 5 Reels per week. Use "Trial Reels" (shown only to non-followers) to test zero-risk.

## Carousel strategy

- **5 to 10 slides** : sweet spot
- **Slide 1** : hook / curiosity (headline)
- **Slide 2** : the why (stakes, problem)
- **Slides 3 to 7** : the how (one tactic per slide)
- **Slide 8** : summary or example
- **Slide 9** : CTA (save/share priority)

Consistent template design builds brand recognition.

## Stories strategy

- Post daily : active accounts appear higher in search
- Interactive stickers (polls, questions, quizzes) boost engagement signal
- Behind-the-scenes outperforms polished
- Share new posts as Story reposts for extra visibility
- "Add Yours" sticker : viral potential
- 5 to 7 Stories/day minimum for signal of active creator

## IG SEO : keywords > hashtags in 2026

Instagram is a search engine now.

**Where keywords go:**
- Username (include primary keyword if possible)
- Bio (natural keyword inclusion)
- Caption (first 125 characters = most important)
- Alt text (describe images with keywords)
- Hashtags : secondary now, use 5 to 15 relevant + specific (not generic)

## 30-minute engagement window protocol

IG tests posts with a small group immediately after posting. High retention = expanded distribution.

1. **Before posting :** engage with followers for 15 minutes
2. **Post content**
3. **First 30 minutes :** reply to every comment
4. **After posting :** engage with niche content for 15 minutes
5. **Immediately :** share post to Stories

## Organic growth (7-step system)

1. Tight niche, stay in it : topic cluster clarity drives distribution
2. Profile optimized for search (keywords in name, bio, alt text)
3. Consistent posting : 3 Reels + 2 Carousels + 5 Stories/week minimum
4. Engage deeply with niche community
5. Use Trial Reels to test zero-risk
6. Collab feature with complementary accounts
7. Iterate weekly on watch time %, saves per 1K views, shares per 1K views

## Weekly metric targets

| Metric | Target |
|---|---|
| Reel completion rate | 75%+ |
| Saves per 1,000 views | 3%+ |
| Shares per 1,000 views | 2%+ |
| Engagement per follower | 5 to 10% |
| Profile visits (non-follower) | Week-over-week positive trend |

## Hashtag strategy (concrete)

- Use 5 to 15 per post (not 30, not 3)
- Mix: 40% niche-specific (10k to 100k posts), 40% mid-tier (100k to 500k), 20% broad (<1M)
- Never use: #instagood, #love, #photooftheday, #follow4follow
- Rotate hashtag sets every 2 to 3 weeks to avoid shadow-ban signals

## What cannot be done via Graph API

(Relevant when Social Media Dispatch ships.)

- Attach trending audio from IG library to Reels or Carousels : API-blocked for rights reasons.
- Save drafts via API.
- Edit posts after publishing (except caption).
- Reply to DMs at scale.

Workaround for trending audio: Dispatch flags `manual_required`, sends Discord ping with prepared media, Gaurav finishes in-app in ~30 seconds.
