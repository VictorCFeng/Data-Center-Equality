# Data Center–Driven Grid Costs & Price Impacts

This repository contains the data, code, and derived results used to quantify how data-center load growth affects **wholesale electricity prices**, **transmission cost allocation**, and downstream **burden and distributional outcomes** across major U.S. power markets.

The repo is intentionally **data-centric**: besides the core code and figure gallery, most folders store task-specific input data and intermediate artifacts.

---

## Repository structure

- **00_code/** — Required code to reproduce the main calculations and figures.
- **01_tables/** — Panel dataset for estimating the impact of **ISO-level** data center capacity on wholesale prices.
- **01_tables_city/** — Panel dataset for estimating the impact of **non-ISO cities’** data center capacity on wholesale prices.
- **02_fuel_mix/** — Raw generation mix (fuel mix) data for each ISO.
- **03_regressive_path/** — Inputs used to construct the **regressive scenario** for data-center capacity trajectories.
- **04_load_and_costs/** — Source files for **transmission charges** and **long-term load forecasts**, plus extracted/cleaned tables.
- **04_rider/** — PUC docket documents and extracted tables used to compute **data-center transmission cost responsibility** (“rider” allocation).
- **05_burden/** — Price decomposition, projections, and fuel-price forecast files used in burden calculations.
- **06_AI_accept/** — AI tool usage (adoption) data and related computed outputs.
- **07_employment/** — State- and county-level employment data and processing outputs.
- **08_tax/** — Raw and processed data related to tax incentives / abatements.
- **figures/** — Static (SVG) and interactive (HTML) visualizations.
- **results/** — Paper-facing outputs (processed tables, model outputs, summary artifacts).

---

## Large datasets (hosted on Google Drive)

Due to size constraints, the two panel datasets used for the price-impact regressions are **not stored directly in this GitHub repository**:

- `01_tables/` — panel inputs for ISO-level regressions  
- `01_tables_city/` — panel inputs for non-ISO city regressions  

They are hosted on Google Drive:

- **Google Drive folder**: https://drive.google.com/drive/folders/1YjEEAJrFbZg64ZUPRTsWpSEI4e6IMdKe?usp=sharing

---

## Figures (2025 static previews → click for interactive HTML)

GitHub README does not execute interactive HTML/JavaScript for security reasons.  
This repo therefore uses a simple pattern:

- The README shows **static 2025 SVG previews**.
- Clicking an image opens the **interactive Plotly HTML** hosted via **GitHub Pages**.

<p align="center">
  <a href="https://<username>.github.io/<repo>/figures/PJM.html">
    <img src="figures/PJM_2025.svg" alt="PJM 2025 (click for interactive)" width="49%">
  </a>
  <a href="https://<username>.github.io/<repo>/figures/MISO.html">
    <img src="figures/MISO_2025.svg" alt="MISO 2025 (click for interactive)" width="49%">
  </a>
</p>

<p align="center">
  <a href="https://<username>.github.io/<repo>/figures/ERCOT.html">
    <img src="figures/ERCOT_2025.svg" alt="ERCOT 2025 (click for interactive)" width="49%">
  </a>
  <a href="https://<username>.github.io/<repo>/figures/CAISO.html">
    <img src="figures/CAISO_2025.svg" alt="CAISO 2025 (click for interactive)" width="49%">
  </a>
</p>

---

## Enable the interactive figures (GitHub Pages)

To make the HTML figures clickable and fully interactive:

1. Go to **Settings → Pages**
2. Under **Build and deployment**, choose:
   - **Source**: Deploy from a branch
   - **Branch**: `main` (or your default branch)
   - **Folder**: `/ (root)` *(recommended; allows `/figures/*.html` to load directly)*
3. Save.

Once enabled, interactive figures will be available at:

- `https://<username>.github.io/<repo>/figures/PJM.html`
- `https://<username>.github.io/<repo>/figures/MISO.html`
- `https://<username>.github.io/<repo>/figures/ERCOT.html`
- `https://<username>.github.io/<repo>/figures/CAISO.html`

---

## Reproducibility (high level)

- Core scripts live in **00_code/**.
- Inputs are organized by task folder (see structure above).
- Outputs are written to **results/** and **figures/**.

If you maintain an entry-point script, document it here, e.g.:

```bash
python 00_code/run_all.py

