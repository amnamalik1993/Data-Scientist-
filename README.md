## Finding Sales Data Insights
## Forcasting Sales Using Machine Learning 

**Author**: 
Amna Malik 

### Business problem:
How to predict sales for the future? Sales prediction — also commonly called sales forecasting — is the process of estimating future sales by predicting the amount of product or services an individual salesperson, a sales team, or a company is likely to sell in a fixed time period i.e. next week, month, quarter, or year.



### Data Source:
The url for the data: https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view
For this dataset, there were 8523 rows and 11 columns.



## Data Preparation

- The data was cleaned. Duplicates were removed. Missing values were imputed. 
- Visualizations were made to demonstrate different findings.

## Exploratory Analysis

- During the exploratory data analysis, a boxplot and histogram was visualized for each numeric datatype column. 
- Also, a barplot was visualized for each categorical column. 
- This gave a good baseline for all of the numeric and categorical columns for univariate EDA.

<img width="827" alt="image" src="https://user-images.githubusercontent.com/124516948/224366122-a7d19eec-c658-4f21-a49a-7944f972902b.png">

## Expanatory Data Analysis

- To visualize the data for explantory purposes, many bargraphs were chosen and one linegraph was chosen.
- The bargraphs were chosen to show how the categories compare to each other. 

<img width="827" alt="image" src="https://user-images.githubusercontent.com/124516948/224367312-b755d18b-54f3-4759-93f0-765166a7f7e9.png">



The plot shows outlet sizes and that Medium size is more than the other two

## Analysis about which item type generates the most sales from this dataset

<img width="879" alt="image" src="https://user-images.githubusercontent.com/124516948/224371148-2e658e3f-1096-4eac-8748-13bab719c8a6.png">

The plot shows thatStarchy Foods is generating the most sales.

## Graphical Representation about the year that had the highest sales revenue.

<img width="854" alt="image" src="https://user-images.githubusercontent.com/124516948/224371756-899191fa-978b-40de-a217-a213c5154cbc.png">

The graph shows that most sales occurred before 1985. 


## Maching Learning Using the Following Models:

- Linear Regression Model
- Decision Tree Regressor Model
- Tuned Decision Tree Regressor Model

## Models Evaluated & Results
Linear Regression Model (Testing Set):
  - R^2 = -2.3054399434341525e+20
  - RMSE = 25220341873846.766
  
Decision Tree Regressor Model (Testing Set):
  - R^2 = 0.214
  - RMSE = 1472.942

Tuned Decision Tree Regressor Model (Testing Set):
  - R^2 = 0.596
  - RMSE = 1055.685


## Recommendations:

The final recommedation would be the Decision Tree Regressor / Regression Tree model.

This model performed well on the testing data after tuning the max depth.

It did lead to poor performance of training set after tunning the model. However it showed improved results with the testing data.

There was still some bias in the model, but by far it outperformed the linear regression model.


## Next Steps

Further modelling can also be performed like Random Forest that may show different results. 


### For further information


For any additional questions, please contact **amna.malik10@hotmail.com**
