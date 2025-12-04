Mediational g-formula Analysis Code
This repository contains the R code used to estimate interventional direct and indirect effects in the study: Narita et al., “Mediators of girls’ higher prevalence of internalizing problems: the role of loneliness, thin-ideal internalization, and gender-related stressors.” The code implements the parametric mediational g-formula and reproduces all quantitative results reported in the manuscript.

File organization
This package is organized as follows:

run_analysis.R : main analysis script to reproduce the manuscript results

helper_functions.R : supporting functions used by the main script

demo/demo_gformula.R : demo script using simulated data

example_data/example_simulated_data.rds : example dataset for the demo

output/ : directory where analysis results are saved (created automatically if not present)

System Requirements
Software:

R version: 4.5.1 or higher

Required R packages: tidyverse (≥1.3.0), mice (≥3.14.0), boot (≥1.3), data.table (≥1.14), MASS (≥7.3), and any additional packages used in the actual analysis scripts.
Operating systems tested: macOS (Sonoma), Windows 10/11, Ubuntu Linux 22.04 LTS
Hardware requirements: no non-standard hardware required; runs on a standard desktop or laptop computer.

Installation Guide
Install R (version 4.5.1 or higher).
Install required packages using: install.packages(c("tidyverse","mice","boot","data.table","MASS"))
Download or clone this repository using: git clone https://github.com/ZuiCNarita/Mediational-g-formula.git

Ensure all .R files remain in the same directory.
Typical installation time is less than 2 minutes on a standard desktop computer.

Demo Instructions
A simple demonstration using simulated data is included in demo/demo_gformula.R and example_data/example_simulated_data.rds.
To run the demo, start R in the repository directory and execute: source("demo/demo_gformula.R")
Expected output includes estimated interventional direct and indirect effects, bootstrap-based confidence intervals, and diagnostic summaries printed to the console.
The expected run time for the demo is approximately 30–60 seconds on a standard desktop computer.

Instructions for Use (Real Data)
To run the mediational g-formula on real data, prepare a dataset including: exposure (sex assigned at birth), mediators (loneliness, thin-ideal internalization, gender-related stressors), outcomes (depression, suicidal ideation, self-harm, anxiety), and confounders assessed at age 12 (as listed in the manuscript).
Modify file paths and dataset names in run_analysis.R as appropriate for your environment.
Run the analysis by starting R in the repository directory and executing: source("run_analysis.R")
Outputs include the total effect, interventional direct effect, interventional indirect effect, proportion mediated, and bootstrap confidence intervals (4,000 samples across imputations).
Results are automatically saved in the output directory.

Reproduction Instructions (Recommended)
To reproduce all results reported in the manuscript, run: source("run_analysis.R")
This script loads multiply imputed datasets, fits mediator and outcome models, implements the parametric mediational g-formula, computes interventional effects for all outcomes, and recreates the main quantitative tables (for example, Tables 2 and 3 in the manuscript).

License
This code is released under the MIT License, an Open Source Initiative–approved license. Users may freely use, modify, and distribute the code with appropriate attribution.

Contact
For questions related to this software, please contact:
Zui C. Narita (zuinarita@ncnp.go.jp
)
GitHub: https://github.com/ZuiCNarita
