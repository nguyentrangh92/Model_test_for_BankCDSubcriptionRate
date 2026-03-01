# Data-Driven-Approach-to-Predict-Success-of-Bank--Marketing
Finding out the characteristics that are helping Bank to make customers successfully subscribe for deposits, which helps in increasing campaigns efficiently and selecting high value customers.

# Title: Data Driven Approach to Predict Success of Bank- Marketing
Dataset: Success of Bank marketing
Bank Marketing Data - dataset by data-society | data.world

## Phase 1: Business Understanding

Dataset Overview: The data is related with direct marketing campaigns of a Portuguese banking institution.The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to assess if the product (bank term deposit) would be (‘yes’) or (‘no’).

Purpose: Improve bank marketing strategy and come up with technology driven solutions to reduce phone calls but increase success rate. The classification goal is to predict if the client will subscribe (yes/no) to a term deposit (variable y).

Problem Statement: Finding out the characteristics that are helping Bank to make customers successfully subscribe for deposits, which helps in increasing campaigns efficiently and selecting high value customers.

Application area: The goal is to build a Machine Learning model that learns the unknown patterns, maps and several input features classifying whether clients will subscribe for longer deposits or not.

-	Is there a relationship between a customer's demographic profile and their decision and duration of phone call?
-	Does a customer's credit affect the customer’s decision?
-	Does the information from the previous campaign help improve the successful rate of calling?

## 2/ Initial Data Exploration:

Determine potential dependent variables (DV’s) and independent variables (IV’s) from the data set. These are variables that you would use in your analysis according to the business problems addressed in #1 

<img width="887" height="608" alt="image" src="https://github.com/user-attachments/assets/9d15bb40-9d71-4363-8f63-350d82cc6ad0" />

## 3/ Correlations
### a/ The correlation analysis for the numerical variables 

We have 3 pairs of variables have the highest correlation, more than 0.9 for each of pair
-	Euribor3m with emp.var rate 
-	emp.var.rate with nr.employed
-	Euribor3m with nr. employed

emp.var.rate with nr.employed (0.907)
	Euribor3m with emp.var rate(0.972)
	Euribor3 with nr. employed(0.946)
 	 

We also have few negative relationships but those are not meaningful (previous, pdays) so we do not continue to interpret or discover them more.

### b/ Interpret the results. Is there evidence of a linear relationship between the variables? If so, characterize the relationship. Is it positive or negative? Is it weak or strong?

-	Based on scatter plot chart above, there might have been a positive linear relationship between these 3 pairs (emp.var.rate, euribor3m, and nr. employed) numerical variables, as they have strong positive correlation which we can see from the correlation matrix and the distribution of plots in the chart

### c/Provide any business cases related to the results of your correlation analysis.

In our case, the three variables belong to social context attributes, which are the index of market:
-	emp.var.rate: the employment variation rate, which is the rate between who are employed to the population
-	euribor3m: the Euro interbank offered rate, which makes sense because the collected data is from a bank in Portuguese
-	nr.employed: number of employees in the population
The definition of each index can show us part of relationship between these variables, when the employment variation rate or the currency rate increases that shall result in the growth of amount of employees (nr.employed)

## 4/ Multiple Regression – since our DV is binary so we cannot run this regression
## 5/ Logistic regression:
We choose to go with the Decision Tree model in this case as we can analyze meaningful patterns from the data to give rich suggestions to the management team. We have taken credit history and attributes related to previous campaign information into consideration to construct the model. When combining all the three models, the decision tree gave detailed information on customer response rate in specific areas. 
We would suggest to the management that certain months of the year are not successful, so they should focus on their marketing strategies to attract their customers. Also in terms of credit history, we found out that those who are in unknown and no category are not subscribing to the term deposit. We have to make a plan on how to target those customers as well. 
The management has to investigate  demographic profiles of these clients in the unknown/no category to find out the reason for their response. Also, as the number of days increased since last contacted there was low subscription rate for some customers. This means that we need to improve the quality of contacting the customers. Once we understand the demographic profiles for those clients we can connect with the customers in a different way (social media, text messaging, flyers) and do cost benefit analysis accordingly
Model/Performance	Logistic regression	Decision Tree	Neural networks
Accuracy	92.69%	92.74%	92.56%
Sensitivity	17.75% 	22.39%	23.43%
<img width="468" height="102" alt="image" src="https://github.com/user-attachments/assets/de86d01a-d4f6-4361-8f7f-6f20c21b46ff" />

