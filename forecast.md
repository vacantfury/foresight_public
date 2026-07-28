# Forecast — dated probabilistic claims

**What this file is.** The claim layer: `worldview.md` cards argue *mechanisms*, `worldtree.md`
holds the *possible worlds*, and this file asserts *dated, checkable claims* about what will
actually be observed. Every claim cites the cards it rests on and the worldtree node it
discriminates. Claims are never edited after their edition is stamped — they stay scoreable
forever; revisions are new claims in a later edition, so the record stays honest.

**Status: v1 — MVP edition, as-of 2026-07-25.** Scope per design §5 (confirmed same day): slices
1–2 deep, slices 3–5 thin, far tier priors only. **26 claims (F1–F26)** — one above §5's 15–25
band, deliberately, because the first draft left the +3-month rung empty and that rung carries the
edition's fastest feedback (F25 resolves in five weeks). Methodology per design §4 (confirmed same
day, five additions binding). Every anchor number was verified against a fetched primary source;
nothing here is quoted from memory or from a search summary. (F-IDs are assigned in creation
order and are permanent, so F25/F26 sit inside slice 1 rather than at the end — an ID is a
claim's identity for scoring, never its position.)

**Rolling rungs this edition:** +3mo = 2026-10-31 · +6mo = 2027-01-31 · +12mo = 2027-07-31 ·
yearly grain = 2028-12-31.

## How a claim is produced (the mechanism, in order)

1. **Pick a question that a named source will answer on a named date.** Not "will AI progress
   continue" — that can never be scored. The resolution source and threshold come first; the
   interesting-sounding question comes second. Most vague futurism dies at this step, which is
   the point.
2. **Pull the outside view first.** What does the measured trend say, and what do professional
   forecasters or a prediction market already say about this or a neighbouring question? This
   number is the starting point, and it outranks unaided judgment (design §4 addition 1).
3. **Apply the structure.** Which worldview cards bear on it, and which worldtree branch does it
   discriminate? A claim that no world distinguishes is not worth making.
4. **Adjust, and write down why.** Every step away from the anchor is stated in words. This is
   the part that can be wrong in an interesting way — and the part a later reader can audit.
5. **Score it when the date arrives.** Brier score per claim; the calibration table over many
   claims tells us whether "70%" actually happens about 70% of the time. That accumulated
   record — not any individual claim — is what makes this a forecasting system rather than an
   essay.

Note what step 4 is not: there is no machine that computes the future here. The number is a
judgment, disciplined by an anchor, a structure, and a written argument, then punished by a score.
That is what every serious forecasting operation does, including the ones we anchor against.

## The divergence table — where we disagree with the market, and by how much

This is the edition's fastest feedback (design §4 addition 4). A large divergence is a claim to be
proud of or embarrassed by; a table of zeroes would mean we are just copying prices and learning
nothing. Positive = we are more confident than the tracked number.

| Claim | Ours | Tracked | Δ | Source of the tracked number |
| --- | --- | --- | --- | --- |
| F2 GPT-6 released by end-2026 | 0.84 | 0.885 | −0.045 | Polymarket |
| F3 FrontierMath ≥90% before 2027 | 0.80 | 0.845 | −0.045 | Polymarket |
| F4 Chinese company in top-3 models | 0.25 | 0.20 | **+0.05** | Polymarket |
| F6 ARC-AGI grand prize by end-2026 | 0.35 | 0.44 | **−0.09** | Manifold |
| F7 Agent solves 90% of SWE-bench | 0.75 | 0.846 | **−0.10** | Manifold |
| F8 AGI before 2029 | 0.18 | 0.275 | **−0.095** | Manifold |
| F10 >150k tech layoffs in 2026 | 0.92 | 0.853 | **+0.067** | Manifold |
| F11 Job loss "basically fine" by 2028 | 0.55 | 0.611 | −0.061 | Manifold |
| F15 H-1B cap raised for FY2028 | 0.20 | 0.361 | **−0.161** | Manifold |
| F16 China blockades Taiwan by mid-2027 | 0.08 | 0.09 | −0.01 | Swift Centre |
| F18 NVDA −50% with SOX −25% by 2027 | 0.20 | 0.23 | −0.03 | Swift Centre |
| F20 Agentic zero-day in a Tier-1 OS | 0.38 | 0.44 | −0.06 | Swift Centre |
| F25 METR 80% horizon > 10h before Sept | 0.30 | 0.34 | −0.04 | Manifold |
| F26 Arena score ≥1510 by 2026-09-30 | 0.72 | 0.67 | **+0.05** | Polymarket |

Fourteen of 26 claims are mirrored. The pattern is worth noting against ourselves: we are below the
tracked number on eleven of fourteen, which is a systematic scepticism about thin-volume benchmark
and timeline markets. If the scorecard later shows those markets were right and we were low, that
is a correctable bias, and it will show up as over-confidence in the NO direction rather than as
noise.

---

## Slice 1 — AI capability trajectory (deep)

**F1 · METR time horizon, end-2026** — p = **0.55** · resolves 2026-12-31
- *Resolution:* the `p50_horizon_length.estimate` field in METR's published benchmark results
  (`metr.org/assets/benchmark_results_1_1.yaml`). YES iff ≥1 entry has a point estimate > 2400
  minutes with a release date on or before 2026-12-31. Point estimate only. If METR publishes no
  update covering a model released after 2026-04-07, resolves NO.
- *Anchors:* current highest measured p50 = 1044.78 min (~17.4 h), Claude Mythos Preview (early),
  released 2026-04-07, CI [508.9, 3304.3] min. Previous: Claude Opus 4.6, 718.8 min (~12.0 h),
  2026-02-05. METR's published doubling for the 2023-on series: 128.7 days, CI [104.4, 158.0].
  Epoch: frontier training compute 5×/yr since 2020; largest known run Grok 4 ~5e26 FLOP.
- *Mirror:* near-miss only — Manifold runs "METR **80%** time horizon exceeds 10h before
  September" at 0.34, a different statistic, threshold and date. Recorded as the closest tracked
  question; not a true mirror, so F1 stays tagged `unmirrored`.
- *Reasoning:* naive extrapolation says YES easily — 268 days at a 128.7-day doubling is 2.08
  doublings, taking 17.4 h to ~74 h, crossing 40 h around September. Three discounts bring it to
  0.55. **(i)** METR's doubling fit explicitly excludes points above 16 h, and the current SOTA
  point (17.4 h) is itself inside that excluded region — the trend we are extrapolating was fitted
  entirely below the range where a bend would first appear. **(ii)** The CI on the current point
  spans 8.5–55 h; a future estimate near the threshold is close to a coin flip on measurement
  noise alone. **(iii)** Resolution risk is not world risk (§4.3): the claim needs METR to publish
  in time, and the time-horizons page was last updated 2026-05-08. Roughly 10–15 points of the
  discount are about METR's schedule and say nothing about AI.
- *Cards / worlds:* W16, W8 · discriminates **N0**. YES near the 74 h line supports "keeps
  compounding" (prior 0.65); NO *with a measured bend* rather than a publication gap is the
  earliest ceiling evidence anywhere in the tree.
- *Changes if:* a published doubling time lengthening beyond ~6 months in the above-16-hour regime
  cuts this to ~0.25 and moves N0 mass toward the ceiling branches. A METR methodology or cadence
  change moves the claim without moving the world — that would be logged as resolution noise.
- *Known flaw, recorded:* discount (iii) makes this a compound claim. Its successor splits into
  one capability claim conditional on publication and one claim on whether METR publishes. F1
  stands unedited so the score is honest and the improvement is on the record.

**F2 · GPT-6 released by end-2026** — p = **0.84** · resolves 2026-12-31
- *Resolution:* the Polymarket market "Will GPT-6 be released by December 31, 2026?"
  (polymarket.com/event/gpt-6-released-by), as that market resolves. Mirrored exactly so the
  adjudication is not ours to argue.
- *Anchor:* Polymarket YES 0.885, volume $80,774. The companion August-31 market sits at 0.275.
- *Ours vs anchor:* −0.045. Release-date markets systematically under-price naming and slippage
  risk — the resolution turns on OpenAI choosing the label "GPT-6", not on a capability event.
- *Cards / worlds:* W8 · weak evidence on **N0** (release cadence, not capability level).
- *Changes if:* OpenAI signals a naming change (e.g. a non-numeric flagship brand), which would
  make NO likely without any change in the underlying trajectory.

**F3 · FrontierMath ≥90% before 2027** — p = **0.80** · resolves 2026-12-31
- *Resolution:* the Polymarket market "AI model scores ≥90% on FrontierMath Benchmark before
  2027", as it resolves.
- *Anchor:* Polymarket YES 0.845, volume $108,542. Corroborating: Manifold "≥2 FrontierMath open
  problems solved before 2027" at 0.83. Context: Epoch released FrontierMath v2 on 2026-06-12 —
  338 problems, 43 in Tier 4, correcting errors in 42% of v1 problems.
- *Ours vs anchor:* −0.045. The v2 revision is a live source of ambiguity about which set a "90%"
  claim is scored against, and benchmark-saturation markets have run hot.
- *Cards / worlds:* W16, W8 · supports **N0** compounding if YES.
- *Changes if:* Epoch publishes a tier-resolved score table showing Tier 4 well below the rest —
  aggregate saturation would then be masking the part that matters.

**F4 · A Chinese company holds a top-3 AI model at end-2026** — p = **0.25** · resolves 2026-12-31
- *Resolution:* the Polymarket market "Will a Chinese company have one of the top 3 AI models by
  December 31?", as it resolves.
- *Anchor:* Polymarket YES 0.20, volume $10,867.
- *Ours vs anchor:* +0.05, our largest upward divergence. Epoch measures the open-weight lag at 4
  months, and Chinese labs have repeatedly produced step-changes between market re-pricings; thin
  volume here means the price is not strongly informed.
- *Cards / worlds:* W2, W6 · discriminates **N2** (access diffuses vs concentrates).
- *Changes if:* a US export-control tightening that bites within the year would cut this sharply;
  see F5 for the cleaner N2 instrument.

**F5 · Open-vs-closed capability gap widens past 6 months** — p = **0.45** · resolves 2027-07-31
- *Resolution:* Epoch AI's published open-vs-closed Epoch Capabilities Index gap
  (epoch.ai/data-insights/open-closed-eci-gap). YES iff Epoch's stated average time-lag exceeds 6
  months in any update published on or before the resolution date. `unmirrored`.
- *Anchor:* Epoch, as of 2026-05-29: "the most capable open-weight models have lagged frontier
  closed models by an average of four months" since January 2026; average ECI gap 8 points (90% CI
  7–11). This *grew* from Epoch's prior 3-month estimate covering Jan 2023–Oct 2025. Epoch flags
  that its own estimate likely understates the true gap.
