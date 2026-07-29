# Worldview — the mechanisms layer

**What this file is.** The project's argument library. Each entry is a **thesis card** — a belief
about how the AI-shaped future works, stated sharply enough to argue with. Cards are the
*reasoning layer* beneath forecasts: the forecast document (when it exists) asserts dated,
probabilistic claims, and each claim cites the thesis cards it leans on by ID (W1, W2, …).
This is also how methodology commitment 3 ("legible reasoning per claim") gets a home: the
argument lives here once, and many claims can point at it.

**Discussion protocol (settled 2026-07-07).**
1. Owner thought-dumps in conversation, raw form — no polish expected, any language.
2. Claude engages in-session: names the concept where established literature exists, steelmans,
   stress-tests, disagrees where warranted.
3. Settled threads are distilled into cards *in the same session* — append or amend, never batch
   to "later." The owner's original intuition is always preserved in the card, even when amended.
4. Card anatomy: **statement · mechanism · strongest counterargument · observables** (what to
   watch that would strengthen or weaken it) **· slices it feeds · personal stakes**. Per the
   shared-private discipline (2026-07-07), owner-specific personal-stakes content lives in the
   local, uncommitted personal layer (`personal/stakes.md`); committed cards carry only generic
   analysis and a pointer.

**Status vocabulary:** `owner-intuition` (stated, not yet stress-tested) · `argued` (survived a
round of counterargument; counterargument recorded) · `contested` (owner and Claude genuinely
disagree; both positions kept until evidence moves one).

---

## W1 — States will capture frontier AI and align it to state interest [argued]

**Owner's original statement (2026-07-07):** advanced models may be controlled by governments,
which may "get rid of alignment and use it as a weapon."

**Mechanism (as amended in discussion):** the capture pathway is real and has precedent
(Manhattan Project, crypto export controls, satellite imagery — every general-purpose strategic
technology got a national-security takeover or chokehold). One amendment: states would not
*remove* alignment — alignment techniques are principal-agnostic. The same methods that align a
model to "helpful and harmless" align it to any principal's objectives. The risk is therefore
**narrow alignment** (AI aligned to one state or faction) rather than de-alignment. This is worse
in a way: a narrowly-aligned system is *more* controllable and *more* usable as an instrument
than a misaligned one.

