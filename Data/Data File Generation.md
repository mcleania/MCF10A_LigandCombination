# Data File Generation

The following text briefly describes the data files used for the analyses in this repository. Raw live-cell images of MCF10A cells treated with ligands are deposited on Zenodo 10.5281/zenodo.14261795. RNA sequencing data can be accessed from the Gene Expression Omnibus: GSE282654. For a full description of the tools and methods used to generate intermediate files in this repository, please reference the Star Methods section at https://doi.org/10.1101/2025.04.03.647095. .

## File Descriptions

##### LiveCellTracking_Data
-Tracking data generated from live cell imaging. Raw data is available Zenodo 10.5281/zenodo.14261795.
-Stacks were registered using FIJI, segmented using CellPose, then tracked using Baxter Algorithm.
-Tracking data is used as input to LiveCellPhenotype_Quantification_Figure1.Rmd and CREBExperimentalAnalysis_Figure6.Rmd
##### PLSR_VIP_Scores
- Genes ranked and scored based on their importance in PLSR models used to predict the indicated phenotypes.
- Files were generated using PLSRAnalysis_Figure4.Rmd. 
##### Phenotypic_Metrics
- Replicate summarized phenotypic metrics derived from live cell imaging.
- Metrics were calculated using LiveCellPhenotype_Quantification_Figure1.Rmd and serve as input into the PLSR models constructed using PLSRAnalysis_Figure4.Rmd. 
##### Priori_TF_Scores
- Transcription factor enrichment scores calculated using bulk RNAseq TPM scores as input.
- Transcription factor scores are analyzed and plotted using RNAseqAnalysis_Figure2.Rmd.
##### RNAseq_DGE_Files
- Differential gene expression files comparing across multiple controls and conditions.
- DGE analyses were conducted using RNA-seq gene-level summaries with the R package DESeq2.
- These files serve as input into both RNAseqAnalysis_Figure2.Rmd and RNAseqSynergyAnalysis_Figure3.Rmd.
##### RNAseq_Supp_Files
- This directory contains files supporting the analysis and validation of PLSR models
- MDD_ligandCombination_RNAseq_log2TPM_allGenes.csv contains Log2 normalized expression from ligand combination conditions.
- JWGray_BCCL_rnaseq_matrix_v3_tatlowGeneAbundance.csv contains RNAseq data from https://doi.org/10.1073/pnas.1018854108. The data was reprocessed to conform with current standards and the experimental RNAseq data.
- Migration_BCCL.csv and Proliferation_BCCL.csv contain migration estimates and proliferation rates of cancer cell lines. The data is from https://doi.org/10.1073/pnas.1018854108 and https://doi.org/10.1038/s41598-019-47440-w
