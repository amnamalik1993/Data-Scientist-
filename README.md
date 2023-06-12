## Finding Sales Data Insights
## Forcasting Sales Using Machine Learning 

**Author**: 
Amna Malik 

### Business problem:
How to predict sales for the future? Sales prediction — also commonly called sales forecasting — is the process of estimating future sales by predicting the amount of product or services an individual salesperson, a sales team, or a company is likely to sell in a fixed time period i.e. next week, month, quarter, or year.



## Data Source:
The url for the data: https://drive.google.com/file/d/1syH81TVrbBsdymLT_jl2JIf6IjPXtSQw/view

For this dataset, there were 8523 rows and 11 columns.

## Data Dictionary: 
<img width="571" alt="Data dictionary" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/32db2fa5-8061-4ed7-a007-f7a1766d7279">


## Data Preparation

- Processed the data by removing duplicates
- Replaced the missing values in the Item_Weight column with 'Missing'.
- Replaced the missing values in the Outlet_Size column with the median Outlet_Size so that those missing data could still be counted with the most common variable.
- Removed the Outlet_Establishment_Year column because it is unnecessary in the Sales Predictions for the Outlet_Sales
- Corrected the values of Item_Fat_Content to gain uniformity in the values presented

## Exploratory Analysis

- During the exploratory data analysis, a boxplot and histogram was visualized for each different datatype column. 
- Also, a barplot was visualized for each categorical column. 
- This gave a good baseline for all of the numeric and categorical columns for univariate EDA.

<img width="827" alt="image" src="https://user-images.githubusercontent.com/124516948/224366122-a7d19eec-c658-4f21-a49a-7944f972902b.png">

## Explanatory Data Analysis

- To visualize the data for explantory purposes, many bargraphs and scatter plots were created and one linegraph.
- The bargraphs were chosen to show how the categories compare to each other.
-  
<img width="668" alt="scatter plot" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/680b1622-94c9-4c5d-9e06-c7e3e3d5a029">

<img width="674" alt="scatter plot1" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/939feae5-4a57-4527-8fa9-f7c9a275796d">

**Top 3 Most Impactful Features:**

- Outlet_Type - Depending upon the location, positively influences the sales price of items.
- Outlet_Size - The size of the outlet positively influences the sales price.
- Item_Type_Seafood - The product category of Seafood also positively influences the sales price.

<img width="542" alt="Screenshot 2023-06-12 001910" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/467c96f8-8569-4997-ba62-9939c0076e60">

**Top 5 Most Important Features:**

- Item_MRP
- Outlet_Type
- Item_Visibility
- Item_Weight
- Outlet_Size

<img width="557" alt="Screenshot 2023-06-12 002643" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/d96b2c26-9006-4e9b-b33e-5037f4969d4f">

<img width="557" alt="Screenshot 2023-06-12 002943" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/9b7920aa-043d-4001-a06a-2c2b49a0d260">

Both SHAP and the Original Feature Importances have the same top 5 chosen importances.

**Global SHAP Findings:**

<img width="490" alt="Screenshot 2023-06-12 003509" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/6228555c-88fe-49dd-930e-1013e7a66541">

**Local SHAP/LIME Findings:**

Group 1:

- High Item_MRP
- Smaller Outlet_Type
- Low Item_Visibility
- Low Item Weight
- Smaller Outlet_Size

<img width="564" alt="Screenshot 2023-06-12 003759" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/5a519abc-25db-4c86-a2db-dc35ab7a0483">

As we can see in the force plot for group 1:

Item_MRP is a strong factor pushing towards a higher sales prediction.

Decreasing factors are: Item_Visibility, Item_Weight and Outlet_Size.

<img width="628" alt="Screenshot 2023-06-12 004255" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/eca8711b-e48c-457e-9eec-bacc19db2749">

It is evident from the LIME explanation above for Group 1, there are many factors pushing for a higher sales prediction:

Item_MRP
Item_Type_Hard Drinks

**Group 2:**

- Low Item_MRP
- Smaller Outlet_Type
- Low Item_Visibility
- Low Item Weight
- Smaller Outlet_Size

<img width="586" alt="Screenshot 2023-06-12 004651" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/063a4c41-b889-47a2-8fc3-be46c4175955">

As we compare to Group 1, Item_MRP is still a large influence on pushing the sales prediction higher, it is evident that there is slightly more influence now from Item_Visibility and Outlet_Type pushing towards the higher sales prediction When Item_MRP is lower.

Decreasing factors for Group 2 are as follows:

- Item_Weight
- Item_Type_Dairy
- Outlet_Size

<img width="634" alt="Screenshot 2023-06-12 004918" src="https://github.com/amnamalik1993/Sales-Prediction/assets/124516948/a736a2c0-0ec7-4eed-b243-b0443d535291">

Based on the LIME explanation above for Group 2, there are factors pushing for a higher sales prediction.

Contributing factors are:

- Item_MRP
- Item_Visibility
- 
Item_MRP is still a major factor in the sales prediction, but with Group 2 representing lower MRP, we can see more influence from the actual Item Type and Item Visibility.

### Models Evaluated & Results:

The final model that was chosen to be used was the RandomForestRegressor Model.

After processing it and breaking it down, it was the best choice by far.

The R^2 values were found to be:

Training Data: 61% 

Testing Data: 60% 

With an overall RMSE of $1060.31

## Reccomendations:

This model can be used and it may provide useful predictions if the company decides to go for it.

## Next Steps:

Further modelling can also be performed like Random Forest that may show different results.

## For further information
For any additional questions, please contact amna.malik10@hotmail.com

