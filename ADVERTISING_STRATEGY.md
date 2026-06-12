# Design & Destiny — Advertising Strategy

**Goal:** Drive paid Skool community memberships for Design & Destiny (Taksa Astrology + Behavioral Feng Shui) using destiny.ac as the conversion hub.

---

## 1. The core asset: the free 2-minute diagnostic

destiny.ac already has the single best ad funnel format that exists for this category: a free, no-signup, 2-minute personality/home reading. Quiz funnels consistently outperform direct "join my community" offers because the ad only has to sell curiosity, not commitment.

**Funnel:**

```
Short-form video ad (Meta / TikTok / YT Shorts)
        ↓
Free Taksa or Feng Shui diagnostic on destiny.ac
        ↓
Personalized results page + email capture ("get your full reading")
        ↓
Email nurture (3–5 sends) + retargeting ads
        ↓
Skool community join (free tier or trial → paid membership)
```

Everything in this document feeds the top of that funnel. The diagnostic is the conversion event we optimize ads against — not the membership purchase (too far down-funnel for the algorithm to learn on early budgets).

## 2. On Higgsfield for UGC ads — verdict: yes, as the volume engine, not the whole strategy

Higgsfield's Marketing Studio (2026) supports UGC formats — talking heads, reviews, tutorials — across 15+ models (Sora 2, Veo 3.1, Kling 3.0) with 100+ avatars. It's well suited to what this account actually needs: **high-volume creative testing**. Note that at least one third-party comparison rates HeyGen ahead for direct-to-camera talking heads, so validate Higgsfield's avatar lip-sync quality in week 1 before committing the whole pipeline to it.

**Why it fits:**
- Winning at Meta/TikTok in 2026 is a creative-volume game: 10–20 new variants/week, kill losers in 48–72h. Human UGC creators can't iterate at that speed or cost.
- The product is conceptual (personality systems), not physical — AI UGC's biggest weakness (fake product handling) doesn't apply. Talking-head "I tried this 2-minute Thai astrology test…" reactions are exactly what AI avatars do well.
- Plus plan (~$34/mo, 1,000 credits) covers early volume; Kling 3.0 at ~6 credits/video means cheap iteration, reserving Sora 2/Veo 3.1 (40–70 credits) for polished winners.

**The two caveats that matter:**

1. **Don't let AI faces carry the trust layer.** The brand's whole moat is credibility ("the only astrology methodology cleared by a university medical-research ethics board," Mae Fah Luang study, Fox/NBC/ABC features). That claim coming from a synthetic avatar undercuts it. Split the creative system:
   - **AI UGC (Higgsfield):** hooks, curiosity, reaction-style, "what's your weekday personality" angles — top of funnel, high volume.
   - **Real founders (Gut & Non) + real member testimonials:** the credibility/retargeting layer — lower volume, higher production care. These will almost certainly be your best-converting retargeting ads.
2. **Platform AI-disclosure rules.** Meta and TikTok require labeling photorealistic AI-generated people in ads. Tick the disclosure box; undisclosed synthetic "testimonials" risk ad-account bans — fatal for a new account.

## 3. Audiences & angles

Primary market is English-speaking (US-led, given the press positioning); the THB ad account is fine for this but billing/budgets will be in baht.

