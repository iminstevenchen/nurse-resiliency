# Nurse Resiliency — Burnout Risk Modeling

Analysis of burnout and resiliency in **6,000+ medical providers**, using national survey data and Vanderbilt University Medical Center (VUMC) datasets. Completed as a project at the Vanderbilt Data Science Institute.

> ⚠️ **No data or identifiable results are included in this repository.** The underlying datasets contain sensitive information about medical providers and cannot be shared. This repo documents the problem, approach, and methods.

## Problem

Provider burnout is a major driver of attrition and patient-safety risk in healthcare. The goal of this project was to (1) understand patterns of burnout and resiliency across provider populations and (2) build models that assess burnout risk so support resources can be targeted earlier.

## Approach

**1. Text representation** — Free-text survey responses were embedded with **sentence-transformers**, turning provider narratives into vectors that capture semantic similarity.

**2. Segmentation** — **Clustering** on the embedding space identified groups of providers with similar burnout/resiliency profiles.

**3. Risk modeling** — **XGBoost regression** (with scikit-learn pipelines for preprocessing, feature engineering, and validation) predicted burnout-risk scores from survey features and embedding-derived signals.

## Tech Stack

`Python` · `sentence-transformers` · `scikit-learn` · `XGBoost` · `pandas` · `NumPy`

## Author

**I-Min (Steven) Chen** — Vanderbilt MSDS '27
[GitHub profile](https://github.com/iminstevenchen) · [LinkedIn](https://www.linkedin.com/in/i-min-chen/)
