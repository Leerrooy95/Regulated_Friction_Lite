# Core Theory: The Regulated Friction Framework

**What this is**: the condensed version of the statistical backbone behind the main repository — the friction/compliance correlation and how it works. For what the research found about the bigger picture, in plain language, start with [`The_Structure.md`](The_Structure.md); this file is the numbers underneath it. For the full derivation, robustness suite, and changelog, see the main repo (linked throughout).

**Source**: distilled from `README.md`, `Report.md`, and `_AI_CONTEXT_INDEX/01_CORE_THEORY.md` in [The_Regulated_Friction_Project](https://github.com/Leerrooy95/The_Regulated_Friction_Project).

---

## The Core Finding

**Friction events predict compliance events with a 7-day median sequential lag.**

| Metric | Value |
|---|---|
| Correlation | r = +0.6196 |
| Significance | p = 0.0004 |
| Sample | n = 28 paired observations (30-week hand-scored dataset) |
| Historical backfill (2017–2024) | 66 pairs, median lag +7 days, Δr = +0.0012 (negligible change) |

**What this does NOT claim**: central coordination or intentional orchestration. The pattern is emergent — multiple actors responding to the same environmental signals (holidays, fiscal deadlines, media saturation) without needing to communicate. Correlation ≠ causation. The claim is structural: the pattern exists, is statistically significant, and is reproducible.

---

## The Two Event Types

| | Definition | Examples |
|---|---|---|
| **Friction event** | Anything that grabs public attention and consumes media bandwidth | Document releases, congressional hearings, scandals, viral moments, protests |
| **Compliance event** | An institutional action that might draw scrutiny normally, but proceeds with less attention because the public is watching a friction event | Executive orders, regulatory changes, acquisitions, sovereign wealth fund moves, personnel appointments |

Analogy used in the main repo: friction is the car crash on the highway everyone slows down to look at; compliance is what happens in the lane nobody's watching while they do.

---

## How the Pattern Works

```
Compliance goes through quietly  → friction dies down
Compliance meets resistance      → friction ramps up
```

No single actor has to be running this. Many actors (governments, financial institutions, media organizations) respond to the same calendar signals and the same attention gaps, and the pattern shows up in the timing. [`The_Structure.md`](The_Structure.md) covers the other half: why attention matters so much once the other checks have been removed.

> **A note on the old name.** Earlier versions of this project called this the "Thermostat Model." Lite retired that term on 2026-09-22 because it implied a single mechanism with someone operating it, which is more than the evidence supports. Main-repo files still use it (`01_CORE_THEORY.md`, `tier3_thermostat_ruleset.md`, `Thermostat_Explained.md`, and others), and a few condensed files here quote those sources directly. When you see "thermostat" in quotes, that's the source's wording, not this repo's.

### Dual-Track System (evolved understanding, Feb 2026)

| Track | Domain | Mechanism | Function |
|---|---|---|---|
| **Track A** | Foreign / geopolitical | Information leverage | High-visibility friction (unreleased data, cyber intrusions) holds diplomatic attention |
| **Track B** | Domestic / structural | Capital leverage | While Track A consumes attention, capital/infrastructure restructuring proceeds |

Most of what [`The_Structure.md`](The_Structure.md) documents (the civil-service changes, PCAST, Arkansas) is Track B material under this labeling. Note that the main repo's v10.0 summary uses the same two labels for a different split. See [`Corrections_and_Caveats.md`](Corrections_and_Caveats.md) under "Still open."

---

## Why 7 Days, Not 14

Originally reported as a 14-day lag, based on 2-week index binning in the 30-row dataset. A higher-resolution pass on the 66-pair historical backfill dataset found the actual median lag is 7 days (mean 6.5 days). The underlying correlation (r = 0.6196, p = 0.0004) didn't change — only the lag label, corrected for measurement precision.

---

## Robustness (Independent Verification)

The core correlation was independently stress-tested with 16 statistical scripts (permutation, Granger causality, autocorrelation-adjusted bootstrap, rolling window, and more). It survived all of them:

| Test | Result |
|---|---|
| Permutation (10K shuffles) | p < 0.0001 |
| Granger causality (lag 1) | p = 0.0008 |
| Block bootstrap (autocorrelation-adjusted) | p = 0.008 |
| December 2025 exclusion | ρ = 0.60 (holds) |
| Historical backfill (2017–2024) | Δr = +0.0012 |

Full suite and scripts: `Project_Trident/Copilot_Opus_4.6_Analysis/Statistical_Tests/` in the main repo.

---

## What the Theory Does NOT Claim

1. Central coordination between actors
2. That friction events *cause* compliance events
3. Illegal activity — this documents observable patterns only
4. That any individual acts with improper intent

## Limitations

1. **Correlation ≠ causation** — events cluster together; one doesn't necessarily cause the other.
2. **Event classification involves judgment** — what counts as "friction" vs. "compliance" requires researcher decisions.
3. **Granger causality is bidirectional** on event-count data, suggesting a common driver rather than simple one-way causation (the hand-scored data does show friction → compliance at short lags).
4. **Alternative explanations remain possible** — fiscal calendar effects, bureaucratic cycles, coincidence.

## Falsification Criteria

The theory would be falsified if the r = 0.6196 correlation can't be reproduced, the December 2025 clustering turns out to be a data artifact, future friction–compliance windows show no pattern, or calendar anchors show a random event distribution.

---

## Go Deeper

- **Plain-language version of what it all adds up to**: [`The_Structure.md`](The_Structure.md).
- **What the 7-day lag can and can't carry**: "Verification and Methodology" in [`AI_Context_Index.md`](AI_Context_Index.md).
- **Full derivation & event history**: [`Report.md`](https://github.com/Leerrooy95/The_Regulated_Friction_Project/blob/main/Report.md) in the main repo.
- **Reproduce it yourself**: [`Run_Correlations_Yourself/`](https://github.com/Leerrooy95/The_Regulated_Friction_Project/tree/main/Run_Correlations_Yourself) in the main repo.
- **Robustness suite**: [`Statistical_Tests/`](https://github.com/Leerrooy95/The_Regulated_Friction_Project/tree/main/Project_Trident/Copilot_Opus_4.6_Analysis/Statistical_Tests) in the main repo.
- **Original core-theory file**: [`01_CORE_THEORY.md`](https://github.com/Leerrooy95/The_Regulated_Friction_Project/blob/main/_AI_CONTEXT_INDEX/01_CORE_THEORY.md) in the main repo.