- *Reasoning:* the trend is already 3 → 4 months and Epoch says its method is biased low. Against
  that, a single strong open release compresses the gap immediately, and the measure is noisy at
  this resolution. Slightly below even.
- *Cards / worlds:* W2 crux, W6 · this is the **cleanest N2 instrument in the edition** — N2's
  prior is 0.67 toward concentration, and a widening gap is exactly what concentration looks like
  before licensing formalises it.
- *Changes if:* a frontier-parity open-weight release drops the gap below 2 months, which would
  move N2 mass toward "diffuses" and re-weight WT4 upward.

**F6 · ARC-AGI grand prize claimed by end-2026** — p = **0.35** · resolves 2026-12-31
- *Resolution:* the Manifold market "Will the ARC-AGI grand prize be claimed by end of 2026?", as
  it resolves.
- *Anchor:* Manifold 0.44, volume $10,869, 52 bettors.
- *Ours vs anchor:* −0.09. The grand prize carries efficiency and open-sourcing conditions that
  raw capability does not satisfy; prize-claim markets have historically run ahead of prize rules.
- *Cards / worlds:* W16 · **N0**, secondary.
- *Changes if:* the prize rules are relaxed, which would make this a capability claim rather than
  a compliance claim.

**F7 · An autonomous agent resolves 90% of SWE-bench** — p = **0.75** · resolves 2026-12-31
- *Resolution:* the Manifold market "Will an autonomous agent resolve 90% of tasks on SWE-bench by
  2027?", as it resolves.
