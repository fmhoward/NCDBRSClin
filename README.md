# Valiation of the RSClin Clinical Risk Calculator within the National Cancer Data Base
A retrospective validation of the RSClin clinical risk calculator

## Attribution
If you use this code in your work or find it helpful, please consider citing our<a href='doi:10.1200/JCO.2021.39.15\_suppl.549'>ASCO abstract</a> (paper forthcoming).
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

URL = { 
        https://doi.org/10.1200/JCO.2021.39.15_suppl.549
    
},
eprint = { 
        https://doi.org/10.1200/JCO.2021.39.15_suppl.549
    
}
```

## Installation
The associated Jupyter notebook can be downloaded and all relevant code is provided within the notebook.

Requirements:
* python 3.8.5
* pandas 1.0.5
* numpy 1.19.0
* pymatch 0.3.4
* tableone 0.7.10
* lifelines 0.26.3

## Overview
The notebook is divided into sections to replicate all components of our paper.
The first section entitled 'Downloading RSClin Scores' details downloading RSClin scores in bulk to get associated scores for all patients within the National Cancer Data Base
The second section entitled 'Data Loading from NCDB' allows for selection of the relevant patient cohort from an NCDB csv data file
The third section, 'Distribution of RSClin Predictions', provides plots of the cumulative density function of RSClin predicted 
