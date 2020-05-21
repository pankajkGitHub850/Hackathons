# machine-hack-churn-predictio
I have attached code file(latest tried model), you can go through that for better understanding.if you stuck anywhere ping me.In the code file i have trained a voting classifier with lightgmb,xgboost,knn but got less than the lightgmb.
# Problem statement
To predict the insurance customer churn.
# Data set information.
The data set was **embalanced** in nature, number of churned customers was very less.Training dataset had 15 attributes names feature_0 to feature_15, 7 was numeric among this and rest categorical.
# Approach
After simple **EDA** found that number of churned customer is independent to the number of occurances of categorical values.(ploted bar with hue as labels), SO decided to do **Target Encoding**.
Derived aprox 120 attributes by aggregating both numeric and categorical attributes with different techniques(used itertools.combination()).
Trained a RF as base model,but the model was not able predict churned customer (confusion_matrix) due to less number of churned customer in training data set.
Done upsampling(SMOTE).
Selected 30 attributes(RFE).
Trained Lightgbm and got 0.60 f1score.
Tuned the model (GridSearch) and got 0.627 f1score and 40th,48th position in Public LB and Private LB respectively.