- *Anchor:* Manifold 0.846, volume $857, 17 bettors — thin. Related: "Claude Sonnet 5 exceeds 85%
  on SWE-bench verified" at 0.945.
- *Ours vs anchor:* −0.10. Seventeen bettors is barely a price, and SWE-bench contamination
  concerns mean a reported 90% may be disputed at resolution.
- *Cards / worlds:* W8 · **N0**. Directly relevant to slice 2: SWE-bench is the closest public
  proxy for the automatable core of applied-scientist and senior-SWE work.
- *Changes if:* the benchmark is retired or replaced, which resolves it on a technicality.

**F8 · AGI before 2029** — p = **0.18** · resolves 2029-03-01
- *Resolution:* the Manifold market "Will we get AGI before 2029?", as it resolves.
- *Anchor:* Manifold 0.275, volume $99,456, 271 bettors. Companion "AGI before 2028" at 0.136
  (volume $160,882, 315 bettors). Independent: Metaculus community date for the first publicly
  announced general AI system is **Dec 2032** (1.9k forecasters, 90% interval Feb 2029 – Jul 2041),
  via the ForecastBench mirror. Polymarket "OpenAI announces AGI before 2027" at 0.105; Kalshi's
  equivalent last traded at $0.11.
- *Ours vs anchor:* −0.095, and this is our most considered disagreement. Metaculus's much larger
  panel puts the *median* at 2032 with only the tail edge reaching 2029; Manifold's AGI markets
  resolve on contested definitions and attract definitional optimism. Weighting the deeper panel
  more heavily gives ~0.18.
