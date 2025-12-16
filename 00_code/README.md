## Notebook guide (by prefix)

Inside this folder, notebooks are grouped by a simple numeric prefix convention.  
In short: **1 → estimate price impacts**, **2 → project prices under scenarios**, **3 → quantify misallocation**, **4 → translate into energy-burden outcomes**, **5 → jobs/employment analysis**.

### `1_*` — Panel regressions: data center capacity growth → wholesale price growth
Notebooks starting with **`1_`** estimate the panel-regression effects of **data-center capacity growth** on **wholesale price growth** (baseline econometric estimation, controls, diagnostics, and main coefficient extraction).

### `2_*` — Price growth under different paths (built on `1_*`)
Notebooks starting with **`2_`** use the estimated effects from **`1_`** to compute **price growth trajectories under alternative capacity-growth paths/scenarios** (i.e., “what happens to prices if the data-center growth follows path A vs. path B”).

### `3_*` — Infrastructure cost misallocation across ISOs
Notebooks starting with **`3_`** compute **infrastructure cost misallocation** (who pays vs. who drives the upgrades) for each ISO/RTO, including the logic and accounting needed to quantify misallocated shares.

### `4_*` — Energy burden outcomes (before/after price increases; with/without misallocation)
Notebooks starting with **`4_`** translate wholesale price changes into **energy burden** outcomes across:
- different demographic / income groups,
- counties,
- states,

and compare:
- **before vs. after** wholesale price increases, and
- **with vs. without** infrastructure cost misallocation.

### `5_*` — Data center build-out and employment
Notebooks starting with **`5_`** analyze the relationship between **data center construction / capacity expansion** and **employment outcomes**, including fitting and correlation/regression-style analyses.

> Tip: If you want a “run order”, a typical workflow is **1 → 2 → 3 → 4**, with **5** as an independent analysis track.


