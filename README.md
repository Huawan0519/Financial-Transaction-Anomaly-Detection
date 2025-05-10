# Financial-Transaction-Anomaly-Detection
Use Google Cloud Platform Handle Data

### Contributors
- Huawan Zhong
- Ching Hsuan Lin
- Aryan Sehgal
- Jean Miranda Huarancca
- Rodrigo Yeo Cordero

### Executive Summary
In this project, our goal is to detect potential money laundering activities through transaction analysis. We begin by loading the dataset from our S3 bucket and performing an initial overview of its dimensions and missing values. In our case, we intentionally retain outliers, since they may represent the most suspicious transactions for our analysis. We then merge this main dataset with our currency exchange file.

Next, we carry out exploratory data analysis to uncover key patterns: the time-series behavior of transactions, transaction volumes by region, the currencies in use, and the payment formats most commonly employed. After identifying these insights, we move on to data preprocessing to prepare the data for our machine-learning models. This phase includes converting string fields to numeric values, encoding categorical variables, and standardizing datetime formats.

Once the data are ready, we train a baseline logistic regression model and follow by random forest classifier, using our labeled data for evaluation. We employ LIME to interpret and explain the models’ predictions. Finally, due to computational constraints, we sample the dataset and apply K-means clustering to identify distinct transaction groups, as well as Isolation Forest to compute an anomaly score for each transaction.