- *Cards / worlds:* W16, W1 · **N0**, far-tier-relevant.
- *Changes if:* Metaculus's community date moves inside 2030, which would mean the deep panel and
  the market have converged and our discount is unjustified.

**F25 · METR 80% time horizon exceeds 10h before September** — p = **0.30** · resolves 2026-08-31
- *Resolution:* the Manifold market "METR 80% time horizon exceeds 10h before September", as it
  resolves. This is the **+3-month rung's fastest claim — five weeks to resolution.**
- *Anchor:* Manifold 0.34. Note this is the **80%** horizon, a much stricter statistic than F1's
  50% horizon: the 80% figure runs far below the 50% figure for the same model, so a 10-hour 80%
  horizon is a considerably harder bar than F1's 40-hour 50% horizon despite the smaller number.
- *Ours vs anchor:* −0.04. Same publication-timing risk as F1 — METR must publish inside five
  weeks — and the last results file update was 2026-05-08.
- *Cards / worlds:* W16, W8 · **N0**. Deliberately included so F1's family is mirrored and so the
  driver question gets a scored data point in 2026 rather than only at year end.
- *Changes if:* METR publishes early with a long-horizon model, which resolves this almost
  immediately in either direction — the point of a five-week claim.

**F26 · Chatbot Arena score of 1510 by 2026-09-30** — p = **0.72** · resolves 2026-09-30
- *Resolution:* the Polymarket market "Will any AI model reach 1510 Overall (Chatbot) Arena Score
  by September 30, 2026?", as it resolves.
- *Anchor:* Polymarket 0.67, volume $60,234. Companion market for ≥1550 by 2026-12-31 sits at
  0.255.
- *Ours vs anchor:* +0.05. Arena scores move in steps at each frontier release, and the gap
  between the 1510 and 1550 markets implies the market expects roughly one step in this window —
  which is the base rate for a two-month period in the current release cadence.
- *Cards / worlds:* W8 · **N0**, weakly — Arena is a preference benchmark and a poor proxy for the
  agentic capability that N0 actually turns on. Included for rung coverage and speed, and its
  limited diagnostic value is recorded here rather than overstated.
- *Changes if:* Arena changes its scoring normalisation, a recurring event that would move the
  number without moving capability.

---

## Slice 2 — Knowledge-work labor market (deep)

**F9 · Early-career exposure gap persists** — p = **0.72** · resolves 2027-01-31
- *Resolution:* Stanford Digital Economy Lab's Canaries Dashboard
  (digitaleconomy.stanford.edu/project/indicators/canaries-dashboard/). YES iff the dashboard, in
  its most recent monthly update on or before the resolution date, still shows past-year
  employment for early-career (22–25) workers in the most-exposed occupations contracting at ≥3.0%
  per year for at least one gender split. `unmirrored`.
- *Anchor:* dashboard as of 2026-07-22 — most-exposed occupations, past year: contracting 5.4%
  (women) and 3.1% (men). Least-exposed, same age band: growing 1.3% (women) and 2.7% (men). The
  underlying paper's separate headline is a 16% cumulative relative decline for ages 22–25 through
  Oct 2025 (13% through Jul 2025) — a different framing; this claim uses the dashboard's
  annualised rates and says so (§4.3, cite the vintage).
- *Reasoning:* the effect has persisted and strengthened across three published vintages, and the
  most-exposed/least-exposed divergence is the part that is hard to explain by interest rates or
  the general cycle. Against: 3.0% is close enough to the men's 3.1% reading that one soft month
  flips half the test, and Stanford could revise its methodology.
- *Cards / worlds:* W2, W8 · **N3-adjacent** — cognitive-labor substitution without embodiment is
  the WT5 (Economic Squeeze) signature.
- *Changes if:* the dashboard's least-exposed cohort starts contracting too, which would reframe
  the whole effect as macro rather than AI-specific and cut this claim's decision relevance.