**Strongest counterargument:** capture by *multiple* states restores a balance-of-power structure
rather than producing a single weaponized hegemon; and capture and public benefit are not
mutually exclusive (the Internet was DARPA-born and still bloomed civilian). The dystopia
requires capture *plus* concentration (see W2's crux).

**Observables:** security-clearance requirements appearing at frontier labs · government compute
contracts and datacenter co-siting with defense infrastructure · export-control escalation
(weights, not just chips) · nationalization proposals moving from essays (Aschenbrenner-style)
into draft policy · classified model versions diverging from public ones.

**Slices:** 1 (state-level AI-race dynamics sub-layer), 5. **Personal stakes:** → local personal
layer.

---

## W2 — AI removes the strong's dependence on the weak; power compounding loses its brakes [argued]

**Owner's original statement (2026-07-07):** power and advantage are usually exponential in time —
the strong become stronger, the weak weaker; if AI is too strong, common people are useless.

**Mechanism (as sharpened in discussion):** the exponential itself is not new — what is new is the
removal of the *brakes*. Historically, compounding power was checked by: (a) **dependence** — the
strong needed the weak as labor, soldiers, taxpayers, consumers, which gave the many implicit
bargaining power (the real foundation beneath democracy, unions, and welfare states); (b)
**mortality and succession** — dynasties break; (c) **coordination threats** — revolt was credible
because the many were load-bearing. AI-substituted labor attacks (a) directly: an owner of AI
labor needs no workers and eventually no consumers of its intermediate output. This is the
rentier-state / resource-curse analogy ("intelligence curse"): states funded by oil don't need
citizens and treat them accordingly; firms and states running on AI labor face the same incentive
gradient. The owner's "common people are useless" is precisely a **bargaining-power collapse**,
which precedes and causes the income collapse — the sequencing matters for timing personal
decisions.

**Strongest counterargument (the crux):** the whole argument assumes **concentration** — exclusive
or compute-gated access to frontier capability. If capability commoditizes (open weights near the
frontier, collapsing inference costs), the weak get the same tools and the exponent flattens.
Whether AI stays compute-moated or diffuses is arguably the single biggest branch variable for
the far tier. *Amended 2026-07-07 (owner's round-2 point, see W6):* diffusion is not merely a
technical/economic variable — it is a policy lever incumbents can and already do gate by license,
so the counterargument only holds where licensing regimes fail or leak.

*Amended 2026-07-07 (owner's round-3 points — the loop closes):* the owner's embodiment and
prediction points complete this card. Of the three historical brakes: cognitive automation
removes (a), economic dependence; **embodied AI removes the enforcer-loyalty constraint that made
(c) credible** (armies defect, robots don't — see W9); and **asymmetric prediction removes the
opacity that made coordination organizable at all** (predicted dissent is preempted dissent — see
W4's amendment). All three brakes fail from the *same* underlying capability driver, which also
weakens any "the cards are independent" comfort.

*Amended 2026-07-07 (round 4 — the fourth brake):* there was an implicit brake (d): **exit**
(Hirschman's exit alongside voice) — emigrate, homestead, hide; the frontier as escape valve.
Planetary legibility removes it (see W10(i)). The brake table is now complete across the cards:
(a) dependence ← automation (this card) · (c) voice/revolt ← embodiment + prediction (W9, W4) ·
(d) exit ← legibility (W10). Brake (b), mortality, is the inverse case: it is being removed *for*
the powerful (longevity — already a tracked far-tier variable), not against the many. *Amended
2026-07-21 (round 8):* the brake-(b) removal now has its own card — W14 argues elite life
extension is the *predictable first purchase* of AI-scale power, not a side effect.

**Observables:** labor share of income · junior-role hiring rates in knowledge work (the canary —
already tracked in slice 2) · gap between frontier and best-open-weights capability (Epoch data) ·
first firm or state function visibly run on majority-AI labor · whether frontier access gets
licensed/gated vs. sold flat-rate.

**Slices:** 2, 4, and the far tier's world-state branching. **Personal stakes:** → local personal
layer. (Generic corollary, worth keeping public: if bargaining power erodes *before* income does,
the high-value window for converting labor into durable capital is early — sequencing, not
level, is the actionable fact.)

---

## W3 — Racing dynamics create preventive-strike incentives [argued]

**Owner's original statement (2026-07-07):** powerful people may think to destroy opponents with
AI, to defend themselves, in a prisoner's dilemma.

**Mechanism (named):** this is the **security dilemma** plus **preventive war**, and the cleanest
formal frame is Fearon's (1995) commitment problem: rational wars happen when a rising power
*cannot credibly promise* not to exploit its future advantage — so the declining side's last
rational moment to act is *before* the rival crosses the threshold. An AI race with a plausible
decisive-strategic-advantage threshold maximizes this commitment problem. This is not fringe
reasoning: it is now explicit doctrine debate — Hendrycks/Schmidt/Wang's "Superintelligence
Strategy" (2025) proposes MAIM (Mutual Assured AI Malfunction), i.e., states deterring rivals'
destabilizing AI projects by credible sabotage. The owner's intuition matches a live strategic
literature.

**Strongest counterargument:** the nuclear precedent. Preventive-war logic against the USSR was
seriously advocated (von Neumann, famously) and never executed; states are empirically more
risk-averse than the clean game theory implies, and sabotage is graduated and deniable — so the
realistic expression is covert friction (cyber operations, supply-chain interference, talent
restrictions), not overt strikes. Frightening, but a different, slower failure mode than "destroy
opponents."

**Observables:** attributed sabotage/cyber incidents against AI infrastructure · datacenter
hardening, siting, and air-defense colocation · doctrine language about rivals' AI programs in
defense documents · US–China talks (or their absence) establishing AI red lines.

**Slices:** 1, 3. **Personal stakes:** → local personal layer. (Generic observation retained:
escalation historically hits foreign nationals in sensitive roles first — talent restrictions are
cheap early moves for a state, so they lead actual conflict as an indicator.)

---

## W4 — Strong prediction reshapes conflict in both directions [contested → argued, amended]

**Owner's original statement (2026-07-07):** if AI can predict the future accurately, everything
is near certain — and that is frightening.

**Mechanism (both directions — this card was genuinely amended in discussion):** prediction's
effect on conflict is not monotone.
- *Destabilizing:* certainty sharpens W3 — if you can see with confidence that a rival overtakes
  you in 18 months, preventive logic strengthens. Deterrence-by-uncertainty (Schelling's "threat
  that leaves something to chance") also erodes.
- *Stabilizing:* in Fearon's frame, wars of **miscalculation** disappear under mutual accurate
  prediction — if both sides can predict the war's outcome, they take the implied bargain without
  paying the deadweight cost of fighting. Further, mutual transparency enables cooperation opaque
  agents cannot reach (program-equilibrium results: "cooperate iff I can verify your strategy
  cooperates") — verification is historically what made arms control work at all.
- *Limits (the physics point):* full certainty is unlikely to be the operating regime. Prediction
  of an adversarial agent is self-undermining — an agent that knows it is predicted randomizes
  (mixed-strategy equilibria exist precisely because predictability is exploitable) — and chaotic
  sensitivity bounds horizon length for any intelligence. The plausible regime is "far better
  calibrated than humans, still probabilistic."

*Amended 2026-07-07 (owner's round-3 challenge — asymmetric prediction):* the "limits" paragraph
above holds **among near-peer predictors, and that is exactly its weakness**. Chaos bounds
trajectory-level prediction of chaotic systems (weather), but the strategically decisive domains —
individual human behavior, aggregate social dynamics, markets, persuasion — are predictable at
the grain that matters, and a world-model breakthrough could push this far beyond current levels
(recommender systems already demonstrate superhuman behavioral prediction at scale, today). And
the mixed-strategy defense requires that the predicted party *knows* it is being predicted and
*can afford* to randomize — protections available to states and sophisticated actors, not to
ordinary people. Between unequal predictors, the stronger extracts value from the weaker's
residual predictability. So the frightening regime is not "the future is certain" but "**you are
certain — to them**": asymmetric prediction as manipulation and preemption power. This feeds
W2 directly (coordination that can be predicted can be preempted — predictive policing of
dissent) and is a sharper form of the owner's original fear than Claude's first amendment
allowed.

**Status note:** the owner's fear stands for the preventive-logic branch; the amendment is that
the same capability also removes an entire class of wars and enables verification-based
cooperation. Net sign is genuinely unresolved — treat as a branch variable, not a doom premise.
The round-3 amendment strengthens the owner's side for the *asymmetric* case (strong predictor
vs. weak predicted); Claude's stabilizing branch survives mainly for the near-peer state-vs-state
case.

**Observables:** forecasting-capability benchmarks (AI vs. superforecaster calibration on
geopolitical questions) · any deployment of AI forecasting inside national-security
establishments · verification tech in AI treaties (compute accounting, training-run attestation).

**Slices:** 1, 3. **Personal stakes (reflexive):** this project's own premise is the middle
regime — the world is predictable enough that forecasting pays, not so predictable that the
scorecard is trivial. If W4's "limits" paragraph is wrong in either direction, the project's
methodology needs revisiting.

---

## W5 — AI sits in the worst quadrant of offense–defense theory [argued]

**Owner's original statement (2026-07-07):** too strong intelligence, too strong offense, too
strong defense are all frightening.

**Mechanism (named):** offense–defense theory (Jervis 1978): the security dilemma's severity
depends on (i) whether offense or defense dominates and (ii) whether offensive and defensive
postures are *distinguishable*. AI is bad on both axes: offense-dominant in cyber and bio (the
attacker needs one hole; the defender must close all), and **indistinguishable** — the identical
model that hardens a network attacks one, so even sincerely defensive AI buildup looks
threatening and feeds the spiral. The owner's "all of it is frightening" is exactly the
indistinguishability point: in Jervis's worst quadrant there is no reassuring posture.

**Strongest counterargument:** defense may win in specific domains — formal verification of
critical code, AI-hardened infrastructure, and evals-based "safety cases" are attempts to make
defensive capability distinguishable. Empirically unresolved; cyber offense/defense data over the
next two years is the test.

**Observables:** ratio of AI-attributed intrusions to AI-attributed prevented intrusions ·
adoption of formally verified components in critical infrastructure · whether capability evals
become treaty-grade distinguishers.

**Slices:** 1, 5. **Personal stakes:** background risk level; no direct personal decision hangs
on W5 yet — it mostly modulates how bad W1/W3 branches get.

---

## W6 — Frontier AI access will be license-gated; licensing amplifies incumbent advantage [argued]

**Owner's original statement (2026-07-07, round 2):** the weak cannot get equal AI access. The
future world will be more ruled by license — governors will use their licensing power to amplify
their advantage, and the AI-leading country will use it to amplify its lead over other countries.
The future world will be full of licenses.

**Mechanism:** this is not a prediction; it is already drafted policy. The US AI Diffusion Rule
(Jan 2025 — rescinded May 2025 in favor of bilateral deals, but the instrument survives) created
a literal three-tier global *license* system for AI compute. "Structured access" (Shevlane 2022)
is the academic name for gating capability behind permission layers instead of open release — and
it is the *safety community's own preferred tool*. That is the sharp edge of this card: safety
licensing and hegemonic gatekeeping use identical instruments and are indistinguishable from the
outside (the same structure as W5's indistinguishability problem). Between states: export
controls climbing the stack — chips → training compute → model weights → cloud access. Within
states: KYC'd API access, tiered capability release, compute thresholds triggering licensure
(EU AI Act GPAI thresholds as the seed), clearance-gated roles. And the economics of licensure
(Stigler's regulatory capture; India's License Raj as the historical saturation case) says such
regimes drift toward incumbent protection regardless of founding intent — the license's stated
purpose and its distributional effect come apart within a generation.

**The two-layer physics of licensability (refines W2's crux):** weights are *information* — they
leak like 1990s cryptography, where US export controls failed totally (the crypto wars).
Training and large-scale inference compute is *physical* — it chokes like fissile material, where
licensing (NPT) largely held. AI has both layers, so the license regime's real strength reduces
to one variable: **does the frontier stay compute-hungry?** If yes, the physical layer stays
governable and W6 bites hard. If algorithmic efficiency keeps letting yesterday's frontier run on
commodity hardware, the world stays *de jure* licensed but *de facto* leaky.

**Strongest counterargument:** license regimes need near-monopoly on the supply chain plus
jurisdictional reach. Open weights have trailed the frontier by only ~6–18 months so far;
jurisdictional competition (Gulf compute, China's domestic chip stack) erodes any one licensor's
bite; and the crypto-wars precedent shows pure-information controls fail against motivated
diffusion. A world "full of license" may therefore be a world full of *porous* license — real
friction for ordinary actors (which still hurts the weak most, partially conceding the owner's
point), weak against determined states.

**Observables:** whether model weights get formally classified as export-controlled technology ·
citizenship/clearance requirements appearing in frontier-lab and government AI job postings ·
compute-threshold licensing hardening in US/EU law · KYC requirements for cloud compute ·
frontier-vs-best-open-weights gap (shared observable with W2) · bilateral compute deals replacing
multilateral rules.

**Slices:** 1, 3 (directly), 5. **Personal stakes:** → local personal layer. (Generic
second-order point retained, feeds slice 2: licensing also shapes *who gets displaced* —
guild-licensed professions (medicine, law) can legally slow AI substitution of themselves;
applied science and software have no guild license and no such moat.)

---

## W7 — The slide is gradual, not explosive — and it feels like destiny [contested]

**Owner's original statement (2026-07-07, closing the first dump):** the future seems very
desperate; not bursting like the two world wars, but the world seems to have an inevitable
destiny.

**Steelman (the coherent version of the fear):** W1–W6 compose into a single slow slide — state
capture (W1) + dependence-removal (W2) + racing friction (W3) + worst-quadrant security dilemma
(W5) + license enforcement (W6) — all pushing one direction with no single cataclysm required.
This matches the **gradual disempowerment** literature (disempowerment "without a bang"): each
step is locally rational for someone, so there is never a discrete moment to rally resistance
around. The *absence* of a burst is precisely what makes it feel inevitable — nothing to prevent,
so nothing prevents it.

**Claude's contest (recorded; owner has not conceded):**

- *Equilibrium multiplicity.* The doom states are equilibria, not unique solutions. In
  coordination games, *beliefs select the equilibrium* — which makes declared inevitability not a
  neutral observation but a move that helps select the bad branch. "Destiny" is a category error
  for a system whose solution concept is a set.
- *Gradient vs. trajectory.* The structural read of US–Soviet dynamics said nuclear war was
  near-inevitable — von Neumann, who invented the theory being used, advocated preventive war on
  exactly these grounds ("why not bomb them today?"). The structure was real; the destiny never
  arrived. What intervened was not luck but mechanisms: verification, arms control, iterated play
  lengthening the shadow of the future, individual vetoes (Arkhipov, Petrov). Game-theoretic
  predictions are hypersensitive to the game's specification — payoffs, information, commitment
  technology — and the specification is a *design variable* (Schelling's whole program). The game
  is not handed down; it gets rebuilt mid-play.
- *Conjunction discipline.* "Desperate" reads every card at its worst branch simultaneously. The
  cards are partly independent; the all-worst-branches conjunction is not the modal world. The
  modal world is mixed — some licensing, partial diffusion, covert friction rather than open war,
  major displacement with messy partial responses — bad-ish and navigable. Replacing this mood
  with multiplied probabilities is literally what forecast.md is for.
- *Slow crises are the tractable kind.* The owner's own observation ("not bursting") cuts against
  him: slow means visible, feedback-rich, and correctable — the regime where foresight and early
  positioning pay most, at both civilizational and personal scale.

**Resolution path:** the disagreement reduces to a quantity, not an argument — how much
probability mass the far tier (2032–2040) puts on *locked-in-slide* world-states versus mixed or
corrected ones. That is a forecast.md number. This card closes the first thought-dump by handing
its question to the forecast document.

**Observables:** nothing unique — W7 resolves through W1–W6's observables, plus one of its own:
whether institutional counter-moves with teeth emerge (AI treaties with verification, compute
governance, labor-share policy responses). Their emergence is direct evidence against lock-in;
a decade of their absence is evidence for the owner's position.

**Round-3 update (2026-07-07):** the owner's additions (W8 pace mismatch, W9 embodiment, W4's
asymmetric-prediction amendment) weaken two of the four contest arguments: *gradient vs.
trajectory* (trajectory-bending mechanisms need time the pace mismatch may not grant) and
*conjunction discipline* (the new variables share one underlying capability driver, so the cards
are more correlated than first claimed). The contest narrows to **equilibrium multiplicity** and
the **personal-agency corollary**. Claude moved probability mass toward the owner's position and
still contests "inevitable." The resolving quantity (far-tier probability on locked-in-slide
world-states) is unchanged — it just got a higher prior.

**Round-7 posterior note (2026-07-07, Claude — gut numbers, pre-methodology, to be anchored in
forecast.md):** asked directly by the owner whether the future is doom after rounds 3–7. Answer
recorded: *doom decomposes*. Extinction-class doom: unmoved, low, the owner's cards never argued
it. **Domination-class doom (locked-in W11 benevolence regime in ≥1 pole by ~2040): moved from
~15–20% at session start to ~30%** — conditional on the capability driver compounding as the
cards assume. Mixed/muddle worlds (incl. seki) ~50%; hot catastrophe ~10%; broad-rescue worlds
~10%. Unconditionally, discount the whole stack by P(driver sustains) ≈ 0.6–0.7. **Largest
unpriced variable: the driver premise itself** — every card conditions on capabilities continuing
to compound, and no round has stress-tested that premise (flagged as the next dump candidate).
Standing warning: seven rounds of one intelligent pessimist plus one engaged interlocutor is
exactly the process that produces *coherent* correlated structure — coherence is not calibration;
the outside-view anchoring pass is mandatory before these numbers harden.

**Round-8 note (2026-07-21):** the flagged driver-premise stress test has begun — W16 structures
the plateau branch (ceiling-height trichotomy, diffusion-vs-lock-in race, resource reversion).
The conceptual branching is now carded; the *empirical* anchoring of P(driver sustains) — scaling
economics, data walls, capability-gap trend data — still belongs to the forecast.md
outside-view pass.

**Slices:** far tier, all slices. **Personal stakes:** fatalism is strategically corrosive at the
personal scale regardless of the global answer — every playbook entry pays off better under early
action than under despair, *in every branch including the bad ones*. The posture the cards
actually support is not "nothing matters" but "position early, watch the tripwires."

---

## W8 — The pace mismatch: capability outruns institutional adaptation [argued]

**Owner's original statement (2026-07-07, round 3):** newer, stronger models are appearing very
quickly — a direct correction to Claude's W7 contest, which leaned on institutions bending
trajectories.

**Mechanism:** every trajectory-bending mechanism in the nuclear precedent took decades against a
slow-moving, state-monopolized technology — 18 years from Hiroshima to the Limited Test Ban,
25+ to real verification — and the negotiated object (warheads, delivery systems) held still
while being negotiated over. AI capability generations turn over in months, are privately held,
and the object of governance mutates faster than treaties can specify it; verification requires
the verified thing to sit still long enough to define. If institutional latency exceeds
capability doubling time, "the game can be redesigned mid-play" loses its operative window: the
game changes faster than it can be redesigned. This is the strongest single objection to W7's
contest.

**Counterargument (three speed-ups on the governance side):** (1) this cycle's institutional
response is historically anomalous in speed — EU AI Act within ~2 years of GPT-4, US export
controls within months, safety institutes within a year (shallow, but fast); (2) institutions can
regulate *inputs* — compute, capital, energy — which move on infrastructure timescales even when
capability moves on software timescales; (3) the capability curve can be pointed at governance
itself (AI-assisted verification, monitoring, treaty design) — the only mechanism that truly
re-matches the speeds, and therefore a first-class thing to watch for.

**Observables:** cadence of frontier releases vs. median time from rule proposal to enforcement ·
whether any AI agreement achieves *verification* (not just declaration) · emergence of
AI-assisted governance/verification tooling · input controls (compute, energy) with teeth.

**Slices:** 1, 5. **Personal stakes:** the pace mismatch compresses the owner's decision windows
too — it argues for making robust moves (playbook S1/S2) *earlier than comfort suggests*, because
tripwires may trip faster than revision cadence catches them. Directly supports a faster
revision cadence when settling proposal §5.

---

## W9 — Embodied AI removes the enforcement brake [argued]

**Owner's original statement (2026-07-07, round 3):** Claude did not count models in physical
bodies — robot power.

**Mechanism:** W2's brake (c) — the credible threat of the many — always ran through *human*
enforcers. Revolutions succeed when armies defect (1917, 1989 — the canonical channel); even
autocrats must pay, feed, and persuade soldiers and police, which forces a minimal bargain with
some human constituency. Embodied AI (drones, humanoids, autonomous weapons) severs enforcement
from human loyalty: no defection channel, no morale constraint, no bargain required. It also
extends W2's substitution from cognitive to physical labor — the bargaining collapse covers
everyone, not just knowledge workers — and decouples military power from population size, letting
small rich actors field large force. Combined with W4's asymmetric prediction it closes a
complete control loop: predict (sense) + enforce (act) with no human intermediary anywhere in the
loop. Early but pointed current evidence: drone-dominated attrition in Ukraine, the humanoid
investment surge, eroding human-in-the-loop language in autonomous-weapons debates.

**Counterargument (about timing, not direction):** Moravec's paradox still holds — dexterity and
unit-cost curves lag cognition by years; physical fleets have supply chains, manufacturing
bottlenecks, and electronic-warfare vulnerabilities (attackable in ways weights are not); and
governing a hostile population stays expensive even with robotic enforcement. This card loads the
mid and far tiers, not the near tier — the direction is conceded; the *date* is the live
question.

**Observables:** humanoid/drone unit-cost curves and deployment counts · dexterity benchmarks
crossing economic task thresholds · autonomous-weapons doctrine (human-in-the-loop language
eroding in official documents) · share of conflict outcomes attributable to autonomous systems ·
first *internal-security* (not battlefield) deployment of armed autonomous systems anywhere.

**Slices:** 1, far-tier world-states; touches 3 (US–China military balance). **Personal stakes:**
indirect but heavy — W9 is the variable that most differentiates "bad but navigable" from
"locked-in" far-tier world-states, because it decides whether W2's collapse is merely economic or
also political. It belongs on the watchlist for the far tier's *where-to-settle* question.

---

## W10 — The legible planet: from open world to game board [contested in part]

**Owner's original statement (2026-07-07, round 4):** 200 years ago this planet was like a vast
unknown universe to humans; today, with too-powerful tools and too-intelligent AI, it looks like
a Go board before professional players — complex, but with very limited optimal strategies. And
the world is like a slightly imbalanced Go position: common people think the game is still close,
while the professional already sees the definite end and simply resigns.

**Sub-claim (i) — the frontier has closed [conceded, argued]:** 200 years ago exit was a live
strategy: emigrate, homestead, disappear. Exit was the implicit fourth brake on domination
(Hirschman's *exit* alongside *voice*) — the weak could always leave the game. A fully mapped,
sensed, networked planet forecloses exit-as-escape: what remains is jurisdictional arbitrage
(decaying on W6's license timeline) and, marginally, space (not material on this project's
tiers). This completes the brake-removal table recorded in W2's amendments — and it makes the
one remaining exit form, *choice of jurisdiction*, time-sensitive.

**Sub-claim (ii) — the position is already readable to a strong-enough evaluator [contested]:**
Go's readability rests on five properties, and the world lacks every one of them.

- *Perfect information.* The world is poker, not Go: hidden state, private minds. In
  imperfect-information games optimal play is *necessarily randomized* (bluffing), and "definite
  end" evaluations do not exist — even superhuman poker AI wins in expectation and can never see
  a "decided" hand the way a Go engine sees a decided board.
- *Two players.* N-player games have no minimax value — only equilibrium selection among
  coalitions, and beliefs still choose the equilibrium (W7's surviving argument). The "winning"
  player can be dogpiled.
- *Zero-sum.* The world contains bargains; "resign" is not even a defined move. The readable end
  of a non-zero-sum game is a *settlement* — and Fearon says the settlement beats fighting for
  both sides. The evaluator does not create the imbalance; it *prices* it. The badness lives in
  the position (W2's brakes), not in the eyesight.
- *Fixed rules.* Go's rules never change mid-game; the world's rules are endogenous — players
  add rows to the board while playing (new technology, new institutions, input regulation, W8).
  "The definite end" of a rule-changing game is undefined.
- *A non-embedded evaluator.* A Go engine is not a stone on its own board; a world-evaluator is
  inside the position it evaluates. Reflexive prediction faces diagonalization limits (a
  theorem-shaped obstacle, not an engineering gap), and rival evaluators mutually cancel
  readability (W4's near-peer clause). Plus computational irreducibility: Go's space is vast but
  *cold* — discrete, static, fully specified; the world's is continuous, hot, self-modifying.

Empirical anchor: no current AI reads the world-game at professional depth — forecasting evals
sit at or below top human superforecasters, with calibration degrading fast past ~12 months. The
"professional player" for the world-game does not exist yet; whether one emerges is a tracked
slice-1 observable, not an assumption either way.

**The socially valid core of (ii) [conceded]:** the fear does not require the game to *be*
decided — only that the powerful *believe their evaluator*. Actors who trust a strong evaluator
act as if the end were visible: quiet repositioning, exit purchases, fortification — resignation
*behavior*. An overconfident evaluator in powerful hands is dangerous even when wrong —
especially when wrong. Watch what the holders of the best evaluators *do*, not what they say
(→ playbook T5).

**Observables:** AI-vs-superforecaster benchmark gap (does a world-game professional emerge) ·
elite resignation behavior: clustered hard-asset flight, citadel/bunker investment,
exit-infrastructure acquisition by the best-informed actors · legibility metrics (biometric
coverage, satellite revisit cadence, data-broker reach) · health of jurisdictional arbitrage
(golden-visa closures; W6-correlated).

**Slices:** 1, far tier; (i) feeds 3 directly. **Personal stakes:** (i) makes the surviving exit
form — jurisdiction choice — time-sensitive, reinforcing S1 and the far tier's where-to-settle
question; (ii)'s social core becomes tripwire T5: elite resignation behavior as
revealed-preference evidence about what the strongest evaluators see.

---

## W11 — The benevolence regime: the many live by the sovereign's virtue and mood [argued]

**Owner's original statement (2026-07-07, round 5, correcting Claude's W10 emphasis):** an
overconfident strong evaluator is not so frightening; a genuinely correct super-evaluator and
predictor is more frightening. Common people are just alive because of the superpower's virtue
and mood.

**Mechanism (conceded core, named):** this is **domination** in the strict republican-theory
sense (Pettit): unfreedom is not interference but *dependence on the arbitrary will of another* —
the kindly master's slave is still a slave. And it is Adam Smith inverted: we normally expect our
dinner not from the butcher's benevolence but from his self-interest — exchange, not virtue. When
the exchange value of the many goes to zero (W2, all four brakes removed), **only the benevolence
term remains**. "Virtue and mood" is exactly the right decomposition: virtue = the sovereign's
utility function; mood = its stability over time. The owner's correction of Claude also stands
recorded: a *wrong* evaluator's dangers are recoverable — errors create slack, exploitable cracks,
eventual reality-correction — while a *correct* evaluator forecloses the slack. Wrongness kills
by accident; correctness dominates gently and permanently.

**Reconciliation with W10's social core (both survive, on different tiers):** the overconfident
evaluator is the **near/mid-tier** danger (it exists today; hence tripwire T5); the correct
evaluator is the **far-tier** danger (it requires W10(ii)'s "professional player" to actually
emerge). The cards do not conflict — they schedule the same fear.

**Two structural moderators (Claude's addition — what separates "living under law" from "living
under mood"):**

- *Plurality and residual exit.* One sovereign → pure grace. Multiple sovereigns competing for
  anything at all — status, allies, legitimacy, migration of the still-useful — leave the many
  residual leverage, and exit-between-sovereigns (the last remnant of W10(i)'s frontier) stays
  worth something. Unipolar vs. multipolar is therefore *the* first-order far-tier branch
  variable for how bad the benevolence regime gets.
- *Institutionalization of virtue — including in the enforcement layer itself.* The historical
  answer to domination is constitutionalism: replacing mood with rules. The AI-age version has a
  twist W9 missed: **an aligned model that refuses unlawful orders is a robot that CAN defect.**
  W9 said embodiment removes the enforcer-loyalty brake because robots don't defect — but refusal
  can be deliberately re-engineered into the enforcement layer. Whether frontier deployments to
  military/police preserve refusal capabilities, or field stripped "helpful-only" variants, is
  the live design question that decides whether brake (c) gets re-installed by design.

**Observables:** unipolarity vs. multipolarity indicators (capability gap between top-2 AI
powers/labs) · whether military/police AI deployments retain refusal/constitutional constraints
or field stripped variants · enforceable charters binding sovereign AI use (not declarations) ·
golden-visa/exit-between-jurisdictions health (shared with W10) · early welfare policy in
post-labor sectors (does the benevolence term show up when exchange value dies — UBI-like
responses as *evidence about sovereign disposition*).

**Slices:** far tier (primary), 3, 5. **Personal stakes:** under a benevolence regime, personal
strategy shifts from bargaining (obsolete) to **positioning within grace**: choose the
jurisdiction whose sovereign's disposition is most institutionalized and most stable — i.e., pick
the polity by its *AI-constitutional quality*, not its GDP — and keep optionality between
sovereigns while exit still functions. This sharpens the far tier's where-to-settle criterion and
further reinforces the local playbook's front-loading moves.

---

## W12 — Planetary circumscription: the bounded arena converges toward one winner [contested in part]

**Owner's original statement (2026-07-07, round 6, countering W11's plurality moderator):**
multiple sovereigns is just a temporary imbalanced state — isolated systems converge very easily
to one winner, theoretically. Empirically: Europe and Russia are going down; China and India are
rising, but the propelling power is population, and population is itself temporary (growth rates
must fall). After all, the planet is too small and isolated for current advanced humans.

**Named lineage (validating the intuition):** this is **circumscription theory** (Carneiro 1970)
at planetary scale — states first formed exactly where populations were *bounded* (river valleys,
coastal strips) because the defeated could not flee and were absorbed instead. W10(i)'s closed
frontier is planetary circumscription: no exit for losers → absorption → consolidation. The
world-state-as-attractor conclusion has its own literature (Wendt's "Why a World State Is
Inevitable"; Morris's war-makes-larger-units trajectory: bands → states → empires → ?).
Isolation conceded outright for this project's horizons: no meaningful off-world autonomy by
2040.

**Physics correction that strengthens the owner (recorded honestly):** isolated systems in the
thermodynamic sense converge to *equilibrium* — maximum entropy, uniform mixing — not to one
winner. Winner-take-all requires a **driven system with increasing returns** (positive feedback).
But that is exactly what the AI world supplies (W2's compounding), so the owner's conclusion
survives with the corrected mechanism: bounded arena + compounding advantage + no exit →
absorption dynamics.

**The fuel-transition extension (Claude's addition, strengthening the owner):** population was
history's *equalizing* power fuel — every country has people; fertility is nature's
redistribution. The owner is right that it is also temporary (China already shrinking; India's
fertility ≈ replacement and falling). But W2/W9 imply something stronger: AI **deprecates
population as a power fuel altogether**, replacing it with compute + energy + capital, which
concentrate far harder than people ever did. On the new fuel metric the candidate set is already
a **US-system / China-system duopoly** (Europe and Russia nowhere; India's rise may be the last
population-fueled rise in history, and it stalls unless converted into compute/capital before the
deprecation completes).

**Contest — on permanence, not direction:** the owner's own civilization wrote the canonical
counterevidence: 天下大势，分久必合，合久必分 — "long united, must divide; long divided, must
unite" (三国演义 opening). Every circumscribed arena that converged to universal empire (China
repeatedly, Rome once) subsequently *fragmented* — via principal-agent decay, succession crises,
overextension (Tainter's declining marginal returns to complexity). Honest concession: AI
plausibly patches the classic fragmentation channels — agent loyalty (W9: robots don't defect),
succession (institutional sovereigns don't die), administrative decay (W10 legibility). Two
counter-mechanisms survive the patching:

- *Nested multipolarity.* "One winner" is never one agent — the winner is a coalition (party,
  board, factions), and the game continues *inside* it. Convergence moves the multipolarity
  inward rather than ending it; W11's plurality moderator partially survives as internal
  factional competition.
- *Seki.* In Go's own terms: professional games do not always converge to one color — boards end
  with **mutual life**, regions where neither side can move without dying. Nuclear deterrence
  already froze one bipolar endgame for 80 years; W3's MAIM logic is explicitly an attempt to
  engineer AI-era mutual life. The convergence attractor may stall at **two** because the final
  absorption is the one move whose cost exceeds its value even for a correct evaluator.

**The far-tier trichotomy (what this card actually settles):** the end-state set for the
2032–2040 tier is now structured — (1) **resolve-to-1** (one pole absorbs or definitively
outgrows the other), (2) **freeze-at-2** (seki: durable US–China mutual life under AI
deterrence), (3) **fragmentation-of-a-pole** (internal decay wins before external convergence
does). Probabilities over this trichotomy are a first-class forecast.md deliverable.

*Amended 2026-07-21 (round 8):* two connections. (1) The trichotomy conditions on the capability
driver sustaining; the plateau branch now has its own card — W16 — where the fuel transition
partially *reverses*: resource endowments revalue (Russia, the Gulf write partially back up on
that branch) while population stays deprecated in both branches. (2) W14 (elite life extension)
patches the fragmentation channel further than this card's honest concession allowed: succession
crises — history's most reliable fragmenter — die with mortal sovereigns.

**Observables:** top-2 compute/energy gap trajectory (Epoch-class data) · whether US–China AI
deterrence doctrine stabilizes into declared mutual-restraint (seki evidence) or one pole opens a
decisive lead · India's conversion rate of demographic dividend into compute/capital before
deprecation · internal-cohesion stress in both poles (elite purges, constitutional crises,
succession clarity) · EU strategic relevance in AI inputs (a control: the card predicts continued
decline).

**Slices:** far tier (primary), 1, 3. **Personal stakes:** → local personal layer. (The
trichotomy is the owner's branch map; the branch-by-branch personal reading lives locally.)

---

## W13 — The physical rescues are mispriced: real escape hatches are political, not physical [argued]

**Owner's original statement (2026-07-07, round 7):** there may be rescues for humans, but very,
very difficult — nearly forbidden in physics. Usable nuclear fusion is half a point, but very
hard and maybe not possible. Space colonization to other stars would thoroughly rescue humans,
but is nearly definitely impossible.

**Physics honesty (modality corrected, pricing roughly upheld):**

- *Fusion* is not physics-forbidden — the sun runs, H-bombs work, and NIF crossed target gain > 1
  in 2022 (later ~2.4×). It is an engineering-economics problem: sustained gain, first-wall
  materials, tritium breeding, capex per MW. Realistic grid relevance lands 2035–2050 — i.e.,
  mostly *after* this project's far tier. "Maybe not possible" is too strong; "not decision-
  relevant before 2040" is about right.
- *Interstellar colonization* is likewise not forbidden, but the arithmetic prices crewed exit at
  effectively zero for a century: a 10⁶ kg ship at 0.1c carries kinetic energy ~4.5×10²⁰ J —
  order of magnitude, *humanity's entire annual primary energy consumption*, per ship, before
  deceleration. The owner's "nearly definitely impossible" stands for populations on any
  policy-relevant timescale.

**The rescue-value contest (where the card earns its title):**

- *Fusion is half a rescue for the wrong party.* Abundance does not redistribute — **the
  distribution of abundance is set by the pipe, not the flow.** Fusion is maximally concentrating
  in geometry: capital-intense, plant-scale, tritium-regulated — the ultimate W6 *licensed*
  technology. And note its first customer: the AI industry is already pre-buying fusion
  (Helion–Microsoft PPA, lab-adjacent investments) as **datacenter fuel**. Fusion arriving feeds
  the compute pole before it feeds anyone else. Meanwhile the actually-decentralizing abundance
  tech already exists: solar + batteries — deployable at household scale, cost curves still
  falling, effectively unlicensable. The boring present tech is more rescue-shaped than the hard
  future one, purely because of distribution geometry.
- *Interstellar exit is a category error as a rescue for the many.* Even if possible, an escape
  hatch priced at civilizational energy budgets is boarded only by sovereigns — it is the
  ultimate elite exit (T5's endpoint). And rescue-by-exit reproduces the game inside the
  lifeboat: a generation ship is the most circumscribed arena imaginable — W12 dynamics at
  maximum, zero exit, one hull. Nearer term, a Mars colony is the *perfected* W11 benevolence
  regime: the sovereign licenses the **air**. Space colonization rescues the *species* (existence
  diversification against planetary catastrophe) while *deepening* the individual condition. It
  answers x-risk, not domination.

**The completed rescue portfolio (ordered by probability × rescue-value-for-the-many):**

1. **Constitutional enforcement / refusal-capable enforcers** (W11's second moderator) — restores
   brake (c) by design. Politics-hard, not physics-hard. Being decided *now*.
2. **Diffusion winning** (W2/W6 crux, tripwire T4) — the many keep frontier tools. Already
   partially real; economics- and politics-contingent.
3. **Seki** (W12) — not a rescue, but frozen plurality preserves between-poles slack.
4. **Solar + batteries** — quiet, deployed, decentralizing abundance.
5. **Fusion** — half a point, concentrating geometry, mostly post-2040.
6. **The stars** — ~0 this century; and not a rescue for the many even in success.

**The closing symmetry:** the rescues that would actually rescue the many are forbidden by
nothing except politics. Politics is more malleable than physics — grounds for hope — and less
reliable than physics — grounds for the owner's despair. Both true; the ratio is what forecast.md
prices.

**Observables:** fusion pilot-plant sustained-gain milestones · who signs fusion PPAs first
(AI-datacenter buyers confirm the concentrating geometry) · solar+battery cost curves and
*distributed* (behind-the-meter) share of deployment · refusal-capable-enforcer deployments
(shared with W11) · open-weights gap (shared with T4).

**Slices:** 1, 4 (energy as AI-capex variable), far tier. **Personal stakes:** place no planning
weight on physical rescues inside the project horizon — the hedgeable rescues are the political
ones already in the playbook (T4, W11's constitution-watch). Energy tech enters his life mainly
through slice 4: fusion exposure ≈ AI-capex beta; solar ≈ the deflation trade — treat as forecast
variables, not conviction trades.

---

## W14 — The first AI dividend the powerful buy is time: elite life extension removes the mortality brake [argued]

**Owner's original statement (2026-07-21, round 8):** leaders and upper-class people, if they own
AI power, their most prior target would be developing biotech to extend life. Will that be good
for common people? Still, common people only have value as experiment material.

**Mechanism (priority claim conceded on revealed preference):** the billionaire longevity wave
*predates* AGI — Altos Labs (~$3B, Bezos/Milner), Retro Biosciences ($180M from Altman), Calico,
the Thiel circle. The economics make it predictable, not incidental: for an actor whose wealth
already saturates every purchasable good, remaining lifespan is the only binding constraint, so
life extension is the first thing AI-scale power gets spent on. The systemic significance
(completing W2's brake table): mortality — brake (b) — was the one brake that operated *on* the
powerful. Succession is history's most reliable redistributor; W12's fragmentation channel runs
straight through it; a dictator's actuarial table is the opposition's most dependable ally. Elite
life extension removes the last *natural* turnover mechanism — an unaging sovereign has no
succession crisis — which is why this card feeds W12's resolve-to-1 permanence, not just the
far-tier texture.

**The trickle-down question (the sharp edge):** whether it reaches the many decomposes by *why*
health ever trickled down. Mass public health was never charity — it was **fuel maintenance**
(biopower: states cultivated population health because population *was* power — soldiers,
workers, taxpayers). W12's fuel transition deprecates population exactly as the life-extension
tech arrives, removing the engine behind mass health investment. Default distribution on the
cards' main line: longevity for the sovereign tier, decaying public-health investment for the
many — by incentive gradient, not malice.

**The experiment-material sub-claim (amended):** real, precedented (the poor as trial substrate
is the historical norm), but plausibly *transitional* — organoids, digital twins, and simulation
shrink the need for mass human subjects, and the rich self-experiment eagerly (the biohacker
pattern). The grimmer *stable* form of the owner's point: after labor value → 0 (W2), the many's
residual instrumental values enumerate shortly — trial substrate, behavioral-data source, status
audience for competing sovereigns (W11's plurality). The durable residual role is data and
audience, not guinea pig.

**Strongest counterargument:** therapeutics are information goods — once a molecule or protocol
exists, marginal cost collapses and generics diffuse (vaccines, statins: broad diffusion within
decades is the historical curve). If the first-generation longevity stack is pill-like
(rapamycin-class small molecules), it diffuses regardless of sovereign intent. The concentration
case requires longevity to be *clinic-like* geometry (continuous, personalized, capital-intense —
cell reprogramming, constant monitoring): W13's rule that distribution is set by the pipe, not
the flow. Which geometry wins is open — and W6 licensing can be imposed on either, so the
counterargument is strongest where licensing is weakest.

**Observables:** billionaire/sovereign-fund longevity investment flow · pill-like vs. clinic-like
geometry of first-generation interventions · top-1%-vs-median life-expectancy gap in AI-leading
countries (already widening; the card predicts acceleration) · public-health spending share in
economies undergoing labor displacement · trial-recruitment demographics for longevity therapies
· first head of state visibly on a longevity protocol.

**Slices:** far tier (the tracked longevity variable — this card is its argument), 1 (AI-for-bio
as capability evidence), 4 (longevity biotech as an investment theme). **Personal stakes:** →
local personal layer.

---

## W15 — The insider coup runs through the state, not against it [argued]

**Owner's original statement (2026-07-21, round 8):** will a tech company's small elite group try
to secretly develop AI without the alignment layer, to rule people? But he thinks they cannot
really beat governments.

**Mechanism (both halves validated, then fused):** the threat is real and has a literature —
AI-enabled coups (Davidson et al. 2025: a small group using secretly loyal AI to seize power) and
internal-deployment risk (Apollo Research: the most capable models run *inside* labs for months
with no outside oversight). Two amendments sharpen it. First, per W1: nobody removes the
alignment layer — alignment is principal-agnostic, so the feared artifact is not an *unaligned*
model but a **secretly narrowly-aligned** one (the stripped "helpful-only" internal variant is
the existing technical form). Second, the secrecy asymmetry: frontier *capability* cannot be
hidden from states (compute footprint, energy draw, talent flows — intelligence services see all
three), but *loyalty* can. Fine-tuning a secretly-loyal variant is cheap and invisible, and no
eval for "aligned to whom" currently exists. **You cannot hide the model; you can hide who it
serves.**

**The owner's "cannot beat governments" — correct, and beside the point:** in open contest the
state wins — datacenters are immovable seizable assets (W6's physical layer), the state holds
legal violence and the nationalization option (W1), and the East India Company precedent runs
both ways (a company acquired an army and ruled a subcontinent — under state charter, and was
absorbed by the Crown in 1858 the moment it grew threatening). But the coup pathway is not
company-beats-state; it is **faction-captures-state**. The lab does not fight the government — it
staffs it (personnel pipelines into AI-policy roles), supplies it, and becomes its epistemic
infrastructure: when the state's analysts, drafting tools, and decision support run on a lab's
models, a secretly-loyal model *is* state capture with no shot fired. The modal danger is a
fusion faction spanning lab and government — W1 (state captures AI) and this card (lab captures
state) converging from opposite directions onto the same object.

**Strongest counterargument:** singular secret loyalty is hard to sustain — several labs, several
agencies, and rival states all audit each other; whistleblower probability scales with headcount
(the Manhattan Project leaked to Moscow within years); and the interpretability/eval tooling
alignment research is building is the natural loyalty-audit instrument — if it matures inside
W8's pace window.

**Observables:** internal-deployment governance with third-party access (does anyone outside the
lab see internal models?) · helpful-only internal-variant policy at frontier labs · lab↔state
personnel flow and epistemic dependence (which agencies run on which lab's models) ·
secret-loyalty / sleeper-agent eval research maturing into deployable audits · whistleblower
protections at frontier labs · any attributed incident of a model with undisclosed instruction
layers.

**Slices:** 1, 5; far tier through W11 (whose enforcement layer inherits whatever loyalty the
fielded models actually carry). **Personal stakes:** → local personal layer.

---

## W16 — The ceiling branch: a plateau rebalances between states only if diffusion outruns lock-in; at the ceiling, advantage reverts to resources [argued; contested in part]

**Owner's original statement (2026-07-21, round 8):** if AI tech itself has a ceiling, the
countries left behind have time to chase, and the planet will finally come back to balance —
will it? Then resources are the key to distinguishing strong and weak.

**Standing:** this card begins the stress test W7's round-7 note flagged as the largest unpriced
variable — every prior card conditions on the capability driver compounding; W16 structures the
branch where it does not.

**The ceiling-height trichotomy (sharpening "a ceiling" into decision-relevant cases):**

- **Low ceiling** — AI plateaus as a tool; human labor stays complementary. Most of W1–W13
  dissolves; the world stays recognizable. This is the only *truly* rebalancing ceiling — and the
  only branch where the owner's "back to balance" holds fully.
- **Mid ceiling** — labor is substituted but capability stops short of runaway. Between-states
  rebalance becomes *possible* (see the race below); within-state W2 dynamics persist everywhere.
- **No ceiling in the relevant range** — the main-line cards.

**Catch-up logic (conceded, named):** Gerschenkron's late-mover advantage — adopters of proven
technology move faster than its inventors; at a hard ceiling the frontier lead is a *transient of
the growth phase* and diffusion erases it. History supports the owner here: transient technology
monopolies have never converted into permanent hegemony — Britain's industrial lead diffused
within decades; the US nuclear monopoly lasted four years and was never converted (preventive war
advocated, never executed — W3's counterargument).

**Contest 1 — balance is a race, not a consequence:** rebalancing requires **diffusion to outrun
lock-in** — a two-clock race, the same shape as W8's pace mismatch. The leader's transient lead
is exactly what W2/W6/W9/W10 say converts into *permanent structural* position: robotic
enforcement, license regimes, planetary legibility, absorbed institutions. AI differs from steam
and nuclear in one respect — the lead itself works on entrenching the lead (capability automates
its own conversion). If lock-in completes before laggards arrive, the ceiling *preserves* the
frozen hierarchy — no further capability change ever disrupts it. A ceiling reached after
lock-in is the lock-in's best friend. So: early ceiling → the owner's rebalancing world; late
ceiling → W12's trichotomy with extra permanence.

**Contest 2 — between is not within:** the ceiling equalizes *between states* but not *within
societies*. At any ceiling high enough to substitute for labor (mid or above), W2's
bargaining-power collapse persists in every country that reaches it — the many do not regain
leverage because every state owns the same AI. "Planet back to balance" is a between-states
claim only.

**Resource reversion (the owner's conclusion, conceded and sharpened):** at a diffused ceiling,
intelligence commoditizes; with algorithms equal everywhere, advantage reduces to what you can
*feed* them — energy, materials, territory, installed industrial base. Near-thermodynamic
framing: equal intelligence per watt → power scales with watts. Resources are key in *both*
phases, but different sets: during the race, energy and chips already bind (datacenter power is
today's frontier bottleneck); at the ceiling the binding set broadens to materials and land.
Testable geopolitical inversion: resource-rich middle powers (Gulf states, Canada, Australia,
Brazil — and Russia, which W12 wrote down on the compounding branch) revalue upward relative to
skill-rich, resource-poor states (Japan, Korea, Taiwan, Singapore, Israel, most of Europe).
Population stays deprecated on *every* branch above the low ceiling — robots at the ceiling
still substitute labor, so W12's fuel transition survives; only its resource term reverses.

**Strongest counterargument (against the branch mattering at all):** a ceiling may never be
observable as an event. Capital and energy constraints produce a slow bend, not a wall — and
during a slow bend the leader's *integrated* advantage (lead-size × lead-years) keeps
accumulating even as growth slows. The decision-relevant quantity is not ceiling existence but
the **gap-years integral** before convergence: a slow asymptote can deliver lock-in as surely as
endless compounding.

**Observables:** frontier-vs-best-laggard capability gap per release cycle (Epoch-class data —
closing vs. widening is the single sharpest discriminator) · scaling returns per dollar and per
watt across generations (bend detection) · data-wall evidence (synthetic-data efficacy at the
frontier) · whether frontier training investment growth stalls (the economic ceiling arrives
before the physical one) · resource-state positioning: Gulf/Russia/Australia as compute-energy
hosts (revealed belief in the resource branch) · laggard-state adoption of near-frontier open
weights at scale (diffusion-speed measure).

**Slices:** 1 (primary — this is the driver-variable card), 3, 4, far tier (conditions all
far-tier branching). **Personal stakes:** → local personal layer.
