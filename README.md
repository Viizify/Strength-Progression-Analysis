# Volume Debate: A 10-Month Strength Training Analysis

**How three training phases compared on estimated 1RM growth — August 2025 to May 2026.**

This repository contains the raw training log and analysis from a personal experiment testing how reducing the number of **working sets per exercise** affected strength progression over ~40 weeks. Across 159 workouts and 29 exercises, weekly strength gains roughly **doubled with each volume cut** — from 0.52%/week with 3 working sets, to 1.03%/week with 2 sets, to 1.87%/week with 1 set.

---

## TL;DR

| | Phase 1 | Phase 2 | Phase 3 |
|---|---|---|---|
| **Period** | Aug 11 – Oct 31, 2025 | Nov 1, 2025 – Mar 26, 2026 | Mar 26 – May 16, 2026 |
| **Duration** | 11.6 weeks | 20.6 weeks | 7.3 weeks |
| **Split** | 5-day rotation (Workout 1–5) | 4-day Upper/Lower × 2 | 4-day Upper/Lower × 2 |
| **Working sets / exercise** | 3 | 2 | **1** |
| **Avg Str. gain per week** | 0.52% | 1.03% | **1.87%** |

Less is more. Across all three phases, halving the working sets roughly doubled the weekly strength gain

---

## Background

The dataset spans **August 11, 2025 → May 16, 2026** (~40 weeks of continuous training). The training split changed once (5-day → 4-day Upper/Lower) at the start of Phase 2 and stayed constant from Phase 2 → Phase 3 — meaning **the only major variable changed between Phase 2 and Phase 3 was the number of working sets per exercise** (2 → 1). That transition is the cleanest comparison in the dataset.

The original motivation was the long-running 'volume debate' in strength training: specifically, whether reducing training volume in favor of higher per-set intensity would still drive strength gains — and at what point the trade-off between volume and intensity becomes favorable for progress

---

## Method

### Data collection
- **Source:** personal workout log (one row per working set).
- **Fields:** session type, date, exercise, weight (kg), reps, RPE.
- **Rows:** 1,510 working sets across 159 sessions and 29 exercises.

### Estimated 1RM (e1RM)
Each set's e1RM was calculated from weight, reps, and RPE using:

```
e1RM = Weight × (1 + (Reps + RIR) / 30)
RIR  = 10 − RPE
```

This is the Epley formula extended with RIR (Reps in Reserve) to handle sub-maximal sets, which makes it possible to compare progression across sets that weren't taken to failure.

### Phase metrics
For each exercise within each phase:
- **Start e1RM** = average of the first 3 sessions in the phase
- **End e1RM** = average of the last 3 sessions in the phase
- **% per week** = total % gain ÷ number of weeks between first and last session

Averaging across the first/last 3 sessions smooths out single-session noise (a bad sleep, a missed warm-up, an off day).

---

## Results

### Per-phase summary (across all tracked exercises)

| Phase | Duration | Avg. total gain | Avg. %/week |
|---|---|---|---|
| P1 — 3 sets, 5-day split (Aug–Oct 2025) | 11.6 wk | 5.9% | 0.52% |
| P2 — 2 sets, Upper/Lower (Nov 2025 – Mar 2026) | 20.6 wk | 13.5% | 1.03% |
| P3 — 1 set, Upper/Lower (Mar–May 2026) | 7.3 wk | 12.0% | **1.87%** |

### Phase 3 — exercise-by-exercise gains (1 set per exercise)

All 20 tracked exercises showed positive 1RM progression in Phase 3:

| Exercise | P3 gain |
|---|---|
| Leg Press (Machine) | +25.0% |
| Rear Delt Reverse Fly (Cable) | +21.5% |
| Seated Calf Raise | +21.0% |
| Calf Press (Machine) | +20.5% |
| Lat Pulldown (Cable) | +19.9% |
| Lying Leg Curl (Machine) | +18.1% |
| Lateral Raise (Dumbbell) | +15.8% |
| Bicep Curl (Machine) | +14.8% |
| Hip Thrust (Machine) | +11.5% |
| Shoulder Press (Machine Plates) | +10.5% |
| Romanian Deadlift (Barbell) | +9.9% |
| Sissy Squat (Weighted) | +8.4% |
| Seated Leg Curl (Machine) | +7.6% |
| Seated Row (Machine) | +7.5% |
| Bicep Curl (Barbell) | +7.4% |
| Incline Bench Press (Dumbbell) | +6.8% |
| Triceps Pushdown | +6.1% |
| Bench Press (Barbell) | +3.6% |
| Lunge (Dumbbell) | +3.1% |
| Single Arm Tricep Extension (Dumbbell) | +0.5% |

For comparison: Phase 1 had **5 regressions** (exercises that went backwards over the phase), Phase 2 had **8**, Phase 3 had **0**.

