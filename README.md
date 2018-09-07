Instacart Market Basket Analysis with SQL (SQlite3)

Which products will an Instacart consumer purchase again?
Data for this project is downloaded from https://www.kaggle.com/c/instacart-market-basket-analysis/data

# Data Description

The dataset is a relational set of files describing customers' orders over time. The goal is to predict which products will be in a user's next order. The dataset is anonymized and contains a sample of over 3 million grocery orders from more than 200,000 Instacart users. For each user, we provide between 4 and 100 of their orders, with the sequence of products purchased in each order. We also provide the week and hour of day the order was placed, and a relative measure of time between orders. 

# Data analysis
csv files were loaded into SQlite and new tables were created by joining loaded tables.
Following the visual data analysis features were chosen for machine learning algorithms. Feature selection was performed by both SelectKBest and LASSO algorithms and showed simillar results. Top 6 fearures (order_number, 'add_to_cart_order', 'days_since_prior_order', 'order_hour_of_day', 'product_id', 'order_id') were chosen as best features for prediction of the product in the next customer's order.
8 Machine learning algorithms for classification were tested:
1. Logistic Regression
2. SVM_rbf
3. SVM_sigmoid
4. Gaussian Naive Bayes
5. SVM_linear
6. Decision Tree
7. Random Forest
8. K - Nearest Neighbors.
Random forest proved to be the best algorithms for this classification task. 
The parameters of Random Forest were optimized and slightly better results were achived.
Overall, customer's next order could be predicted with over 76% confindence.
