# SomaticLike-ML

## Introduction
This was a project to produce a machine-learning model to identify somatic cell contamination in sperm methylation data. 
This final product is hosted here: https://github.com/jenkins-lab-byu/Somatic_Cell_QC_Pipeline/tree/main/Somatic_Cell_ML_Pipeline

## Feature Identification
~1000 differentially methylated were selected from a USEQ sliding window analysis on our training set. I generated mean beta values at each of these regions for each sample, 
and plotted them on a clustermap.

![SLSFig4 2](https://github.com/carternorton11/SomaticLike-ML/assets/99043737/d78570df-92e8-4dbe-8024-365ba164a26f)

## Binarization
I established a cutoff for hyper/hypomethylation using mean methylation values from sperm samples in our training set. All samples were then assigned a "0" or "1" at each region,
depending on methylation value. 