**F10 · More than 150k tech layoffs in 2026** — p = **0.92** · resolves per market (2027-05-09)
- *Resolution:* the Manifold market "Will more than 150k tech layoffs occur in 2026?", as it
  resolves.
- *Anchor:* Manifold 0.853. Measured: roughly 120,000 tech roles cut in 2026 as of 2026-07-06, per
  TechCrunch reporting Layoffs.fyi's count (layoffs.fyi itself is JavaScript-rendered and was not
  directly readable — vintage recorded per §4.3). Named 2026 AI-cited cuts in the same piece:
  Amazon 16,000, Oracle 21,000 over twelve months, Meta 8,000, Dell ~11,000, Microsoft 4,800,
  PayPal 4,500+.
- *Ours vs anchor:* +0.067, on arithmetic rather than judgment. 120k in roughly six months is a
  ~20k/month run-rate; 150k needs only ~30k more across the remaining half-year. The market looks
  like it has not updated on the mid-year print.
- *Cards / worlds:* W2 · slice-2 severity, not a tree discriminator.
- *Changes if:* the Layoffs.fyi methodology changes, or the market's resolution source differs
  from Layoffs.fyi — a resolution-source risk we cannot fully see from outside.

**F11 · Job loss "basically fine" through 2028** — p = **0.55** · resolves 2028-12-01
- *Resolution:* the Manifold market "Will things basically be fine regarding job loss and
  unemployment due to AI?", as it resolves.
- *Anchor:* Manifold 0.611.
- *Ours vs anchor:* −0.061. F9's divergence is real and concentrated exactly where "basically
  fine" is measured loosely — aggregate unemployment can look fine while the entry-level rung of
  one occupation is removed.
- *Cards / worlds:* W2, W7 · end-2028 rung; weak **N3** signal.
- *Changes if:* a resolution criterion is published that keys on aggregate unemployment only, in
  which case our reasoning does not bear on the claim and the number should move to the market's.

**F12 · A large employer attributes ≥5,000 cuts to AI** — p = **0.80** · resolves 2027-07-31
- *Resolution:* an official company statement, SEC filing, or earnings call by a Fortune-100
  company explicitly attributing ≥5,000 job reductions to AI or automation, reported by at least
  two independent outlets. `unmirrored`.
- *Anchor:* 2026 already has several near-misses at or above this scale with AI cited in reporting
  (Oracle 21,000; Amazon 16,000; Meta 8,000; Dell ~11,000) — but *explicit official attribution*
  is a higher bar than press attribution, which is what makes this claim non-trivial.
- *Cards / worlds:* W2 · the observable that converts a diffuse labor trend into a legible public
  event; matters because legibility drives the regulatory response in slice 5.
- *Changes if:* legal counsel norms shift against attributing layoffs to AI (age/discrimination
  exposure), which would suppress the observable without changing the underlying fact.

**F13 · Junior-senior divergence still visible** — p = **0.70** · resolves 2027-07-31
- *Resolution:* the Canaries Dashboard's most recent update on or before the date shows
  most-exposed early-career employment contracting while least-exposed early-career employment
  grows, for at least one gender split. `unmirrored`.
- *Anchor:* as of 2026-07-22 this holds for both splits (most-exposed −5.4%/−3.1%; least-exposed
  +1.3%/+2.7%).
- *Reasoning:* twelve months is long enough for the labour market to re-sort, and the effect is
  now three vintages old. Lower than F9 because the two-sided test is harder than the one-sided.
- *Cards / worlds:* W2, W8 · **WT5 signature**.
- *Changes if:* Stanford discontinues the dashboard, which resolves NO on availability rather than
  on the world — the same flaw as F1(iii), and worth pre-empting in the next edition.

---

## Slice 3 — Immigration & US–China climate (thin)

**F14 · EB-2 China advances past 2022-01-01** — p = **0.35** · resolves 2027-01-31
- *Resolution:* the State Department Visa Bulletin for January 2027 (travel.state.gov). YES iff
  the EB-2 China final action date is on or after 2022-01-01. `unmirrored`.
- *Anchor:* August 2026 bulletin — EB-2 China final action date 2021-09-01; EB-3 China 2022-01-01;
  EB-2 India unavailable; all other countries EB-3 2024-09-01. (travel.state.gov returned 403 to
  automated fetch; figures verified identical across two independent immigration-law firm
  summaries quoting the bulletin — vintage and sourcing recorded per §4.3.)
