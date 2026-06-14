[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![R](https://img.shields.io/badge/R-Statistical_Analysis-276DC3?logo=r&logoColor=white)](https://www.r-project.org/)
[![R Markdown](https://img.shields.io/badge/R%20Markdown-Reproducible_Report-0B4F6C)](https://rmarkdown.rstudio.com/)
[![Report PDF](https://img.shields.io/badge/Report-PDF-1b5e20)](report/PEC1_analisis_biopsy.pdf)
[![Dataset](https://img.shields.io/badge/Dataset-CSV-b5651d)](data/biopsy_clean.csv)
[![MASS](https://img.shields.io/badge/MASS-CRAN-9c27b0)](https://cran.r-project.org/package=MASS)

# Biopsy Data Analysis in R

## Overview

This repository contains a reproducible R-based workflow for the exploratory and statistical analysis of the Biopsy dataset used in Continuous Assessment Assignment 1 (PEC1) for the course Software for Data Analysis, within the Interuniversity Master's Degree in Bioinformatics and Biostatistics offered by the Universitat Oberta de Catalunya and the Universitat de Barcelona.

The project is centered on the Biopsy dataset distributed with the MASS package and develops a complete analytical report in R Markdown. The workflow covers dataset import, variable renaming, missing-value inspection and cleaning, CSV export of the processed dataset, descriptive analysis, contingency analysis, hypothesis testing, data visualization, and linear modeling.

The analytical scope includes:

- loading the original biopsy dataset from MASS;
- recoding variable names to the format required by the assignment;
- identifying and removing missing values;
- exporting a cleaned dataset to CSV format;
- manipulating data structures and recoding categorical labels;
- computing descriptive statistics and contingency tables;
- assessing associations with a chi-squared test;
- producing publication-ready visualizations with ggplot2;
- fitting and evaluating a linear regression model.

## Repository Components

### Data Assets

The repository includes the cleaned dataset generated during the analysis.

- data/biopsy_clean.csv: cleaned CSV derived from the original biopsy dataset after removing incomplete observations and dropping the identifier column.

### Analytical Report

The main deliverable is an R Markdown report rendered to PDF with LaTeX customization.

- report/PEC1_analisis_biopsy.Rmd: end-to-end analytical document.
- report/PEC1_analisis_biopsy.pdf: rendered PDF report.
- report/preamble.tex: LaTeX header customizations used during PDF generation.
- report/PEC1_analisis_biopsy_files/: auxiliary figure artifacts produced by document rendering.

### Static Resources

- assets/images/: images used by the report.

## Project Structure

```text
.
├── assets/
│   └── images/                 # Figures and static visual assets
├── data/
│   └── biopsy_clean.csv        # Cleaned dataset exported during the analysis
├── report/
│   ├── PEC1_analisis_biopsy.Rmd
│   ├── PEC1_analisis_biopsy.pdf
│   ├── PEC1_analisis_biopsy_files/
│   └── preamble.tex
├── LICENSE
└── README.md
```

## Data Source

This workflow is based on the biopsy dataset available through the MASS package in R. The original dataset contains breast tissue biopsy observations and cellular features used for tumor classification. In this repository, the dataset is imported from MASS, renamed according to the PEC1 specification, cleaned by removing rows with missing values, and exported as a standalone CSV file for reuse.

## Main Outputs

The repository exposes the following main artifacts:

- cleaned dataset: data/biopsy_clean.csv;
- analytical source document: report/PEC1_analisis_biopsy.Rmd;
- rendered technical report: report/PEC1_analisis_biopsy.pdf.

## Requirements

The project is implemented in R and depends on CRAN packages inferred directly from the report source:

- MASS
- dplyr
- visdat
- ggplot2
- gridExtra
- knitr
- rmarkdown

A LaTeX installation is also required to build the PDF report. The current R Markdown configuration uses pdflatex through the standard pdf_document output.

## Setup

Clone the repository and install the required packages in your R environment.

```bash
git clone git@github.com:Marta-Barea/biopsy-data-analysis-r.git
cd biopsy-data-analysis-r
```

Example package installation in R:

```r
install.packages(c(
  "dplyr",
  "ggplot2",
  "gridExtra",
  "knitr",
  "MASS",
  "rmarkdown",
  "visdat"
), repos = "https://cloud.r-project.org")
```

## Reproducible Workflow

### 1. Open the analytical document

The complete workflow is defined in the R Markdown source file:

```text
report/PEC1_analisis_biopsy.Rmd
```

### 2. Render the report

From the repository root, render the report with:

```bash
Rscript -e "rmarkdown::render('report/PEC1_analisis_biopsy.Rmd', quiet = TRUE)"
```

This produces the PDF output at report/PEC1_analisis_biopsy.pdf.

### 3. Regenerate the cleaned dataset if needed

The report itself contains the code that:

- loads the biopsy dataset from MASS;
- removes incomplete rows with na.omit();
- drops the id column before export;
- writes the cleaned data to data/biopsy_clean.csv.

## Analytical Scope

The report covers the following technical tasks:

- import of the MASS biopsy dataset and renaming of variables;
- visual inspection and treatment of missing values;
- export of a cleaned CSV dataset for downstream reuse;
- construction and inspection of R list objects;
- recoding of class labels and conditional filtering of observations;
- descriptive statistics for selected variables;
- derivation of a categorical high_mitosis variable;
- contingency analysis between malignancy and mitosis level;
- chi-squared hypothesis testing;
- scatter plots, histograms, and boxplots with ggplot2;
- linear regression modeling and residual normality assessment.

## Notes on Reproducibility

- The repository already includes the cleaned CSV and the rendered PDF report.
- Rendering the report will regenerate figure artifacts inside report/PEC1_analisis_biopsy_files/.
- The .gitignore file excludes common R, RStudio, and knitr-generated temporary files.
- PDF generation requires a working LaTeX installation accessible from R.

## Access

- PDF report: [report/PEC1_analisis_biopsy.pdf](report/PEC1_analisis_biopsy.pdf)
- Cleaned dataset: [data/biopsy_clean.csv](data/biopsy_clean.csv)

## Author

Marta Barea Sepúlveda  
PhD  
Interuniversity Master's Degree in Bioinformatics and Biostatistics  
Universitat Oberta de Catalunya - Universitat de Barcelona

## License

This project is distributed under the GNU General Public License v3.0. See the LICENSE file for the full license text.
