# cais-mixed-methods-data-analysis-pipeline

**Data Analysis Pipeline for the CAIS Paper "Qualitative Research Meets AI: A Mixed-Methods Approach to Explaining Semi-Structured Decisions"**

This repository contains a self-contained Jupyter notebook implementing the data analysis pipeline proposed in the CAIS paper "Qualitative Research Meets AI: A Mixed-Methods Approach to Explaining Semi-Structured Decisions."

The notebook also contains all the results and figures reported in the paper.
________________________________________
**Overview**

The analysis pipeline is designed to address common data challenges inherent to mixed-methods research, including:
- High dimensionality
- Substantial missingness (where missingness may be informative rather than noise)
- (Quasi-)separation and instability in traditional statistical models
  
While the empirical application in the paper focuses on semi-structured decisions,  researchers working with mixed-methods datasets—regardless of research design or phenomenon of interest—can adapt this pipeline to their own data to generate rigorous, interpretable results and high-quality meta-inferences which goes beyond beyond purely correlational analysis.
________________________________________
**Pipeline Structure**

The notebook implements Phase 3 (data analysis strategy) of the mixed-methods design proposed in the paper, but the approach is general and can be applied to mixed-methods datasets across research designs and domains. 

*Phase 3 — Step 1: Training and Evaluating the Gradient Boosting Machine (GBM)*

Step 1 specifically includes:

-	Training a GBM model on the training data
-	Hyperparameter optimization via grid search with cross-validation
-	Calibration of the classification threshold using Youden’s J index
-	Evaluation of model performance on a holdout (previously unseen) test dataset

*Phase 3 — Step 2: Applying Explainable AI (XAI)*

Step 2 specifically includes:

-	Computing Shapley values for each observation in the holdout test data
-	Identifying the most influential factors driving model predictions
-	Explaining individual case-level predictions
-	Interpreting the global effects of key factors across the dataset

In the CAIS paper’s empirical context, these explanations are used to illustrate:

- The reasoning behind each specific decision
-	Decision-makers’ reasoning patterns across cases.
________________________________________
**Data Availability and Use**

The training and test datasets required to replicate the analyses, results, figures, and findings reported in the paper are publicly available via Harvard Dataverse at the following DOI:

https://doi.org/10.7910/DVN/WAWPJR

To run the notebook, download the training and test datasets from Dataverse and place them in the same directory as the notebook.
________________________________________
**Reproducibility**

The notebook is designed to run top-to-bottom and contains all code, outputs, and figures necessary to reproduce the analyses reported in the paper. Researchers interested in adapting the pipeline to other contexts can modify the input data and feature construction steps as needed.

For theoretical background, methodological justification, and interpretation of results, please refer to the CAIS paper.
