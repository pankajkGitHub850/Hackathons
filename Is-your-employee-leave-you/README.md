Employee retention is the most necessary thing for any organization, or if we see with management point of view then it becomes very very important to estimate the attrition rate for uninterrupted production.
So, in this challenge, we had to predict the attrition rate of employees(max 100 scores). This challenge consists of one more problem of SQL query of max 30 scores. So this challenge becomes a total of 130 scores.
Here, I'm sharing my approach towards the challenge, by which I got 34th position among 5000+ participants. Initially, I have made a base model by just leveraging the xgboost and Labelecoder, other than this I did nothing and submit my very first solution file and got a score of 81.00358/100. After this I started some preliminary EDA and found some attributes with missing data, I filled them with either by mean or median. After I generated some new features by aggregation, combined them both and trained two tunned(GridSearch) model xgboost and Lightgbm and got 81.31628/100.

The SQL query was pretty simple, I got 30/30. So my score becomes 111.31628 with this I secured 34th position.


## Atrributes
['Employee_ID', 'Gender', 'Age', 'Education_Level',
       'Relationship_Status', 'Hometown', 'Unit', 'Decision_skill_possess',
       'Time_of_service', 'Time_since_promotion', 'growth_rate', 'Travel_Rate',
       'Post_Level', 'Pay_Scale', 'Compensation_and_Benefits',
       'Work_Life_balance', 'VAR1', 'VAR2', 'VAR3', 'VAR4', 'VAR5', 'VAR6',
       'VAR7', 'Attrition_rate']
