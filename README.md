# Boston Housing Price Prediction

House price prediction is an important concept in the real estate industry and has been a popular problem in research for years since the traditional house price prediction depend on cost and sale price comparison does not satisfy the accepted standards and certification process. In addition to getting accurate prediction it is important to know the factors that have a significant impact on the house price. In this project on House Price Prediction, our task is to predict house prices in Boston using different approaches.

In the EDA folder, we do the exploratory data analysis to exploit the features of the data.

The Boston Housing Dataset is a derived from information collected by the U.S. Census Service concerning housing in the area of Boston MA. It consists of 506 records with 13 attributes each. The attributes are:
- CRIM: per capita crime rate by town 
- ZN: proportion of residential land zoned for lots over 25,000 sq.ft 
- INDUS: proportion of non-retail business acres per town 
- CHAS: Charles River dummy variable (1 if tract bounds river; 0 otherwise)
- NOX: nitric oxides concentration (parts per 10 million)
- RM: average number of rooms per dwelling 
- AGE: proportion of owner-occupied units built prior 1940 
- DIS: weighted distances to five Boston employment centers 
- RAD: index of accessibility to radial highways 
- TAX: full-value property-tax rate per $10,000 
- PTRATIO: pupil-teacher ratio by town 
- B: (1000(𝐵𝑘 −0.63)2 where 𝐵𝑘 is the proportion of blacks by town 
- LSTAT: % lower status of the population  
- MEDV: Median value of owner-occupied homes in $1000’s (unit). This is the response value that we have to predict.
- 
## EXPLORATORY DATA ANALYSIS
Before training, we load the data into the Jupyter notebook to analyze its exploratory variables. First, missing values are checked and there is 0 missing value. After that, some basics statistics are displayed. 
![image](https://github.com/user-attachments/assets/e97552ca-40eb-4e96-b1ef-65a877ac5925)

Then, we plot a heat map to survey the correlation between each feature. 

![image](https://github.com/user-attachments/assets/6f33d684-40fe-46b0-9a25-81fd88981002)

From the graph, we can see that RM and LSTAT are highly associated with MEDV (our target variable) with correlation coefficient 0.7 and -0.74 respectively. To justify our hypothesis, we use scatter plot of each feature to MEDV and a histogram of the respond variable. As a result, RM and LSTAT are both linearly correlated with MEDV.  However, we notice there are some unusual data point related to the values MEDV = 50, RM < 4 and RM > 8.5 at the graph between those two. In addition, similar pattern can also be seen at the plot of MEDV and LSTAT when MEDV = 50, and the histogram represent the normal distribution except for the data when MEDV =50. That is why, we strongly believe that those data points are outlier and remove them immediately. 

![image](https://github.com/user-attachments/assets/30cf0bca-513a-4b7d-837b-7b9f009d16f6)

After removing outliners, the heatmap and scatter plots are sketched again. In this time, the correlation coefficient between RM, LSTAT and MEDV slightly increase to 0.73 and -0.76 respectively. Moreover, uncommon data points are disappeared and the histogram is normally distributed.

![image](https://github.com/user-attachments/assets/378b0523-d7c2-4c47-9a8c-f5e88c35bbbc)


After that, we applied different methods to solve the prediction problems:
1. Linear Regression
2. Neural Network method
3. Tree-based methods


