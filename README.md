# Toxic-Comment-Binary-Classification
## Introduction
This project is part of the Toxic Comment Classification Kaggle Challenge undertaken as part of Deep Learning coursework in final year DSBA, that addresses the critical issue of toxic comments in online platforms. Our solution aims to effectively identify toxic comments and reduce biases associated with specific demographic identities.

## Overview
Welcome to the Toxic comment classification challenge! Automated assessment of user-generated text, such as identifying toxic comments, serves as a crucial tool for managing the vast volume of online content. Regrettably, previous studies have revealed that these classifiers for toxicity often inherit biases from their training data.
The challenge is cast as a subpopulation shift problem. where distinct demographic identities represent these subpopulations. Our aim is to achieve high performance across all these subpopulations, rather than only focusing on the average performance across them. The emphasis is on reducing biases related to comments referencing specific demographic groups, rather than comments authored by individuals from those particular demographics.

## Description
This competition aims to revolutionise the landscape of comment classification within online discourse. Participants will dive into the task of determining the toxicity of comments posted on various online articles. The ultimate goal is to build models that not only accurately identify toxic comments but also demonstrate robustness across diverse demographic subpopulations. The primary objective of this challenge is to develop innovative solutions that mitigate biases inherent in comments mentioning specific demographic identities. Participants are tasked with crafting models that excel in fairness and accuracy across these demographic subpopulations, aiming for superior performance beyond mere overall averages.

## Source of Data: 
You can download the train and test data in csv format here - https://www.kaggle.com/competitions/toxic-comment-classification-dsba-2023-2/overview

## Evaluation
Submissions are evaluated on the Worst-group accuracy. To study the bias of annotating comments that mentions demographic groups as toxic, the models performance will be evaluated by
1) Each of the 8 demographic identities will be separated into 2 groups by toxicity – for example, separate black into black, toxic and black, not toxic;
2) Measure the accuracies of these 8 × 2 = 16 groups and use the lowest accuracy as the final evaluation of the model.
This metric consists of calculating both the sensitivity and specificity of the classifier across each demographic identity, and then highlighting the lower metric among the two across all domains. Strong performance on the group with the lowest accuracy suggests that the model refrains from relying on demographic identity as an indicator of toxic comments.

## Submission File
For each ID in the test set, you must predict a probability for the pred variable. It is very important for the file to have the correct format, and to pay attention to the ID of the prediction (see baseline notebook). The file should contain a header and have the following format:
ID, pred
2,0
5,0

## Methodology
At stage 1, we explored diverse models to cover a broad spectrum of NLP methodologies. While traditional methods like Logistic Regression offer baseline insights, advanced models like BERT, RoBERTa, DistilBERT, and LSTM bring sophisticated neural network capabilities to tackle the complexity of natural language in online comments. This diverse 
selection helped in identifying the most effective approach for the specific challenges presented by the dataset.. We utilized Python and tools like Colab for our analyses.

## Results
In selecting BERT From Stage 1 for further fine-tuning, we were guided by its superior performance in capturing bidirectional context, a crucial aspect for accurately classifying the nuanced and context-dependent nature of online comments. BERT's robust pre-training on a diverse language corpus made it a prime candidate for adaptation to our specific dataset.The finalfine tuned BERT ensembled with its different variation achieved an WGA of 0.793 on the public kaggle leaderboard and then 0.810 private leaderboard, at 7th position amongst 61 teams.

## Files in this repository
1. train_x.csv - File containing the dataset to be used for training your model
2. train_y - File containing the target labels
3. val_x - File containing the dataset to be used for validating your model
4. val_y - File containing the target labels at the stage of validation
5. test_x.csv - File containing the dataset on which predictions were required to be submitted on Kaggle
7. kaggle_baseline.ipynb - Python file containing the baseline code that can be used to prepare the pipeline for modeling
8. FDL_Code_2_EDA.ipynb - Python file containing Exploratory Data Analysis conducted before modeling
9. FDL_Code 1_Model.ipynb - Python file containing the end to end execution of the final best performing model fine tuned BERT model ensemled with its variation, that gave the highest accuracy score on Kaggle Leaderboard
10. FDL_Kaggle_LeaderBoard Standing Private_Irene_Nishtha.PNG - Screenshot of standing on Kaggle Public Leaderboard 
12. FDL_Kaggle Submission_Irene_Nishtha.pdf - Final report describing the end to end execution of the project.

## Help and Contributions
For help and issues, please open an issue in the repository. Contributions to the modelling or analysis are welcome via pull requests.