- *Reasoning:* four months of advancement needed in five bulletins. Recent movement has been
  modest and EB-2 India is already unavailable, which signals demand pressure across the category.
- *Cards / worlds:* slice-3 policy drift; no tree node.
- *Changes if:* a visa-bulletin retrogression, or an annual-limit change, either of which
  dominates the trend.

**F15 · H-1B cap raised above 85,000 for FY2028** — p = **0.20** · resolves 2028-01-01
- *Resolution:* the Manifold market "Will the H1B visa cap be raised (above 85000) for fiscal year
  2028?", as it resolves.
- *Anchor:* Manifold 0.361. The FY2027 companion sits at 0.159.
- *Ours vs anchor:* **−0.161, our largest divergence in the edition.** The cap is statutory: raising
  it requires an act of Congress, which has not happened since 2004 despite repeated attempts, and
  the current policy direction is restrictive rather than expansionary (the $100,000 H-1B fee
  proclamation was litigated through 2026, vacated 2026-06-08, stayed 2026-06-12, and the First
  Circuit declined to pause the vacatur on 2026-07-25). Thin markets price legislative action far
  too high as a rule.
- *Cards / worlds:* slice-3; no tree node.
- *Changes if:* a bipartisan high-skilled immigration bill reaches a floor vote, which would be the
  first real signal in two decades.

**F16 · China blockades or quarantines Taiwan by mid-2027** — p = **0.08** · resolves 2027-07-01
- *Resolution:* the Swift Centre published forecast question "Will China blockade Taiwan by
  mid-2027?" (swiftcentre.org/publicforecasts/china-taiwan-and-tsmc-risks-to-2027), as that
  question resolves.
- *Anchor:* Swift Centre 0.09 (professional panel, range 4.9–15%). Corroborating: Metaculus
  community 0.04 for a blockade before Sept 2026 (via ForecastBench mirror); INFER 0.169 for
  Chinese military exercises within 24nm of Taiwan in a six-month window — a much lower bar.
  Swift Centre also puts a TSMC fab being destroyed or inoperable ≥90 days at 3.7% baseline, rising
  to 59% conditional on a blockade.
- *Ours vs anchor:* −0.01, effectively agreement. Recorded deliberately: our worldtree gives N1
  ("race detonates") a 0.10 conditional over a much longer window, so an 8% blockade probability
  over one year is coherent with the tree rather than an independent judgment.
- *Cards / worlds:* W3, W5 · discriminates **N1** — the only claim in this edition that touches the
  catastrophe branch, which is why the conditional TSMC number matters more than the headline.
- *Changes if:* the conditional TSMC-destruction number moves, since WT3's severity, not its
  probability, is what drives the personal layer.

---

## Slice 4 — Financial / economic (thin)

**F17 · A hyperscaler guides 2027 capex below 2026** — p = **0.22** · resolves 2027-01-31
- *Resolution:* public guidance from Microsoft, Alphabet, Amazon or Meta, in an earnings release
  or call on or before the date, indicating planned 2027 capital expenditure below its 2026 level.
  `unmirrored`.
- *Anchor:* 2026 aggregate guidance across the four is roughly $725B, up ~77% from ~$410B in 2025
  (Amazon ~$200B; Alphabet $175–185B; Meta $115–135B; Microsoft tracking toward $190B) — a rolled-up
  2026 estimate rather than a single-quarter disclosure, recorded per §4.3. NVIDIA Q1 FY2027
  revenue $81.6B total, $75.2B data center, up 92% year over year.
- *Reasoning:* the demand signal is still accelerating and capex guidance is sticky downward
  because it is a competitive commitment as much as a financial one. The first cut, when it comes,
  is the loudest available bubble signal — which is why the claim is worth making at a low number.
- *Cards / worlds:* W2, slice-4 · feeds the WT-independent robustness question in the personal
  layer.
- *Changes if:* a major model release visibly fails to move revenue, which is the mechanism that
  would turn capex from a race commitment into a discretionary line.

**F18 · NVIDIA −50% from peak with SOX −25%** — p = **0.20** · resolves 2027-12-31
- *Resolution:* the Swift Centre question "NVIDIA (NVDA) falls 50% from peak while SOX drops 25%",
  as it resolves.
- *Anchor:* Swift Centre 0.23.
- *Ours vs anchor:* −0.03, near agreement. The joint condition is what keeps this low — a single-name
  drawdown is far likelier than a sector-wide one.
