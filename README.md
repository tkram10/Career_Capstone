# Home Credit Default Risk
### Summary And Objective
Many people struggle to get loans due to insufficient or non-existent credit histories. Unfortunately, this population is often taken advantage of by untrustworthy lenders. Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience.

In this notebook, we aim to explore the issue of credit default risk at Home Credit, a company that seeks to provide loans to individuals with insufficient or nonexistent credit histories. This underserved population often faces exploitation by unreliable lenders, making it crucial for Home Credit to ensure a positive and safe borrowing experience.

To address this challenge, Home Credit leverages various sources of alternative data, such as telecom and transactional information, to predict their clients' repayment abilities.
The primary objective is to ensure that clients with the capacity to repay are not declined, and loans are structured with optimal principal amounts, maturities, and repayment schedules to empower clients toward financial success.

### Process 

Our analysis begins with data cleaning, where we preprocess and prepare the data for modeling. Subsequently, we develop predictive models using the cleaned data to assess credit default risk. We focus on the target variable and employ different machine learning models, calculating relevant metrics like accuracy and ROC values.

The objective is to identify the best-performing model based on Kaggle scores. We start with Logistic regression and then explore penalized regression, specifically LASSO, due to collinearity issues. Additionally, we examine Random Forest, XGBoost, and Light XGBoost to assess their effectiveness in predicting credit default risk.

#### image-1: Results of all modeling techniques that we have used in this project.
<img width="475" alt="Screen Shot 2023-12-06 at 12 00 12 AM" src="https://github.com/tkram10/Career_Capstone/assets/72302122/1a8a6e85-03dd-4be4-b94f-bc2a294aecca">
Here, we can see from the results table the light Gradient boost has a high Kaggle score of 0.72387 and a high AUC score of 0.6860.

We first started with the logistic regression model and got around a 0.67 Kaggle score. We understood that it has multicollinearity by examining the VIF scores and used the penalized regression model LASSO to fit the data, and the Kaggle score improved to 0.69.

We further examined the data modeling with random forest, did hyperparameter tuning, and got Kaggle around 0.66, indicating the need for further models.

So, we used the XG Boost model with hyperparameter tuning and secured the 0.71 Kaggle score. Then, we examined the light Gradient boosting, which is fast and accurate with a Kaggle score of 0.723.

To conclude, Light Gradient Boost is a good model fit for the given cleaned dataset with a Kaggle score of 0.72387.


