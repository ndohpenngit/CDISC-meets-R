# Clinical Trial Analysis: SDTM to ADaM Pipeline

A full end-to-end CDISC-compliant clinical trial analysis pipeline built in R 
using the [pharmaverse](https://pharmaverse.org/) `admiral` package.

## 🔗 Live Report
👉 **[View the full rendered analysis here](https://ndohpenngit.github.io/CDISC-meets-R/)**

## Overview
This project demonstrates a production-ready ADaM dataset construction pipeline 
and regulatory-standard TLF generation for a Phase III clinical trial.

### ADaM Datasets Constructed
| Dataset | Description | Key Derivations |
|---------|-------------|-----------------|
| **ADSL** | Subject-Level Analysis | Treatment vars, population flags, study dates, age groups |
| **ADAE** | Adverse Events | TEAE flag, seriousness, severity grade, study day |
| **ADVS** | Vital Signs | Baseline, change from baseline, % change |

### Tables, Listings & Figures (TLFs)
- **Table 1** — Demographic & Baseline Characteristics
- **Table 2** — Treatment-Emergent Adverse Events by System Organ Class
- **Table 3** — SAE Seriousness & Severity Summary
- **Figure 1** — TEAE Incidence by SOC and Treatment Group
- **Figure 2** — Mean Change from Baseline in Systolic Blood Pressure
- **Figure 3** — Kaplan–Meier Time to First TEAE

## Tech Stack
- **R** + **Quarto**
- [`admiral`](https://pharmaverse.github.io/admiral/) — ADaM derivations
- [`haven`](https://haven.tidyverse.org/) — SAS `.xpt` read/write
- [`gtsummary`](https://www.danieldsjoberg.com/gtsummary/) — Clinical summary tables
- [`survival`](https://cran.r-project.org/package=survival) + [`survminer`](https://rpkgs.datanovia.com/survminer/) — Kaplan–Meier curves
- [`ggplot2`](https://ggplot2.tidyverse.org/) — Figures

## Project Structure
```
clinical-trial-adam/
├── clinical_trial_adam.qmd   # Full analysis source
├── index.html                # Rendered report (GitHub Pages)
├── R/
│   ├── derive_adsl.R
│   ├── derive_adae.R
│   └── derive_advs.R
└── data/                     # Not committed — patient data stays local
    ├── sdtm/
    └── adam/
```

## Standards Compliance
- CDISC ADaM Implementation Guide
- CDISC SDTM Implementation Guide  
- FDA Study Data Technical Conformance Guide
- Pharmaverse ecosystem

## Author
**Ndoh Penn**  
