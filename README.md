# Valiation of the RSClin Clinical Risk Calculator within the National Cancer Data Base
A retrospective validation of the RSClin clinical risk calculator

## Attribution
If you use this code in your work or find it helpful, please consider citing our <a href='https://acsjournals.onlinelibrary.wiley.com/doi/10.1002/cncr.35163'>paper in Cancer</a>.
```
@article{vannier_validation_2023,
	title = {Validation of the {RSClin} risk calculator in the {National} {Cancer} {Data} {Base}},
	issn = {1097-0142},
	doi = {10.1002/cncr.35163},
	abstract = {BACKGROUND: Guidelines recommend the use of genomic assays such as OncotypeDx to aid in decisions regarding the use of chemotherapy for hormone receptor-positive, HER2-negative (HR+/HER2-) breast cancer. The RSClin prognostic tool integrates OncotypeDx and clinicopathologic features to predict distant recurrence and chemotherapy benefit, but further validation is needed before broad clinical adoption.
METHODS: This study included patients from the National Cancer Data Base (NCDB) who were diagnosed with stage I-III HR+/HER2- breast cancer from 2010 to 2020 and received adjuvant endocrine therapy with or without chemotherapy. RSClin-predicted chemotherapy benefit was stratified into low ({\textless}3\% reduction in distant recurrence), intermediate (3\%-5\%), and high ({\textgreater}5\%). Cox models were used to model mortality adjusted for age, comorbidity index, insurance, and race/ethnicity.
RESULTS: A total of 285,441 patients were identified for inclusion from the NCDB, with an average age of 60 years and a median follow-up of 58 months. Chemotherapy was associated with improved overall survival only for those predicted to have intermediate (adjusted hazard ratio [aHR], 0.68; 95\% confidence interval [CI], 0.60-0.79) and high benefit per RSClin (aHR, 0.66; 95\% CI, 0.61-0.72). Consistent benefit was seen in the subset with a low OncotypeDx score ({\textless}26) and intermediate (aHR, 0.66; 95\% CI, 0.53-0.82) or high (aHR, 0.71; 95\% CI, 0.58-0.86) RSClin-predicted benefit. No survival benefit with chemotherapy was seen in patients with a high OncotypeDx score (≥26) and low benefit per RSClin (aHR, 1.70; 95\% CI, 0.41-6.99).
CONCLUSIONS: RSClin may identify high-risk patients who benefit from treatment intensification more accurately than OncotypeDx, and further prospective study is needed.},
	language = {eng},
	journal = {Cancer},
	author = {Vannier, Augustin G. L. and Dhungana, Asim and Zhao, Fangyuan and Chen, Nan and Shubeck, Sarah and Hahn, Olwen M. and Nanda, Rita and Jaskowiak, Nora T. and Fleming, Gini F. and Olopade, Olufunmilayo I. and Pearson, Alexander T. and Huo, Dezheng and Howard, Frederick M.},
	month = dec,
	year = {2023},
	pmid = {38146744},
	keywords = {breast neoplasms, aromatase inhibitors, chemotherapy, clinical decision-making, gene expression profiling, hormone antagonists, precision medicine},
}
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


