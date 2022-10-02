# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

## Results
For this analysis, we were using personal finance metrics to determine the credit risk that lending to certain borrowers posed. Variables examined were: loan size, the interest rate of the loan,how much money the borrower made, how much debt they had relative to that income, how many loans or lines of credit they currently had open, how many derogatory marks were on their credit report, the total amount of debt they had, and finally the status of the loan, with a 0 representing a low risk borrower, and a 1 representing a high risk borrower. We attempted to make a model that could predict the credit risk with the highest degree of accuracy. The loans examined contained 75036 of good loans, and 2500 risky loans. Logistical regression and oversampling was used on the data to try and build an accurate model. 

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
Accuracy
* 0.9218124642767772
precision

* 0: 1.00      

* 1: 0.85              

recall

* 0: 0.99 
* 1: 0.91  
* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
Accuracy
* 0.9205494133884273
precision     

* 0: 1.00    
* 1: 0.84

recall 
* 0: 0.99
* 1: 0.99


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
It seems to me that it's more important overall to predict the 1s than the 0s. Bad borrowers can be costly for a lending platform, so perhaps a model with a higher level of precision would be more valuable in general. That said, both models here scored within 1% of each other in the precision category, so there is not too much difference between them. Recall is a method that is generally prefered when there is a high cost with a false positive, which is actualy not the case here. That being said, because precision is nearly identical with both models, but recall is much higher in the oversampled model, I would reccomend model 2 if I needed to choose between them. Recall is less valuable when sifting through loan applicants, but it seems to create a more accurate model overall and that might balance out the 1% lower precision by selecting more applicants that are actually good borrowers and thereby generating more profit in interest from them. 