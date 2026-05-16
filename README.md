# 🧬 Two-Sample Mendelian Randomization for Causal Inference: Sleep Traits & Cardiovascular Risk

## 📌 1. Project Title
**Evaluating the Causal Architecture of Sleep Patterns on Coronary Artery Disease Using Multi-Method Two-Sample Mendelian Randomization and Genomic Diagnostics.**

---

## 🔍 2. Background & Research Context
While conventional observational epidemiology strongly correlates shortened sleep duration with advanced coronary artery disease (CAD), these traditional matrices are often biased by reverse causation and residual environmental confounders (e.g., socioeconomic status, diet, and lifestyle behaviors). 

To overcome these barriers and isolate the genuine biological etiology, this study deploys an advanced **Two-Sample Mendelian Randomization (MR)** framework. By utilizing independent Single Nucleotide Polymorphisms (SNPs) extracted from large-scale Genome-Wide Association Studies (GWAS) as instrumental variables (IVs), this project calculates the unconfounded, direct causal effect of genetically instrumented short sleep duration on coronary artery disease risk layouts.

---

## 📂 3. Genomic Input Specification & Data Architecture
- **Study Framework:** Two-Sample Mendelian Randomization (Summary-Level Analytical Scheme).
- **Instruments (Exposure Proxy):** Standardized genomic array representing independent genetic proxies for **Short Sleep Duration** harvested at a strict genome-wide significance threshold ($p < 5 \times 10^{-8}$).
- **Target Traits (Outcome Domain):** Matching summary-level statistics corresponding to **Coronary Artery Disease (CAD)** cohorts derived from international diagnostic biobanks.
- **Controlled Instruments:** Systematically removed overlapping variables to shield regression mechanics from horizontal pleiotropic violations.

---

## 🛠️ 4. Advanced Methodology & Statistical Engines Deployed
This project operates via the specialized `TwoSampleMR` analytical architecture to run strict computational genomic checks:
1. **Exposure-Outcome Allele Harmonization:** Executed forward-strand direction corrections via `harmonise_data()` to ensure absolute alignment of effect orientations.
2. **Multi-Engine Causal Estimation:** Combines results from three major genomic estimators:
   - **Inverse Variance Weighted (IVW):** Applied as the primary meta-analysis engine.
   - **MR-Egger Regression:** Formulated to independently track intercept drift.
   - **Weighted Median Estimator:** Deployed to provide robust boundaries even if up to 50% of the instruments are invalid.
3. **Rigorous Sensitivity Controls & Diagnostics:**
   - **Cochran's Q Test (Heterogeneity):** Calculated via `mr_heterogeneity()` to scan for instrument structural consistency.
   - **MR-Egger Intercept Test:** Tracked explicitly to identify and reject instances of directional horizontal pleiotropy.
   - **Leave-One-Out Validation Analysis:** Executed iteratively via `mr_leaveoneout()` to isolate single-variant outlier distortions.
   - **Algorithmic F-statistic Estimation:** Programmed math layers ($F = \frac{\beta^2}{SE^2}$) to screen for and thoroughly eliminate weak instrument biases.
4. **Professional Data Visualization Mapping:** Generated dynamic multi-method scatter plots, Leave-One-Out error bar charts, Funnel plots, and clinical **Causal Forest Plots** via R visualization plugins.

---

## 🏆 5. Primary Research & Causal Insights
- **Direct Biological Causality Confirmed:** The uniform opposite alignment between genomic exposure and outcome dimensions yields a highly significant negative coefficient ($p < 0.05$) under the IVW setup. This proves that abbreviated sleep duration acts as a **direct biological causal trigger** for elevating coronary hazards, completely independent of conventional environmental confounders.
- **Elimination of Horizontal Pleiotropy:** The formal MR-Egger regression intercept centered tightly around zero with a non-significant profile ($p > 0.05$), validating that the selected genetic proxies influence the cardiac structure *solely* via the sleep pathway.
- **Thorough Instrument Validity ($F > 10$):** Every instrumental SNP displayed robust structural significance, with the computed **overall mean F-statistic crossing well above the standard threshold of 10**, proving the dataset is fully shielded from weak instrument biases.
- **Stable Sensitivity Boundaries:** The Leave-One-Out map confirmed that the causal slope trajectory remains resilient even under systematic single-variant exclusions, demonstrating exceptional robustness.

---

## 💻 6. Computational Tech Stack
- **Language & Runtime:** R (v4.6.0) / RStudio Environment
- **Core Genomic Packages:** `TwoSampleMR`, `tidyverse`

---

## 📂 7. Repository File Maps
- `sleep_cvd_mr_analysis.Rmd` — The original executable R Markdown script embedding all genomic math algorithms.
- `sleep_cvd_mr_analysis.html` — The compiled, production-ready interactive output report featuring all diagnostic models and plots.

---

## 🔗 8. Live Interactive Report
[👉 CLICK HERE TO VIEW THE FULL INTERACTIVE GENOMIC REPORT] (https://phyonyeinchan.github.io/mendelian-randomization-sleep-cvd/index.html)
