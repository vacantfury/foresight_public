# Foresight — scorecard

The third committed layer (design §1): resolved claims, Brier scores, and the calibration
table. Born 2026-07-26, at Fatebook adoption — empty by construction until the first claim
resolves (F25, resolve-by 2026-08-31). `forecast.md` stays canonical for claim text and
current probabilities; this file is the **resolution ledger** — a claim appears here when it
resolves and never leaves. Old editions' claims stay scoreable forever (design §2), and this
is where they land.

**Backend.** Each edition's claims are mirrored as private Fatebook questions (tags
`foresight`, `edition-v1`) at authoring time; resolutions are entered there (auto-Brier and
calibration charts) and recorded here as the committed record. The question map lives in the
local personal layer, not in this repo's committed half. The backend is a bounded trial with
a keep/quit checkpoint at the first revision (~Oct 2026) — if quit, this ledger simply
continues by hand; the format does not depend on the backend.

**Scoring rules.** Brier = (p − outcome)², outcome ∈ {0, 1}, with p = the last probability
stated in an edition before the claim's window closed. AMBIGUOUS resolutions score nothing
and are recorded with a reasoning note — an ambiguous resolution is also a defect report
against the claim's resolution threshold, and the successor claim gets a sharper one.
Multi-branch claims (F23's trichotomy) score with the multi-class Brier against the full
recorded distribution, not any mirrored binary.

## Resolution ledger

| F-ID | Claim (short) | Edition p | Resolved | Outcome | Brier | Notes |
|---|---|---|---|---|---|---|
| — | *first entry due at F25's resolution (resolve-by 2026-08-31)* | | | | | |

## Calibration table

Built once ≥10 claims have resolved — a reliability table on fewer is noise. Until then the
per-claim Brier column above is the whole scorecard.
