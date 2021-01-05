# Prediction of Drug Consumption Based on Five Factor Personality Features

## Abstract

In this report, we performed binary classification of users and non-users based on the *Drug Consumption (Quantified)* data set published by (Fehrman et al. 2015). This classification can be used to assess the risk of an individual being a user of a specific drug based on personality features. After an exploratory data analysis (EDA), we decided on three drugs and four different classes of models for evaluation.

The best performance was achieved using regularized discriminant analysis (RDA) models: We report balanced accuracies of 66.5%, 79.2% and 73.2% for the drugs Benzodiazepines, Legal Highs and Ecstasy, respectively. The RDA model outperforms the results reported by (Mahyoub et al. 2019) and performs slightly worse than the highly optimized decision trees of (Fehrman et al. 2015).

A potential improvement is demonstrated by experimental results when using additional input features exploiting drug correlation. Further improvements are expected by using an optimal input feature sub-set for each drug as well as a more sophisticated tune grid for the used model types.

## Details

Author: Eric Gabriel
Date: January 5th, 2021

This repository contains the second project submission of the course *HarvardX PH125.9x "Data Science: Capstone"*.

The data set file was already downloaded from <https://archive.ics.uci.edu/ml/machine-learning-databases/00373/drug_consumption.data> on December 22nd, 2020, and was saved to the "data" sub-directory.

The R script loads the downloaded CSV data file and performs cleaning and pre-processing of the data. Additionally, a data frame for exploring the correlation of user/non-user groups per drug is created.

After an exploratory data analysis (EDA), three drugs are chosen for evaluation based on the minimum difference between the amount of users and non-users: Benzodiazepines, Legal Highs and Ecstasy.

For each of these drugs, four types of models for binary classification into users and non-users are created using a 10-fold cross-validation:

* Boosted Generalized Linear Models (Boosted GLM)
* k-Nearest-Neighbor Classification (kNN)
* Random Forest (RF)
* Regularized Discrimininant Analysis (RDA)

For each of the evaluated drugs, the results are reported and compared to the published results of (Fehrman et al. 2015) and (Mahyoub et al. 2019).

Finally, the impact of additional input features on the classification performance is evaluated using user information of the two most correlated drugs.

The corresponding PDF report contains further details about the data set, the analysis procedure, the model theories and the results. The report can be generated by knitting the Rmd file.  

## References

Fehrman, E., A. K. Muhammad, E. M. Mirkes, V. Egan, and A. N. Gorban. 2015. “The Five Factor Model
of Personality and Evaluation of Drug Consumption Risk.” Data Science. <https://arxiv.org/abs/1506.06297>.

Mahyoub, Mohammed A., Alaith Abu Lekham, Emad Alenany, Lubna Tarawneh, and Daehan Won. 2019.
“Analysis of Drug Consumption Data Using Data Mining Techniques and a Predictive Model Using Multi-Label Classification.” *Proceedings of the IISE Annual Conference*.
