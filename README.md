# Distinct human cervical tissue-adherent and luminal microbiome communities correlate with mucosal host gene expression and protein levels

## General info

This repository contains the code related to the article "Distinct human cervical tissue-adherent and luminal microbiome communities correlate with mucosal host gene expression and protein levels" [Edfeldt, Kaldhusdal et al (202X)](https://doi.org/)

This project used multiple datasets: 
  - Transcriptomics data (bulk mRNA-SEQ)
  - Microbiota data (16S)
  - Protein data (bead-based affinity assay)

The analysis can be reproduced by installing `conda` and running the individual rmarkdown scripts. The `WORKFLOW.md` file describes the input and output of each rmarkdown script. The raw counts for the microbiota and the transcriptomics data is downloaded from ENA and GEO respectively in the rmarkdown script named `03_normalize_data.Rmd`. The normalized MFI protein values is downloaded in `Figure_06.Rmd`.


## Data Availability Statement

The **raw microbiome sequencing data** for this study has been deposited in the European Nucleotide Archive (ENA) at EMBL-EBI under accession number PRJEB50325.

The **processed transcriptomics sequencing data** files can be accessed in the Gene Expression Omnibus public repository, accession ID GSE194276.

The **raw transcriptomic sequencing data** and sociodemographic and clinical characteristics of the study participants cannot be held in a public repository due to the sensitive nature of such personal data. Request for data access can be made to the Karolinska Institutet Research Data Office (contact via rdo\@ki.se), and access will be granted if the request meets the requirements of the data policy.

**Protein data** is previously published in doi: [10.1371/journal.ppat.1010494](https://doi.org/10.1371/journal.ppat.1010494.s017) \
**Cytokine data** is available upon request

## Dependencies

Project is created with:\
\* R version: 3.6.2\
\* RStudio version: 2022.07.1+554

## Setup

Conda

1.  Clone the repo
2.  If not already installed download mini conda/conda
3.  In the terminal navigate to the project directory
4.  create a new environment:<br/> `conda env create -n tissue_adherent_VMB -f ./resources/environment_tissue_adherent_VMB.yml`
5.  Activate the environment:<br/> `conda activate tissue_adherent_VMB`
6.  Open your preferred text editor from terminal by :<br/> `/path/to/rstudio &`
7.  Install niceRplots package from github:<br/> `remotes::install_github("czarnewski/niceRplots",force=T)`

## Repo structure

    project
    │   README.md
    │  
    └───code
    │   │   differential_abundance.R
    │   │   enrichment_function.R knit_function.R
    │   │   knit_function.R
    │   │   Picrust_pipe.sh
    └───data
    │ 
    └───reports
    │   │   00_Preprocessing.Rmd
    │   │   02_Analysis.Rmd
    │   │   ...
    │   └───manuscript
    │       │   Figure01.Rmd
    │       │   Figure02.Rmd
    │       │   ...
    └───resources
    │   └───KEGG_GO_database
    │   └───OptiVag_BVAB_database
    │   │   ...
    │ 


