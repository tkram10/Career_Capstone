# Home Credit Default Risk
### Summary And Objective
Many people struggle to get loans due to insufficient or non-existent credit histories. Unfortunately, this population is often taken advantage of by untrustworthy lenders. Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience.

In this notebook, we aim to explore the issue of credit default risk at Home Credit, a company that seeks to provide loans to individuals with insufficient or nonexistent credit histories. This underserved population often faces exploitation by unreliable lenders, making it crucial for Home Credit to ensure a positive and safe borrowing experience.

To address this challenge, Home Credit leverages various sources of alternative data, such as telecom and transactional information, to predict their clients' repayment abilities.
The primary objective is to ensure that clients with the capacity to repay are not declined, and loans are structured with optimal principal amounts, maturities, and repayment schedules to empower clients toward financial success.

### Process 

Our analysis begins with data cleaning, where we preprocess and prepare the data for modeling. Subsequently, we develop predictive models using the cleaned data to assess credit default risk. We focus on the target variable and employ different machine learning models, calculating relevant metrics like accuracy and ROC values.

### Findings

#### image-1: Gender and Loan Repayment Probability

![by_gender](https://github.com/tkram10/Career_Capstone/assets/72302122/065790a3-f24e-4ee6-9116-4ba25ff4feab)

The probability of loan repayment differs by gender. Male applicants have an approximately 89.85% chance of loan repayment. In contrast, female applicants are more likely (approximately 93.00%) to repay loans. This suggests that female applicants in the dataset have a slightly better loan repayment rate than male applicants.

#### image-2: checking whether Region_Rating has an effect on the default rate or not.

<img width="482" alt="Picture1" src="https://github.com/tkram10/Career_Capstone/assets/72302122/f11bc02b-64b9-4574-964d-e6d8e2736979">

The region ratings have ratings from 0 to 4, where four is a low-rated area, and 0 is a high-rated area.
For the right part, from 2.5 to 4 of the region rating, we can see a high risk of default, whereas the region rating of 0 to 1.5 on the left side of the plot has less default risk.
Thus, Region rating has an effect on the default rate.

#### Contribution to the project
After preprocessing the data, I constructed the fundamental statistical method called the logistic regression model, which is used for binary classification problems, like predicting credit default risk. This model estimates the probability of the occurrence of a binary outcome based on predictor variables.
To Identify multicollinearity among predictors, I performed VIF calculations. High VIF values indicate the presence of multicollinearity, where one predictor variable can be linearly predicted from others.
Multicollinearity can adversely affect regression models by inflating standard errors and making coefficient estimates unstable. I utilized LASSO (Least Absolute Shrinkage and Selection Operator) regression to mitigate this issue.

#### Business Value of the solution

1. The Financial Institutions should concentrate on the goods for which the credit has been provided.
2. The region rating and the region population have an effect on the default rate.
3. The annual credit amount has an effect on the default rate.
4. The customer's age affects the repayment rate, as younger people are more likely to default.

 #### Difficulties that your group encountered along the way.

 #### What you learned in the project.
 1. Addressing class imbalance is critical, especially in this project. To Deal with class imbalance, we performed under-sampling technique to.
 2. To deal with multicollinearity, performed VIF calculations and penalized regression techniques like LASSO which can effectively improves the performance of a model.
 3. Data Pre-processing is the biggest challenge for any project.We used one hot encoder to encode the object variables into dummies so that the modeling can also be done on the factor 
    variables.




### Modelling

The objective is to identify the best-performing model based on Kaggle scores. We start with Logistic regression and then explore penalized regression, specifically LASSO, due to collinearity issues. Additionally, we examine Random Forest, XGBoost, and Light XGBoost to assess their effectiveness in predicting credit default risk.

#### image-3: Results of all modeling techniques that we have used in this project.

<img width="475" alt="Screen Shot 2023-12-06 at 12 00 12 AM" src="https://github.com/tkram10/Career_Capstone/assets/72302122/1a8a6e85-03dd-4be4-b94f-bc2a294aecca">

Here, we can see from the results table the light Gradient boost has a high Kaggle score of 0.72387 and a high AUC score of 0.6860.

We first started with the logistic regression model and got around a 0.67 Kaggle score. We understood that it has multicollinearity by examining the VIF scores and used the penalized regression model LASSO to fit the data, and the Kaggle score improved to 0.69.

We further examined the data modeling with random forest, did hyperparameter tuning, and got Kaggle around 0.66, indicating the need for further models.

So, we used the XG Boost model with hyperparameter tuning and secured the 0.71 Kaggle score. Then, we examined the light Gradient boosting, which is fast and accurate with a Kaggle score of 0.723.

To conclude, Light Gradient Boost is a good model fit for the given cleaned dataset with a Kaggle score of 0.72387.


