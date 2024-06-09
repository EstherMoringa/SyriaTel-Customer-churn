SyriaTel Customer Churn Prediction.

![image](https://github.com/EstherMoringa/SyriaTel-Customer-churn/assets/162351617/ecf62885-4554-47d0-8818-e64c34fd073f)

## Business Overview
The telecommunications industry is marked by fierce competition and rapid technological advancements, where customer retention stands as a pivotal factor for sustainable growth. Customer churn, the phenomenon of customers discontinuing services, poses a significant challenge for telecom companies like SyriaTel, leading to revenue loss, decreased market share, and escalated acquisition costs. 

This project seeks to address the critical issue of customer churn prediction for SyriaTel by leveraging machine learning techniques on available data. By developing a predictive model tailored to SyriaTel's customer base, the aim is to provide actionable insights for strategic decision-making and customer retention efforts. Through an understanding of industry dynamics, SyriaTel's market position, and the significance of churn reduction.

## Problem Statement
In the competitive landscape of the telecommunications industry, SyriaTel faces the challenge of retaining its customer base amidst increasing churn rates. Hence, will aim to develop a robust predictive model capable of identifying customers at risk of churn, thereby enabling proactive retention strategies. By analyzing historical customer data, the aim is to uncover patterns and indicators that precede churn behavior.

## Objectives
### General Objectives
To build a classifier for SyriaTel for predicting customer churn.

### Specific Objecties
1. Identify relevant features correlated with churn.
2. Develop and train predictive models of an accuracy of at least 90% using machine learning algorithms that will identify customers at risk of churning.
3. Interpret model results and derive actionable insights for SyriaTel's business strategy.

## Challenges
* Limited data: The availability and quality of data could be a challenge.
* Imbalanced classes: There might be fewer instances of churn compared to non-churn.
* Identifying relevant features: Selecting the right features that correlate with churn prediction.
* Interpretable model: Balancing between accuracy and interpretability of the model for business understanding.
* Overfitting: Preventing the model from capturing noise in the data.

## Data Understanding
The SyriaTel dataset is from Kaggle and it contains information about customer activity and whether or not they canceled their subscription with the Telecom firm. The dataset contains 3333 entries and 21 columns.

#### Summary of Features in the Dataset

* state : Customer's different states.
* account_length: active number of days for a customer's account.
* area_code : 'customer's location
* phone_number : customer's phone number
* international_plan : "yes" if the user has the international plan, otherwise "no"
* voice_mail_plan : "yes" if the user has the voice mail plan, otherwise "no"
* number_vmail_messages : customer has a vmail plan and how many vmail messages do they get
* total_day_minutes : total number of call minutes used during the day
* total_day_calls : total number of calls made during the day
* totalday_charge : day calls' total charge
* total_eve_minutes : total number of call minutes used in the evening
* total_eve_calls : total calls made in the evening
* total_eve_charge : total charge on evening calls
* total_night_minutes: Total number of call minutes used at night
* total_night_calls : Total number of night calls
* total_night_charge : Total charge on night calls
* total_intl_minutes : total international minutes used
* total_intl_calls : total number of international calls made
* total_intl_charge : total charge on international calls
* customer_ervice_calls : number of calls made to customer service
* churn : boolean on whether the customer left or not

## Data Preparation.
* Drop unnecessary rows like area code since we have state.
* Make phone number be unique Identifier
* Check for outliers
* Perform Univariate analysis
* Bivariate analysis
* multivariate analysis
  
## Modeling
### Logistic Regression
![image](https://github.com/EstherMoringa/SyriaTel-Customer-churn/assets/162351617/9caa985d-edce-42f6-bda3-2a19fdc98e41)

The Train accuracy of the model is 85% and the Test Accuracy 0.85%

The precision for class 0 which is not churned is 86% and the precision for class 1 which is churned is 39%.

The recall for class 0 which is not churned is 99% and  the recall for class 1 which is churned 5%.

The F1-score for class 0 which is not churned is 92% and for class 1 of churned is 9%.

## K-Nearest Neighbors
![image](https://github.com/EstherMoringa/SyriaTel-Customer-churn/assets/162351617/d7e4c48d-70bf-4c01-922c-8cebfbbdd5d0)

This model accurately classifies 89% of the test data. Which is an improvement from the previous model.

 The model will predict that a customer will churn and it will be correct at 77% which is the precision percentage. It correctly identifies 32.9% of all customers who actually churned, which is our recall percentage.

 ## Decision Tree Classifier
 ![image](https://github.com/EstherMoringa/SyriaTel-Customer-churn/assets/162351617/d4048f47-1782-4e85-9fc7-e27ca0c8f5e5)

 The Decision tree classifier has a high accuracy rate of 90.5% compared to the previous models.

There is consistency of Performance in the cross-validation which suggests that the decision tree generalizes well to unseen data.
![image](https://github.com/EstherMoringa/SyriaTel-Customer-churn/assets/162351617/5e7dd398-b1c7-48fb-8af8-7ec609104167)

## XGBoost
![image](https://github.com/EstherMoringa/SyriaTel-Customer-churn/assets/162351617/f5e49e15-2c98-48e3-ba32-b2f05267048c)

High Predictive Power: The XGBoost model demonstrates strong predictive power, achieving a high accuracy rate of 95.1%. Indicating that the model is effectively capturing the underlying patterns and relationships in the data, making accurate predictions on unseen instances.

Precision: It is the ratio of correctly predicted positive observations to the total predicted positives. A precision of 0.95 for class 0 means that 95% of the instances classified as class 0 are actually class 0. Similarly, a precision of 0.94 for class 1 means that 94% of the instances classified as class 1 are actually class 1.

Recall: It is the ratio of correctly predicted positive observations to the all observations in actual class. A recall of 0.99 for class 0 means that 99% of the actual instances of class 0 were classified correctly. A recall of 0.71 for class 1 means that only 71% of the actual instances of class 1 were classified correctly.
    
F1-score: It is the weighted average of Precision and Recall. It ranges from 0 to 1, where 1 is the best value. It provides a balance between precision and recall. A high F1-score indicates good performance.

Model Effectiveness: The high accuracy rate suggests that the XGBoost model is well-suited to predit customer churn as it has outperformed other models.

Potential for Deployment: With such a high accuracy rate, the XGBoost model will be suitable for deployment in the SyriaTel Customer Churrn modeling.

## Recommendations
1. We recommend to the stakeholders to adopt the XGBoost model for predicting customer churn, since it achieved an accuracy of 95.1% when classifying customer churn. This means that it correctly predicted 95.1% of the cases.

2. Check on states like NJ, CA, TX, MD, SC, MI, MS, NV, WA, ME which have the highest churn rate. There could be different reasons that lead to customer churning.

3. Feedback Mechanisms, by creating feedback mechanisms that encourage customers to provide input on their customer service experience will improve service quality. This can be due to the fact that there was a higher proportion of customers who subscribed to the international_plan churning with a percentage of 42.4% which is more than those customers that did not subscribe at 11.5%.  
Hence stakeholders should invetisgate if there are any isues associated with the international plans that could be making the plan unsatisfactory to the client. 
And this can be achieved by developing a feedback mechanism.

4. Regularly Review and Update Plans, since the telecommunications industry is highly competitive and dynamic. Regularly assess and update your service plans to ensure they remain competitive and meet evolving customer needs. Offering flexibility and customization options can be an attractive feature for customers.

5. There is an association with total calls made (tota day calls, total evening calls, total night call) from a state and it probability of having a higher number of customers churning. Like CA had the lowest total calls made and it was leading in the percentage of having numbers of customers churning. As stakeholders increase and work on their marketing, the total call should be considered.








 










































