# Quiz Funnel — Build Spec

Everything required to run paid traffic into the destiny.ac diagnostic and convert it to
$37/mo Skool members. Items marked ✅ already exist; ⬜ must be built/configured.

## 1. Meta account plumbing (blockers — nothing spends without these)
- ⬜ Payment method on ad account `2797032890629290` (active + API-enabled, cannot spend yet)
- ⬜ Verify destiny.ac as a domain in Meta Business Manager
- ⬜ Create **two** pixels/datasets: one for destiny.ac, one for the Skool group (never share one ID across domains)
- ⬜ Page + Instagram account connected to the ad account; Advantage+ placements enabled

## 2. Landing experience
- ✅ Free 2-minute diagnostic, no signup (Taksa + Behavioral Feng Shui)
- ⬜ Ad-specific entry points (or URL params that swap the headline) so the page headline
  matches the ad angle — weekday ads land on weekday framing, home ads on home framing.
  Message-match is the single biggest quiz-funnel CVR lever.
- ⬜ Mobile load < 2.5s (90%+ of this traffic is mobile in-app browser); test in the
  Instagram in-app browser specifically
- ⬜ Progress indicator on the quiz (completion rates drop hard without one)

## 3. Tracking & events (destiny.ac)
- ⬜ Meta Pixel installed site-wide + **Conversions API** server-side, deduplicated via
  shared `event_id` (browser-only tracking loses ~20–30% of events to iOS/ad-blockers)
- ⬜ Event ladder, fired from the quiz app:
  | Event | Type | Fires when |
  |---|---|---|
  | `PageView` | standard | every page |
  | `QuizStart` | custom | first question answered |
  | `QuizComplete` | custom | results rendered |
  | `Lead` | standard | email submitted on results page |
- ⬜ UTM convention on every ad: `utm_source=meta&utm_campaign=[angle]&utm_content=[ad-name]`
  persisted through the quiz into the ESP record and the Skool join link
- ⬜ Skool group: install Skool's Meta pixel plugin (the second pixel) — gives trial-start
  and purchase events natively

## 4. Results page (the conversion moment)
- ⬜ Personalized result headline (their weekday/profile by name — this is what gets screenshotted and shared)
- ⬜ **Partial reveal:** show 2–3 genuine insights free, show the deeper reading as
  visibly locked — the gap is the email's job to close
- ⬜ Email capture: "Get your full reading" (single field, no name required)
- ⬜ Post-email CTA: Skool "Join free for 7 days" with UTM-tagged link
- ⬜ Share button (results screenshots are free distribution)

## 5. Email (ESP + nurture)
- ⬜ ESP connected to the quiz form (any of ConvertKit/Kit, MailerLite, ActiveCampaign),
  tagging each contact with quiz type + result (weekday) + UTM source
- ⬜ 5-send nurture, all conditional on "not yet a member":
  1. **Day 0** — full reading delivered (the promised asset; highest open rate you'll ever get)
  2. **Day 1** — founder story: the university study, why this isn't mysticism (Gut & Non)
  3. **Day 3** — member story / what the community actually does week to week
  4. **Day 5** — trial invitation: what unlocks in your free week, what unlocks after
  5. **Day 7** — direct ask + honest scarcity (live class calendar date works; fake countdowns don't)
- ⬜ Result-personalized merge fields in subjects ("What Tuesday-borns tend to do under stress")
  — fine in email, where personal-attribute rules don't apply like ads

## 6. Retargeting stack (Meta)
- ⬜ Custom audiences: QuizComplete-not-Lead (7/30d), Lead-not-trial (30d), video viewers
  75% (30d), Skool About-page visitors (via Skool pixel), email list upload
- ⬜ Creative per stage: founder-credibility video → D1 community ad → S3 credibility card
- ⬜ Exclusions: members/purchasers excluded everywhere

## 7. Skool side
- ⬜ 7-day free trial enabled on the $37/mo plan
- ⬜ Drip: free classes day 0, main curriculum day 8+ (post-trial only)
- ⬜ Day-5/6 trial-ending email pointing at the locked curriculum
- ⬜ About page rewritten to mirror ad language (message-match again)

## 8. Legal
- ⬜ Privacy policy covering quiz data + email use; consent checkbox at email capture
- ⬜ Cookie consent if EU traffic is allowed (simpler: geo-limit ads to US/CA/AU/UK initially)
- ⬜ Results framed as insight/education — no health, financial, or relationship outcome claims

## Launch gate
Spend starts only when: payment method ✅, both pixels firing verified in Events Manager ✅,
QuizStart/QuizComplete/Lead visible in test traffic ✅, day-0 email delivering ✅,
trial + drip configured ✅. Everything else can improve in flight.
