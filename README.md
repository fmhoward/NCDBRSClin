# Valiation of the RSClin Clinical Risk Calculator within the National Cancer Data Base
A retrospective validation of the RSClin clinical risk calculator

## Attribution
If you use this code in your work or find it helpful, please consider citing our<a href='https://doi.org/10.1200/JCO.2021.39.15_suppl.549'>ASCO abstract</a> (paper forthcoming).
```
@article{doi:10.1200/JCO.2021.39.15\_suppl.549,
author = {Howard, Frederick and Pearson, Alexander T. and Nanda, Rita and Olopade, Olufunmilayo I. and Huo, Dezheng},
title = {Validation of the RSClin risk calculator using the National Cancer Database (NCDB).},
journal = {Journal of Clinical Oncology},
volume = {39},
number = {15\_suppl},
pages = {549-549},
year = {2021},
doi = {10.1200/JCO.2021.39.15\_suppl.549},
URL = {https://doi.org/10.1200/JCO.2021.39.15_suppl.549},
eprint = {https://doi.org/10.1200/JCO.2021.39.15_suppl.549}
```

## Installation
The associated Jupyter notebook can be downloaded and all relevant code is provided within the notebook.

Requirements:
* python 3.8.8
* pandas 1.0.5
* numpy 1.19.0
* tableone 0.7.10
* lifelines 0.26.3

## Overview
The notebook is divided into sections to replicate all components of our paper.

The first section entitled 'Downloading RSClin Scores' details downloading RSClin scores in bulk to get associated scores for all patients within the National Cancer Data Base. This requires a Genomic Health account. After logging into Genomic Health and accessing the risk calculator, you will need to update the JSESSIONID in the code. JSESSIONID can be <a href="https://kb.blackbaud.com/knowledgebase/Article/66671">found through browser developer tools</a>. 

The second section entitled 'Data Loading from NCDB' allows for selection of the relevant patient cohort used in the from an NCDB csv data file. 

The third section, 'Distribution of RSClin Predictions', provides plots of the cumulative density function of RSClin predictions for recurrence risk on aromatase inhbitor and for chemotherapy benefit.

The fourth section, 'Prognostic Value of RSClin Predictions', provides plots for survival stratified by RSClin predicted recurrence risk in hormonal treated patients, as well as comparative plots of survival for hormonal versus chemotherapy, stratified by RSClin predicted chemotherapy benefit.

The fifth section, 'Restricted Cubic Spline Regression', was used to generate continuous plots of the hazard ratio for chemotherapy as a function of predicted chemotherapy benefit.

Finally, the sixth section, 'Subgroup Analysis', was used to generate the forest plot for hazard ratios of chemotherapy for various clinical / demographic subgroups.


