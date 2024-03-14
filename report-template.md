# Module 12 Report: Ravi 

I worked with Kayla on this homework who helped go through my assignment from the first classification report onwards. 

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
  * Model 1 uses a logistic regression model with the Original dataset. The scores from the classification report: 
      * Healthy loans (0) : Precision: 1, Recall: 0.99, F-1 Score: 1.00, Support 18746
      * Unhealthy loans (1): Precision: 0.85, Recall: 0.93, F-1 Score: 0.89, Support: 638 
  ** What this shows us ** 
  * Precision of Healthy Loans vs. Unhealthy Loans. For Healthy Loans, our algo doesn't have any issues with mislabeling. For unhealthy loans, it can create false negatives or positives. For Recall, our algo can find healthy and unhealthy loans (or forecast them) to an extremely high degree. And F-1 score being 1.00 for Healthy and 0.89 for unhealthy means that combined our algo can accurately predict with precision with little inaccuracies in forecasting people with unhealthy loans in the future. 
      
      


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
  * Model 2 uses logistic regression with resampled data. The scores from the classification report are as follows: 
        * Healthy loans: Precision: 0.99, Recall: 0.67, F-1 Score: 0.80, Support: 56290
        * High Risk Loans: Precision: 0.75, Recall: 0.99, F-1 Score: 0.86, Support: 56290
   ** What this shows us ** 
   * Precision of Healthy Loans vs. Unhealthy Loans. For Healthy Loans, our algo doesn't have an issue with mislabeling. However, for unhealthy loans, this becomes apparent. For recall, our algo is less likely to recall Healthy Loans vs. Recalls for High Risk Loans. Lastly, for F-1 Score, our algo is less reliable to predict precision and recall for Healthy loans vs. Unhealthy loans. 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
    * The Machine Learning Model 1 performs significantly better than Model Number 2, with higher F-1 Scores for Healthy and Unhealthy Loans. This is backed by more consistent high precision and recall for both healthy and unhealthy loans. 

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    * Performance does depend on the problem we are trying to solve. It is more important to predict likelyhood of Default. This is because by defaulting - the likelyhood of receiving any ROI is 0. When dealing with loans, an algo that is more aggressive in filtering out healthy loans is more acceptable than one that filters in junk-grade loans. These can be incredibly damaging to financial institutions. 

If you do not recommend any of the models, please justify your reasoning.

I recommend model #1 for more consistency across the board for Precision, Recall, and Support. 
