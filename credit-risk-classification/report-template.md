# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
    * Overall Accuracy: 99.2%
    * Healthy loan:
      * Precision: 99.7%
      * Recall: 99.5%
    * High-risk loan:
      * Precision: 84.7%
      * Recall: 91.0%


* Machine Learning Model 2 (Oversampled):
  * Description of Model 2 Accuracy, Precision, and Recall scores.
    * Overall Accuracy: 99.2%
    * Healthy loan:
      * Precision: 100.0%
      * Recall: 99.4%
    * High-risk loan:
      * Precision: 84.1%
      * Recall: 99.4%

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
If you do not recommend any of the models, please justify your reasoning.
  * The standard model (model 1) and the oversample trained model (model 2) have similar high performance. Near perfect metrics regarding low risk loan identification (>99%) and high precision when predicting high risk loans (~84%). This indicates that both models have a very high rate of prediction correctness (precision) in both classes and a very high rate of low risk loan identification (recall).
  * However, they differ in the recall of high-risk loans. Model 1 has a high rate (>90%) and Model 2 has a very high rate (>99%). This means that model 2 is about 8% better than model 1 in correctly identifying high-risk loans. 
  * Due to the domain of this data, it is safe to say that model 2 is a better model than model 1. Model 2 has a near negligible drop in performance in all metrics aside from the recall of high-risk loans, where it sees large improvement. It is necessary for the model, which is identfying risk of loan, to identify high-risk loans as these loans pose more dynamic danger than the low risk loans.