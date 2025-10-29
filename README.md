# Comprehensive genetic screening in Parkinson’s disease: NeuroBooster array insights from a South African cohort

`GP2 ❤️ Open Science 😍`

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17478293.svg)](https://doi.org/10.5281/zenodo.17478293) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Last updated:** October 2025

## Summary

This repository contains the code, data workflows, and results associated with the manuscript titled **“Comprehensive genetic screening in Parkinson’s disease: NeuroBooster array insights from a South African cohort”**.

This study looks at the pathogenic screening for variants and copy number variations (CNVs) in the South African Study Collection using NeuroBooster array data. 

## Data statement
The data was obtained from the Global Parkinson’s Genetics Program (GP2) release 7 (GP2 release 7, [10.5281/zenodo.10962119](https://doi.org/10.5281/zenodo.10962119)) and access can be requested through the Accelerating Medicines Partnership in Parkinson’s Disease (AMP-PD) via the online application process (https://www.amp-pd.org/).

All GP2 data are hosted in collaboration with the Accelerating Medicines Partnership in Parkinson’s disease, and are available via application on the website (https://amp-pd.org/register-for-amp-pd). For up-to-date information on GP2 data acquisition, access, and policies, visit https://gp2.org/. Tier 1 data can be accessed by completing a form on the Accelerating Medicines Partnership in Parkinson’s Disease (AMP®-PD) website (https://amp-pd.org/register-for-amp-pd). Tier 2 data access requires approval and a Data Use Agreement signed by your institution.

### Helpful Links

- [GP2 Website](https://gp2.org/)
  - [GP2 Cohort Dashboard](https://gp2.org/cohort-dashboard-advanced/)
- [Introduction to GP2](https://movementdisorders.onlinelibrary.wiley.com/doi/10.1002/mds.28494)
  - [Other GP2 Manuscripts (PubMed)](https://pubmed.ncbi.nlm.nih.gov/?term=%22global+parkinson%27s+genetics+program%22)

## Citation
*(pending publication)*
> Cite your manuscript in APA style here.

## Key analyses
* Quality control, file preparation, and pathogenic variant analysis.  
* CNV analysis using CNV-Finder as previously described (https://github.com/GP2code/CNV-Finder). 

## Repository Orientation
- The `analysis/` directory includes all analyses discussed in the manuscript.

<pre> THIS_REPO/ 
  ├── analysis/ 
  |     └── pathogenic_screening.sh
  ├── LICENSE
  └── README.md 
</pre>

## Analysis Notebooks
### Languages: Python, bash, and R
| Directory | Notebooks   | Description | 
|-----------|----------------|--------|
|`analysis/`| `pathogenic_screening.sh`         | The script named ```pathogenic_screening.sh``` is essential as it defines all tools, input/output directories, and parameters at the top, allowing changes there only without altering the core code. It performs key steps: data quality control, a Python script to verify correct reference and alternative alleles, variant annotation using ANNOVAR with hg38 databases, and variant filtering based on Parkinson's disease phenotype with prioritization using in-silico prediction tools in R.|



## Software
| **Software** | **Version(s)** | **Resource URL** | **RRID** | **Notes** |
|--------------|----------------|------------------|----------|-----------|
|Python Programming Language|3.14|http://www.python.org/|RRID:SCR_008394|The Python script resolves any leftover reference and alternative allele issues since PLINK can sometimes incorrectly swap these alleles when switching between pfile and bfile|
|PLINK|v.1.9,v. 2.0|http://www.nitrc.org/projects/plink|RRID:SCR_001757|Used for quality control and file preparation.|
|R Project for Statistical Computing|v.4.4|http://www.r-project.org/|RRID:SCR_001905|R was used to filter variants based on PD phenotypes and then prioritize them using in-silico prediction tools.|
|ANNOVAR|06.08.2020|http://www.openbioinformatics.org/annovar/|RRID:SCR_012821|The process of adding information about a variant or a gene to allow for the interpretation process. The more information available, the better equipped we are to interpret the potential impact of a variant.|
