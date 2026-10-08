# ALA Editions & ACRL Digital Catalog Marketing Analysis

## Table of Contents

- [ALA Editions & ACRL Digital Catalog Marketing Analysis](#ala-editions-acrl-digital-catalog-marketing-analysis)
  - [Project Overview](#project-overview)
  - [Datasets](#datasets)
  - [Notebooks](#notebooks)
    - [Main Analysis Notebooks](#main-analysis-notebooks)
  - [Key Findings](#key-findings)
    - [ALA Email Strategy](#ala-email-strategy)
    - [ACRL Email Strategy](#acrl-email-strategy)
    - [Strategic Implications](#strategic-implications)
  - [File Structure](#file-structure)
  - [Technical Requirements](#technical-requirements)
    - [Python Libraries](#python-libraries)
    - [Environment Setup](#environment-setup)
- [Create virtual environment](#create-virtual-environment)
- [Activate virtual environment](#activate-virtual-environment)
- [Install dependencies](#install-dependencies)
    - [Running the Notebooks](#running-the-notebooks)
  - [Visualization Elements](#visualization-elements)
  - [Contact & Documentation](#contact-documentation)
  - [Project Status](#project-status)

---

# ALA Editions & ACRL Digital Catalog Marketing Analysis
**UMSI Alternative Spring Break Project — ALA Marketing Department**

This project analyzes four datasets to produce observations and e-blast strategy recommendations for:
1. The Spring/Summer 2026 ALA Editions catalog launch
2. A unified Fall/Winter 2027 catalog integrating ALA Editions + ACRL titles

---

## Project Overview
This analysis combines Google Analytics traffic data with e-blast marketing performance metrics to identify patterns in user engagement, content effectiveness, and optimal marketing strategies for ALA and ACRL digital catalogs. The project explores how catalog attributes (body text length, subject line characteristics, send timing, etc.) correlate with open rates, click rates, and unsubscribe behavior.

[Link to Deepnote Environment to run code](https://deepnote.com/workspace/quworkspace-66ecfcba-a684-413d-a464-124bf06d729f/project/AASL-ALA-Marketing-1-3b33a8df-90ac-4d91-8716-a62b1fa405f5/notebook/READMEmd-faf5ea15de8645d9bcb88b9825ef7819?utm_source=share-modal&utm_medium=product-shared-content&utm_campaign=notebook&utm_content=3b33a8df-90ac-4d91-8716-a62b1fa405f5)

---

## Datasets

| Dataset | Source | Description |
|---|---|---|
| `editions_ss25_google` | Google Analytics (CSV) | Weekly traffic: SS25 ALA Editions catalog |
| `editions_fw26_google` | Google Analytics (CSV) | Weekly traffic: FW26 ALA Editions catalog |
| `editions_ala_stats` | Informz (via PDF) | E-blast performance: ALA Editions catalog promos |
| `editions_eblasts` | Informz (via PDF) | E-blast metadata: ALA Editions campaigns |
| `acrl_google` | Google Analytics (CSV) | Traffic: ACRL Publications catalog |
| `acrl_indiv_emails` | Informz (via PDF) | E-blast performance: Individual ACRL book promos |
| `acrl_syllabus` | Informz (via PDF) | E-blast performance: ACRL Syllabus newsletters |

**Note:** Due to PDF conversion errors, the PDF source files may show overlapping code and images. The best way to view these notebooks and visualizations is to run them in a code development environment.

---

## Notebooks

### Main Analysis Notebooks
1. **Notebook #0: Column Definitions**
   - Reference guide for all dataset columns and variables
   - Data schema and terminology

2. **Notebook #2a: ALA Exploratory Data Analysis**
   - ALA Editions traffic and engagement analysis
   - Email body length vs. engagement correlation
   - TF-IDF text analysis of email body content
   - Open/click rate distributions

3. **Notebook #2b: ACRL Exploratory Data Analysis**
   - ACRL Publications catalog traffic analysis
   - Individual book promo performance
   - Syllabus newsletter engagement patterns
   - TF-IDF text analysis of ACRL body content

4. **Notebook #2c: ALA & ACRL Comparisons**
   - Side-by-side comparison of both organizations
   - Traffic volume comparisons
   - Content strategy differences
   - Audience engagement patterns

5. **Notebook #4: Recommendations**
   - Strategic insights and recommendations
   - ACRL individual book promo analysis
   - Optimal send timing and content strategies
   - Unified catalog recommendations

---

## Key Findings

### ALA Email Strategy
- Emphasizes promotional language ("book", "new", "free", "library")
- Highlights practical benefits and accessibility
- Consumer-oriented approach targeting broad audiences
- Email body length shows weak correlation with open rates

### ACRL Email Strategy
- Centers on academic and research-oriented terms ("research", "library", "book", "information")
- Includes professional development keywords ("conference", "session", "professional")
- Targets specialized academic audiences
- Distinct content focus from ALA's marketing approach

### Strategic Implications
- Both organizations use "book" and "library" as core terms but diverge in secondary messaging
- Content strategy should align with target audience expectations and organizational mission
- Timing and frequency of sends impact overall engagement
- Day-of-week effects on open and click rates vary by audience

---

## File Structure

```
ALA Marketing Project/
├── README.md                           # This file
├── Notebook #0_ Column Definitions.ipynb
├── Notebook #2a_ ALA EDA.ipynb
├── Notebook #2b_ ACRL EDA.ipynb
├── Notebook #2c_ ALA & ACRL Comparisons.ipynb
├── Notebook #4_ Recommendations.ipynb
└── Cleaned Datasets/
    ├── acrl_all_emails
    ├── acrl_google
    ├── acrl_indiv_emails
    ├── acrl_syllabus
    ├── editions_ala_eblasts.parquet
    ├── editions_ala_fw26_google.parquet
    ├── editions_ala_ss25_google.parquet
    └── editions_ala_stats_eblasts
```

---

## Technical Requirements

### Python Libraries
- `pandas` — Data manipulation and analysis
- `numpy` — Numerical operations
- `plotly` — Interactive visualizations
- `matplotlib` & `seaborn` — Static plotting
- `scikit-learn` — TF-IDF vectorization and text analysis
- `statsmodels` — LOWESS smoothing for trend analysis

### Environment Setup
```bash
# Create virtual environment
python3 -m venv .venv

# Activate virtual environment
source .venv/bin/activate

# Install dependencies
pip install pandas numpy plotly matplotlib seaborn scikit-learn statsmodels
```

### Running the Notebooks
1. Ensure the virtual environment is activated
2. Open any notebook in a Jupyter-compatible environment (JupyterLab, VS Code, etc.)
3. Run cells sequentially from top to bottom
4. Visualizations will render inline

---

## Visualization Elements

All notebooks employ consistent styling:
- **Colors:**
  - ALA Blue: `#003F72`
  - ALA Red: `#C8102E`
  - ACRL Teal: `#00857C`
  - Accent Gold: `#F5A623`
  - Light Gray Background: `#F4F4F4`

- **Chart Types:**
  - Time-series line plots with LOWESS trends
  - Scatter plots with trendlines
  - Horizontal bar charts for TF-IDF analysis
  - Boxplots for engagement distributions
  - Subplot comparisons for side-by-side analysis

---

## Contact & Documentation

For questions or additional analysis requests, contact Luciana Qu or Taylor Whipple at the University of Michigan via email.

---

## Project Status

✅ **Complete** — All notebooks have been analyzed and key findings documented. Ready for strategic implementation.

Last Updated: March 2026

