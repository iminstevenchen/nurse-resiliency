# Nurse Resiliency — Burnout Risk Modeling

Analysis of burnout and resiliency in **6,000+ medical providers** — nurses and anesthesiologists from national survey datasets (ASRA, ASPAN) and advanced practice nurses from a VUMC-wide dataset. Completed as a project with the Vanderbilt Data Science Institute (Fall 2021).

> ⚠️ **No data is included in this repository.** The de-identified survey data is restricted to project members. This repo documents the problem, approach, and methods only.

## Problem

Provider burnout is a major driver of attrition and patient-safety risk in healthcare. The project team developed the **Self-Identified Burnout survey (SIBO)** — categorizing respondents as *currently*, *formerly*, or *never* burned out — and the **Social Support and Personal Coping survey (SSPC)** to identify practices that contribute to resiliency. Two analytical questions drove the data science work:

1. Do free-text "hobby" responses (what providers do to recharge) fit the team's existing hobby categories, or do new categories emerge?
2. Can burnout status be predicted from survey features?

## Approach

**1. Data preparation** — ASRA and ASPAN survey data read in, cleaned, and joined; Likert-scale conversions applied to enable downstream modeling.

**2. NLP on free-text responses** — Free-text hobby responses embedded with **sentence-transformers**; **clustering** on the embedding space grouped responses into 20 clusters, validated against the checklist-based hobby categories.

**3. Burnout prediction** — Multiple ML algorithms (including **XGBoost regression**, with scikit-learn pipelines) predicted current-burnout status from survey features and embedding-derived signals.

## My Contributions

- **Cross-survey schema harmonization** — mapped and reconciled column structures between the ASRA and ASPAN survey instruments (type comparison, missing-column handling, checklist-item consolidation, target-variable recoding rules) to enable a joined analysis dataset.

## Tech Stack

`Python` · `sentence-transformers` · `scikit-learn` · `XGBoost` · `pandas` · `NumPy`

## Author

**I-Min (Steven) Chen** — Vanderbilt MSDS '27
[GitHub profile](https://github.com/iminstevenchen) · [LinkedIn](https://www.linkedin.com/in/i-min-chen/)

*Team project with the Vanderbilt Data Science Institute; original repository is private due to data restrictions.*