- *Cards / worlds:* slice-4 · the concrete form of the AI-capex-cycle risk.
- *Changes if:* F17 resolves YES, which would raise this materially — the two are the same
  underlying event observed at different points in the chain.

**F19 · Magnificent Seven exceed 38% of the S&P 500** — p = **0.40** · resolves 2027-07-31
- *Resolution:* a published index-weight figure from a major provider or a reputable financial
  outlet showing the seven above 38% of S&P 500 market capitalisation at any point on or before
  the date. `unmirrored` — and deliberately soft-edged, which is a weakness recorded here rather
  than hidden.
- *Anchor:* ~34% as reported 2026-07-08 (Forbes), against 21.6% in 2022 and 12.4% eight years
  prior; the group first passed 30% in 2023.
- *Reasoning:* the trend is strongly upward but 4 points in twelve months is roughly a doubling of
  the recent annual rate.
- *Cards / worlds:* slice-4 · concentration is the transmission channel from an AI correction to
  personal savings.
- *Changes if:* the resolution source proves too vague to adjudicate — in which case this claim
  should be voided rather than scored, and rewritten against a named index provider.

---

## Slice 5 — Regulation & societal response (thin)

**F20 · Agentic zero-day in a Tier-1 OS** — p = **0.38** · resolves 2027-12-31
- *Resolution:* the Swift Centre question on a frontier AI agent autonomously discovering and
  exploiting a previously unknown vulnerability in a Tier-1 operating system on a real-world
  device without human intervention, as it resolves.
- *Anchor:* Swift Centre 0.44 (individual forecasts 20–63%).
- *Ours vs anchor:* −0.06. "Without human intervention" and "real-world device" are strict, and
  most publicised agentic-security results to date have a human in the loop somewhere.
- *Cards / worlds:* W5, W11 · this is the edition's sharpest **AI-security** claim; the personal
  layer carries why this slice matters more than its claim count suggests.
- *Changes if:* a lab publishes an end-to-end autonomous exploitation result on a hardened target,
  which would make this near-certain rather than a coin flip.

**F21 · Federal preemption of state AI law enacted** — p = **0.15** · resolves 2027-07-31
- *Resolution:* an act of Congress signed into law on or before the date that preempts state AI
  regulation in whole or in substantial part. `unmirrored`.
- *Anchor:* Executive Order 14365 (2025-12-11) directs a DOJ AI Litigation Task Force, conditions
  BEAD broadband funding on states dropping conflicting AI laws, and tasks preparation of uniform
  federal preemption legislation. EO 14409 (2026-06-02) explicitly disclaims any mandatory federal
  licensing regime. Meanwhile the state layer is live: California SB 53 in force since 2026-01-01,
  Texas TRAIGA since 2026-01-01, Colorado SB26-189 effective 2027-01-01.
- *Reasoning:* the executive intent is documented and unusually explicit, but preemption is
  legislation, and the same Congress has passed no comprehensive AI statute. Executive action
  substitutes for, rather than accelerates, the legislative path.
- *Cards / worlds:* W6, W11 · bears on **N4** — whether the enforcement layer is nationally
  standardised is upstream of whether refusal capability survives procurement.
- *Changes if:* a preemption provision is attached to a must-pass vehicle, which is how this would
  actually happen if it does.

**F22 · EU further delays or narrows GPAI obligations** — p = **0.30** · resolves 2027-07-31
- *Resolution:* an adopted EU legal act on or before the date that postpones or materially narrows
  the general-purpose AI obligations in force since 2025-08-02. `unmirrored`.
- *Anchor:* the Digital Omnibus on AI completed its passage on 2026-06-16 (Parliament plenary,
  423–57–174), moving Annex III high-risk obligations to 2027-12-02 and Annex I to 2028-08-02, and
  postponing AI-content marking to 2026-12-02 for systems placed before 2026-08-02. **GPAI
  obligations were not deferred** and remain on their original schedule.
- *Reasoning:* the Commission has just demonstrated both willingness and a working mechanism for
  deferral, and industry pressure has not abated — but GPAI was pointedly excluded from the package
  that just passed, which is evidence it is being protected rather than queued.
- *Cards / worlds:* W6 · **N2** — licensing and access regimes are where concentration becomes law.
- *Changes if:* a second omnibus is tabled naming GPAI, which would move this above 0.6 immediately.

---

## Far tier (2032–2040) — order-of-magnitude priors only

