# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
This analysis is to see if a supervised learning model can be used to correclty predict whether or not a loan would be considered a high risk or a healthy loan base on a variety of factors such as debt, income, amount of the loan, the intrest rate and how many derogatory marks a applicant has. It also checks to see if Logistict Regression, SVC, or Decision tree would work the best.
* Explain what financial information the data was on, and what you needed to predict.
loan_size - amount of the loan being requested
intrest_rate - interest rate of loan requested
borrower_income - income of the person 
debt_to_income - a comparison of the total amount of debt comapred to the total income ie total_debt/borrower_income
num_of_accounts -   number of accounts the applicant has
derogatory_marks - marks agains an applicant.
total_debt - amount of debt the applicant has
loan_status - 0 is a healthy loan, 1 is a high risk loan

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`). Looking at the amount high risk loans in comparison to healthy loans, there are a lot more healthy loans than there are high risk, 75036 healthy compared to 2500 high risk, this might result in a bias when it comes to the prediction where it will be easier to find healthy loans than it will be to find high risk loans.

* Describe the stages of the machine learning process you went through as part of this analysis.
The first step of machine learning is to seperate the data between the results we are looking at, the y value and the data that we are using to find those results, the X dataset. The second step is to randomly select part of our data in this case 75% of the data that the algorithm will look at to learn how to figure out wether a loan is high risk or healthy. The remaining 25% of the data will be used to test the model to see if it is accurate or if the model learned correctly.

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
For this study I tried Logistic Regression, SVC, and Decision tree to see which of them would most accurately predict loan status.


## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
        1.Logistic Regression
            * Accuracy: .99 or 99% this means that overall it was 99% successful in identifying wether the loan was a good loan or a high risk loan.
            * Precision: 
                class 0 .99, 
                class 1 .94 This shows the model was very good at correctly predicting healthy loans
            * Recall: 
                class 0 1.00
                    class 1 .84, This score shows that the model struggled a little bit in finding which loans were going to be high risk loans, this is probably due to the larger amount of healthy loans compared to the high risk loans, 75036 healthy, 2500 high risk.
        2. SVC
            *Accuracy:99%
            *Precision: 
                class 0 .99 
                class 1 .99 This shows the model was very good at correctly predicting healthy loans
            *Recall: 
                class 0 1.00 
                class 1 .84, This score shows that the model struggled a little bit in finding which loans were going to be high risk loans, this is probably due to the larger amount of healthy loans compared to the high risk loans, 75036 healthy, 2500 high risk.
        3. Decision Tree
            *Accuracy: 99%
            *Precision: 
                class 0 .99
                class 1 .85 This score shows that the model struggled a little bit in finding which loans were supposed to be healthy
            *Recall: 
                class 0 1.00 
                class 1 .84, This score shows that the model struggled a little bit in finding which loans were going to be high risk loans, this is probably due to the larger amount of healthy loans compared to the high risk loans, 75036 healthy, 2500 high risk.
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
Each of the models preformed very similarly to one another, with each of them getting an overall accuracy score of 99%, the differeces came in the breakdowns of where things were missed. in terms of false positives SVC preformed the best with only 6, followed by logistic regression with 36 and then finally decision tree with 91. However in terms of false negatives. Decision tree did the best with 98, followed by logistic regression with 110 and then last SVC with 114. I think that with more data about high risk loans SVC would be the choice that I go with because I think that the number of false positives would reduce making it the best choice.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
I do think that for this problem we would rather have false negative than false positives or in other words we would rather mark a healthy loan and high risk instead of marking a high risk loan as healthy. So in that respect decision tree would probably be the better choice however I would still probably go with SVC instead because the difference between 114 and 98 is much less than the difference between 91 and 6

If you do not recommend any of the models, please justify your reasoning.
