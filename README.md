# Problem Statement
- The telecom industry faces high competition, leading to an average annual churn rate of 15-25%. Retaining high-profitable customers is a priority for incumbent operators, as acquiring new customers is more expensive. To reduce churn, predictive models are needed to identify high-risk customers in a market dominated by prepaid services in India and Southeast Asia.

# Defining Churn
- Churn prediction is particularly critical for prepaid customers, as they may stop using services without notice. The project focuses on usage-based churn, identifying customers who have had no usage over a specific period. High-value customers, generating 80% of revenue, are targeted to minimize revenue leakage.

# Objective and Data
- The goal is to predict churn in the ninth month using data from the first three months. Understanding customer behavior during churn is vital, involving three phases: 'good,' 'action,' and 'churn.' Predictive models will be built using customer-level data from June to September.

# Approach
1. Preprocess data and conduct exploratory analysis.
2. Derive new features and apply PCA for dimensionality reduction.
3. Train and tune various models, handling class imbalance.
4. Evaluate models with suitable metrics, prioritizing churner identification.
5. Select a model based on evaluation metrics.
6. To identify important predictor attributes for churn, build another model, like logistic regression or a tree-based model. Handle multi-collinearity in logistic regression and visualize the important predictors using plots or summary tables.
7. Finally, provide recommendations for managing customer churn based on observations
   
# Summarzing important details to keep in mind:
- This project is based on the prepaid users only
- This project is based on __usage based churn__: Usage based churn refers to the customers who have not done any usage, either incoming or outgoing - in terms of calls, internet, etc. over a period of time
    - However, if the customer has stopped using the services for a while, it may be too late to take any corrective actions to retain them. Eg: predicting churn could be useless if the customer is not using any services for the past 2 months because a possible scenario is the customer would have already switched to another operator
- This project is focused to decrease the churn rate of __high-value customers__ only
    - High value customers represent the 70th percentile of the average recharge amount in the __first two months__
- This project is to predict the churn rate for the 9th month using the data for 6th, 7th, and 8th month
- The first two months are __good phase__, the third month is the __action phase__ and the fourth month is the __churn phase__
- Tag the churners based on the below conditions
    - Not made any calls (incoming or outgoing)
    - Not used mobile internet once
    - After tagging, reove all the attributes that correspond to the churn phase '_9'