Per design §5 the far tier gets no new claims this edition beyond the two structural priors. These
are the worldtree's numbers restated as scoreable-in-principle claims; they are **`unanchored —
judgment only`** and carry the widest bands in the file.

**F23 · W12 polarity trichotomy, 2032–2040** — resolve-to-one-pole **0.22** · frozen standoff
(seki) **0.45** · fragmentation into more than two poles **0.33**
- *Resolution:* judgment against a written rubric at the 2032 edition; not scoreable before then.
- *Reasoning:* restates worldtree node N5 (0.33 / 0.67 conditional on reaching it) redistributed
  to include the fragmentation branch the tree prunes. The tree's own numbers are pre-anchoring
  priors and W7's standing warning applies: coherence is not calibration.
- *Cards / worlds:* W12 · **N5** · WT7 / WT8.

**F24 · W7 locked-in-slide mass** — p = **0.35** that by 2040 the world is in a state where an
ordinary individual's economic and political leverage is structurally irrecoverable by individual
action
- *Resolution:* judgment against a written rubric at the 2035 and 2040 editions.
- *Reasoning:* the sum of WT7 (0.065) and WT8 (0.13) is 0.195 of *fully* locked worlds; this claim
  is deliberately broader, adding partial-lock mass from WT5 (Economic Squeeze, 0.13). It is the
  crux-claim required by §4.2 for the `contested` card W7, and it is the single number in this file
  that most drives the personal layer's irreversible decisions.
- *Cards / worlds:* **W7 crux** · WT5, WT7, WT8.

---

## Scorecard

No claims have resolved. Resolution calendar: **2026-08-31 (F25)** · 2026-09-30 (F26) ·
2026-12-31 (F1, F2, F3, F4, F6, F7) · 2027-01-31 (F14, F17) · 2027-07-01 (F16) · 2027-07-31 (F5,
F12, F13, F19, F21, F22) · 2027-12-31 (F18, F20) · 2028-01-01 (F15) · 2028-12-01 (F11) ·
2029-03-01 (F8) · F10 per its market (2027-05-09). F23/F24 are far-tier and not scoreable this
decade. The scorecard table and calibration curve are born at the first revision, per design §1;
`scoringrules` or Fatebook adoption is deferred until the manual version shows pain (design §6).

| Edition | Claims | Resolved | Brier | Notes |
| --- | --- | --- | --- | --- |
| v1 (2026-07-25) | 26 | 0 | — | MVP edition; 14 mirrored, 10 unmirrored, 2 unanchored |

## Known weaknesses of this edition, recorded before scoring

1. **Eleven of fourteen mirrored claims sit below the tracked number.** If that pattern is wrong it
   will show as a systematic NO-direction bias, not as noise. Watch it at the first revision.
   Mechanically this is one judgment applied fourteen times (thin markets over-price), so it should
   be treated as roughly one bet, not fourteen independent ones — the scorecard will overstate the
   evidence either way.
2. **Three claims can resolve NO because a publisher went quiet** (F1, F9, F13) rather than because
   the world moved. The successors split publication risk from world risk.
3. **F19's resolution source is too soft** to adjudicate cleanly and should be rewritten against a
   named index provider, or voided rather than scored.
4. **Slice 3 is thin and unmirrored** because no tracked market covers visa-bulletin movement. If
   slice-3 claims matter more than their count suggests, a Manifold question could be created
   rather than found — an option worth weighing at the next edition.
5. **Far-tier claims are not scoreable this decade**, so they contribute nothing to calibration
   while carrying the most decision weight. This asymmetry is inherent, not a defect to fix, but it
   means calibration earned on near-tier claims should not be assumed to transfer to F23/F24.

## Access and verification notes

Metaculus is blocked directly (Cloudflare on the site, authentication required on the API); its
community numbers reach this file through the **ForecastBench public GitHub mirror**, refreshed
roughly bi-weekly. Swift Centre, Manifold, Polymarket and Kalshi's API read without authentication.
BLS, USCIS and travel.state.gov all return 403 to automated fetching, so figures from those sources
are marked with their secondary sourcing above. The verified access table lives in
`knowledge/forecasting_platforms/summary.md` and is re-tested each revision.

During this edition's anchor pull a web search produced confident, specific, entirely fabricated
Metaculus percentages attributed to a real page that does not contain them, and one agent's summary
mislabelled METR's units before a second pass caught it against the raw file. Every number in this
file was read from a fetched primary source. That discipline is not optional — a forecast built on
invented anchors would score exactly as well as a real one for years before the error surfaced.
