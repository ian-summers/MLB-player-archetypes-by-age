## Table of Contents
- [Introduction](#introduction)
- [Data Overview](#data-overview)
- [Logistic Regression](#logistic-regression)
- [Attempts to Improve Model Accuracy](#attempts-to-improve-model-accuracy)
- [Random Forest](#random-forest)
- [Correlation Analysis](#correlation-analysis)
- [Conclusion](#conclusion)

## Introduction
This document presents an analysis of player performance data in a sports organization. The goal of this analysis is to determine if players exhibit unique playing styles based on age. Various techniques such as logistic regression, correlation analysis, PCA, and normalization were employed to explore the data and improve model accuracy.

## Data Overview
The dataset includes a comprehensive range of metrics related to player performance, including offensive and defensive statistics, physical attributes, and age. The dataset was preprocessed to handle missing values and categorical variables, ensuring data integrity for analysis.

## Logistic Regression
We employed a multinomial regression model to handle multiple age groups in our analysis. Initially, the model achieved an accuracy of 50.7%. Despite implementing various optimization techniques, including PCA and normalization, we reached a plateau at around 53% accuracy. Our analysis included generating a confusion matrix and classification reports.

The model demonstrated its strength in accurately identifying players aged 24-28. However, it encountered difficulties with other age brackets, particularly older players. These findings highlight the challenges in categorizing players' playing styles solely based on age.

## Attempts to Improve Model Accuracy
Several strategies were employed to enhance model accuracy, including rearranging age brackets, PCA, and normalization. However, these attempts yielded minimal improvements, indicating that the dataset's classification value was limited compared to its predictive value in linear regression analysis.

## Random Forest
A random forest model was created to see how it would compare to the other machine learning methods we had attempted prior. The same datasest was read in and preprocessing was preformed. Running the model initially with 120 estimators, we were able to achieve very similar results to the other models. Multiple attempts were made to optimize the model including, adding removed feature columns back into the dataset, adjusting the number of estimators, and handeling imbalanced classes. Each attempt at optimizing the model did not work.  

## Correlation Analysis
A correlation matrix was generated to identify relationships between variables. While some weak negative correlations were observed such as a decrease in certain performance metrics with age, no strong correlations were found that significantly impacted model accuracy.

## Conclusion
Our analysis explored the question of whether players exhibit unique playing styles based on age. The findings suggest a nuanced perspective: while age plays a role in playing style to some extent, it's not a definitive determinant.

The logistic regression model we utilized achieved a maximum accuracy of approximately 53%, showcasing its capability to identify players aged 24-28 accurately. However, its performance deteriorated when dealing with age groups outside this range. Attempts to adjust age brackets led to a decrease in model accuracy. Furthermore, additional techniques like PCA and normalization yielded marginal improvements.

A parallel analysis using a random forest model showed comparable accuracy results, indicating consistency in our findings across different methodologies.

Exploring correlations through the matrix revealed weak associations between age and key performance metrics. While older players tend to make fewer errors, these correlations were insufficient to significantly enhance the logistic regression's predictive power by reducing the feature set.

Despite these challenges, our dataset exhibits robust predictive capabilities, especially in predicting a player's future contribution (Wins Above Replacement, or WAR), as evidenced by low mean square error values in linear regression analyses. However, for classification tasks like age-based playing style identification, further refinement and feature engineering may be necessary to achieve higher accuracy.

Overall, while age contributes to playing style variations to some degree, our analysis suggests that other factors play a more substantial role in determining a player's unique style on the field.
