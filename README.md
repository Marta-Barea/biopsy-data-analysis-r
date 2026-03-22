# Biopsy Data Analysis in R

## Overview

This repository contains the materials developed for the **Continuous Assessment Assignment 1 (PEC1)** of the course *Software for Data Analysis*, within the **Interuniversity Master's Degree in Bioinformatics and Biostatistics** offered by the *Universitat Oberta de Catalunya (UOC)* and the *Universitat de Barcelona (UB)*.

The objective of this work is to perform an **exploratory and statistical analysis** of the *Biopsy* dataset using the R programming language and the RStudio development environment. The project demonstrates fundamental data analysis workflows including data cleaning, transformation, visualization, and basic statistical modeling.

The analysis has been developed using **R Markdown**, allowing the integration of code, results, and explanations into a reproducible scientific report.

## Repository Structure

The repository is organized as follows:

* `data/`
  Contains the processed dataset used in the analysis.

* `images/`
  Stores figures or external images used in the report.

* `report/`
  Contains the R Markdown source file and the generated PDF report.

* `.gitignore`
  Specifies files that should not be tracked by Git.

## Main Technologies

* **R** — primary programming language used for the analysis
* **RStudio** — development environment
* **R Markdown** — reproducible report generation
* **LaTeX** — PDF rendering and document formatting

## Software Environment
The analysis was conducted using the following software environment:

* R: 4.5.2
* RStudio: 2026.1.1.403
* R Markdown: 2.30
* LaTeX (TinyTeX): TeX Live 2026

Main R packages used:

* ggplot2: 4.0.2
* dplyr: 1.2.0
* visdat: 0.6.0
* knitr: 1.51
* gridExtra: 2.3

## Contents of the Analysis

The report includes the following components:

1. Data import and preliminary exploration
2. Identification and handling of missing values
3. Data cleaning and transformation
4. Descriptive statistical analysis
5. Data visualization using `ggplot2`
6. Basic modeling and interpretation of relationships between variables

## Reproducibility

The full analysis can be reproduced by opening the `.Rmd` file located in the `report/` directory and knitting the document to PDF using RStudio.

## Author

Marta Barea Sepúlveda, PhD<br>
Interuniversity Master’s Degree in Bioinformatics and Biostatistics<br>
Universitat Oberta de Catalunya — Universitat de Barcelona