### Selected cross-phase trajectories

| Exercise | P1 %/wk | P2 %/wk | P3 %/wk |
|---|---|---|---|
| Bench Press (Barbell) | −0.46 | +0.10 | +0.50 |
| Hip Thrust (Machine) | +3.56 | +1.13 | +1.72 |
| Leg Press (Machine) | +1.09 | −0.05 | +3.72 |
| Seated Calf Raise | +1.05 | +1.80 | +3.13 |
| Shoulder Press (Machine Plates) | 0.00 | +0.91 | +1.56 |
| Triceps Pushdown | +3.05 | −0.04 | +0.91 |
| Rear Delt Reverse Fly (Cable) | 0.00 | −0.06 | +3.20 |

The pattern is uneven across exercises — some (Triceps Pushdown, Hip Thrust) gained fastest in P1, while others (Leg Press, Rear Delt) only really took off in P3. But the **aggregate** weekly gain still increased with each volume cut.

---

## Key findings

1. **Volume reduction coincided with accelerated gains.** Each cut in working sets (3 → 2 → 1) was followed by a roughly doubled weekly gain rate.
2. **Phase 3 was uniformly positive.** Zero regressions across 20 exercises — the only phase with that property.
3. **Plausible mechanisms (self-reported):**
   - With fewer sets to spread effort across, each remaining set carried more of the stimulus, and the lifter reported being more mentally prepared to push to true failure.
   - Subjective enjoyment of training increased as volume decreased, peaking in Phase 3 — likely improving adherence and effort quality.
   - Reduced fatigue between sessions may have allowed heavier loads and better recovery.

---

## Caveats (read these before drawing conclusions)

This is **a single-subject observational study, not a controlled experiment.** Several confounds limit how far the result generalises:

- **n = 1.** Individual response to volume varies enormously. What worked here may not work for others.
- **Order effects.** Phase 3 always came after ~32 weeks of accumulated training base. Some of the "Phase 3 effect" could be late-stage adaptation, not the set-count change itself.
- **Split change between P1 and P2.** P1 used a 5-day rotation; P2/P3 used a 4-day Upper/Lower. So P1 vs. P2 conflates *volume change* with *split change*. The cleanest comparison is P2 → P3 (same split, only sets changed).
- **Phase 3 is short.** 7.3 weeks is enough for neural adaptation but short for muscular hypertrophy — gains may not sustain at the same rate over a longer block.
- **e1RM is an estimate.** It approximates 1RM from sub-maximal sets and depends on the lifter's RPE accuracy. RPE calibration tends to improve over time, which can inflate measured "gains" in later phases independently of actual strength change.


---

## Repository contents

```
.
├── README.md                  ← this file
└── volume-debate-data.xlsx    ← full workbook (5 sheets)
```

### What's in the Excel workbook

| Sheet | Content |
|---|---|
| `Dashboard` | High-level summary, phase table, key findings (mostly English) |
| `Treningsperioder` | Phase definitions: start date, end date, split, working sets (Norwegian) |
| `Rådata` | Raw working-set log — 1,510 rows: session type, date, exercise, weight, reps, RPE (Norwegian field names) |
| `1RM Progresjon` | Per-exercise e1RM start/end/gain by phase, with %/week (Norwegian) |
| `Visualiseringer` | Pivoted data feeding the dashboard charts |

**Norwegian → English field glossary:**
- `Økt type` = Session type
- `Dato` = Date
- `Øvelse` = Exercise
- `Vekt` = Weight (kg)
- `Reps` = Reps
- `RPE` = Rate of Perceived Exertion (0–10)
- `Periode` = Phase
- `Working sets per øvelse` = Working sets per exercise
- `Snitt %/uke` = Average %/week
- `Fremgang` / `Tilbakegang` = Progress / Regression
- `gain kg` = Gain in kilograms

---

## Reproducing the analysis

To recompute e1RM and phase aggregates from `Rådata`:

```python
import pandas as pd

df = pd.read_excel("volume-debate-data.xlsx", sheet_name="Rådata")
df["RIR"] = 10 - df["RPE"]
df["e1RM"] = df["Vekt"] * (1 + (df["Reps"] + df["RIR"]) / 30)

phases = [
    ("P1", "2025-08-11", "2025-10-31", 3),
    ("P2", "2025-11-01", "2026-03-26", 2),
    ("P3", "2026-03-26", "2026-05-16", 1),
]

for name, start, end, sets in phases:
    mask = (df["Dato"] >= start) & (df["Dato"] <= end)
    print(name, "sets/ex:", sets, "rows:", mask.sum())
```

From there, group by `Øvelse`, take the mean e1RM of the first/last 3 sessions in each phase, and divide by the elapsed weeks to get %/week.