| Audience | Angle | Example hook |
|---|---|---|
| Personality-test enthusiasts (MBTI, Human Design, Enneagram, astrology apps like Co-Star) | "Astrology, but it survived a university ethics board" | "I'm a skeptic. Then a Thai university research study made me take this seriously." |
| Home/interior + wellness (feng shui–curious) | Behavioral Feng Shui — your address and layout, read in 2 minutes | "Your front door direction is changing your behavior. Here's how to check." |
| Life-transition moments (new home, new job, breakup, new year) | Person + place + timing as one system | "Before you sign that lease, run the address through this." |
| Skeptic-friendly / data-conscious | The differentiation play: no mysticism, behavioral observation | "You can keep guessing. Or you can know." (already the site's voice — use it) |

The **birth-weekday hook is the unfair advantage**: almost nobody in Western markets knows what weekday they were born on. "What day of the week were you born? It matters more than your star sign" creates an instant curiosity gap that the 2-minute tool resolves.

## 4. Channels & sequencing

1. **Meta (IG Reels + FB Feed) — primary paid channel.** Best quiz-funnel performance, mature optimization, and the audience demo (25–45, skews female, wellness/self-development) lives here. Start here exclusively.
2. **TikTok — organic-first for 30 days.** Post the same Higgsfield variants organically (via the Postiz scheduler already connected to this workspace) to find hooks that earn organic traction, then put paid spend only behind proven ones via Spark Ads.
3. **YouTube Shorts — repurpose only.** Zero extra production; distribution via Postiz.

**Budget phasing (assuming ~$1,500–3,000/mo to start):**
- **Weeks 1–2 (testing):** ~$50/day, 1 campaign, 3–4 ad sets by angle, 3–4 creatives each, optimized to the QuizComplete event. Kill anything above 2× target CPL after ~$30 spend.
- **Weeks 3–6 (consolidation):** shift 70% of budget to winners (Advantage+ / CBO), launch retargeting stack (quiz completers + video viewers → founder-credibility ads → Skool offer).
- **Week 7+ (scale):** raise budget ~20%/week while cost per quiz lead holds; refresh creative weekly from the Higgsfield pipeline.

## 5. Creative production system (weekly cadence)

- **Mon:** pick 3 angles from the hook bank; script 12–15 variants (vary hook, keep body/CTA stable).
- **Tue:** batch-generate in Higgsfield (Kling 3.0 for drafts); run the top candidates through the virality-predictor tooling connected here before spending a credit on premium models.
- **Wed:** launch 8–10 to Meta; post all to TikTok organic via Postiz.
- **Fri:** review; kill losers, promote winners to premium regeneration (Veo 3.1/Sora 2) and Spark Ads.
- **Monthly:** one founder-shot credibility video + one member-testimonial cut for the retargeting layer.

Name every ad `[angle]-[hook#]-[avatar]-[model]-[date]` so performance rolls up by angle, not just by ad.

## 6. Compliance (this category gets accounts banned — read this)

- **Meta personal-attributes policy:** ads cannot assert or imply knowledge of someone's personal attributes, including religion/spiritual beliefs. ❌ "Your birth weekday explains why you self-sabotage." ✅ "Most people don't know their birth weekday matters. Take the 2-minute test." Always invite, never diagnose the viewer.
- **No outcome guarantees:** never promise health, wealth, or relationship results from readings or feng shui changes. Stay in the site's lane: insight, self-understanding, practical guidance.
- **Substantiate the university claim:** "ethics-board-cleared research study" is a precise, defensible phrasing; "scientifically proven" is not. Keep the landing page's exact wording in ads, and keep the study citation one click away.
- **AI content disclosure:** label AI-generated people on both Meta and TikTok (see §2).

## 7. Measurement

Instrument the Meta Pixel + Conversions API on destiny.ac with this event ladder:

| Event | Definition | Early target (US traffic) |
|---|---|---|
| QuizStart | Diagnostic begun | — |
| QuizComplete | Results shown | $1.50–4.00 per completion |
| Lead | Email captured | $4–10 |
| JoinCommunity | Skool free join / trial | $15–40 |
| Purchase | Paid membership | ≤ 1 month of membership LTV |

Optimize campaigns to QuizComplete until Purchase volume exceeds ~30/month, then move optimization down-funnel. The number that decides whether to scale is **cost per paid member vs. average member lifetime value** — measure LTV from Skool retention data starting now.

## 8. Immediate action items

1. **Add a payment method to the Meta ad account** (`2797032890629290`) — it's active and API-enabled but cannot spend yet.
2. Install Pixel + CAPI on destiny.ac and fire the §7 events.
3. Build the email capture step on the diagnostic results page if it isn't there.
4. Generate the first Higgsfield test batch: 12 variants across the four §3 angles; pressure-test avatar talking-head quality before scaling the pipeline.
5. Connect TikTok/IG/YT accounts in Postiz for the organic repurposing loop.
6. Film one founder credibility video (Gut & Non, the university-study story) for the retargeting layer.
