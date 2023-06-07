# capston-project-on-classification

## Problem statement -

Our client is an Insurance company that has provided Health Insurance to its customers now they need your help in building a model to predict whether the policyholders (customers) from past year will also be interested in Vehicle Insurance provided by the company.

An insurance policy is an arrangement by which a company undertakes to provide a guarantee of compensation for specified loss, damage, illness, or death in return for the payment of a specified premium. A premium is a sum of money that the customer needs to pay regularly to an insurance company for this guarantee.

For example, you may pay a premium of Rs. 5000 each year for a health insurance cover of Rs. 200,000/- so that if, God forbid, you fall ill and need to be hospitalised in that year, the insurance provider company will bear the cost of hospitalisation etc. for upto Rs. 200,000. Now if you are wondering how can company bear such high hospitalisation cost when it charges a premium of only Rs. 5000/-, that is where the concept of probabilities comes in picture. For example, like you, there may be 100 customers who would be paying a premium of Rs. 5000 every year, but only a few of them (say 2-3) would get hospitalised that year and not everyone. This way everyone shares the risk of everyone else.

Just like medical insurance, there is vehicle insurance where every year customer needs to pay a premium of certain amount to insurance provider company so that in case of unfortunate accident by the vehicle, the insurance provider company will provide a compensation (called ‘sum assured’) to the customer.

Building a model to predict whether a customer would be interested in Vehicle Insurance is extremely helpful for the company because it can then accordingly plan its communication strategy to reach out to those customers and optimise its business model and revenue.

Now, in order to predict, whether the customer would be interested in Vehicle insurance, you have information about demographics (gender, age, region code type), Vehicles (Vehicle Age, Damage), Policy (Premium, sourcing channel) etc.



## Database:

1.**id** : Unique ID for the customer

2.**Gender**: Gender of the customer

3.**Age** : Age of the customer

4.**Driving_License** : 0=Customer does not have DL, 1= Customer already has DL

5.**Region_Code** : Unique code for the region of the customer

6.**Previously_Insured :** 1= Customer already has Vehicle Insurance, 0= Customer doesn't have Vehicle Insurance

7.**Vehicle_Age** : Age of the Vehicle

8.**Vehicle_Damage** : 1= Customer got his/her vehicle damaged in the past. 0= Customer didn't get his/her vehicle damaged in the past.

9.**Annual_Premium**: The amount customer needs to pay as premium in the year

10.**PolicySalesChannel** : Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.

11.**Vintage** : Number of Days, Customer has been associated with the company

12.**Response** : 1 : Customer is interested, 0 : Customer is not interested.



## Data Cleaning And Feature Engineering

1. **Removing Duplicate Rows**

2. **Handling null values**

## Exploratory Data Analysis

ploting graphs for getting the clear information about dataset.

### *Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:*

1.Bar plot

2.Line plot

3.Heatmap

4.Pie Chart

5.Box Plot

6.violin plot 

7.Dist plot

8.Histogram plot


## Models

1.**Logistic Regression**

2.**RandomForest Classifier**

3.**XGBClassifier**

4.**Decision Tree**

5.**Random Forest**

6.**KNN(K-Nearest Neighbors)**

7.**Gradient Boosting**

8.**XGBoost**

9.**LightBGM**


## Conclusion

1.Starting from loading our dataset, we initially checked for null values and duplicates. There were no null values and duplicates so treatment of such was not required.

2.we observed that customers having vehicles older than 2 years are more likely to be interested in vehicle insurance

3.Customers of age between 30 to 60 are more likely to buy insurance.

4.customers having damaged vehicles are more likely to be interested in vehicle insurance.

5.The variable such as Age, Previously_insured,Annual_premium are more afecting the target variable.

6.I observed that the target variable was highly imbalanced.So this issue was solved by using Random Over Sample resampling technique.

7.Customers with Driving License have higher chance of buying Insurance.

8.The male ratio is slightly higher than the female for purchasing vehicle insurance.

9.we can clearly say that 99.8% i.e majority of people have DL and very less people are not having DL.

10.Around 43.2% of vehicles are less than one year old, 52.6% of vehicles are of 1-2 year old, And 4.2% of vehicles are of more than 2 year old.

11.The count of damaged and not damaged vehical is almost same.

12.1Based on these observations, it appears that the decision tree and random forest models are performing relatively better compared to the other models in terms of accuracy, F1 score, and ROC AUC score.

13.Among the models I have evaluated, the logistic regression, XGBClassifier, decision tree, random forest classifier, random forest, and KNN models have relatively high accuracy scores, ranging from 0.821 to 0.875.

14.The decision tree, random forest classifier, random forest, and KNN models have better performance in terms of these metrics.

15.The decision tree and random forest models show slightly higher ROC AUC scores compared to the other models.




