GROUP 5 : Predicting Video Game Sales
---
## Team Members

- Kodicherla, Vishnu 
- Verma, Deepika


## Problem Statement

As Data Scientists for a large gaming company in the united states, we were provided data on games and sales from a kaggle competition, to look into a providing the company some benefit, a regression problem will be made to predict sale procies from each od the different video games. The different models that were made were Linear Regression and Random Forest. A successful model would have a lower RMSE score compared to the baseline model.

- [Video Game Sales Prediction](https://www.kaggle.com/rush4ratio/video-game-sales-with-ratings)


## Items in this Repo
1) "code" folder containing:

    - 01.1-Video-Data-Cleaning-and-EDA

2) "data" folder containing:

    - Video_Games_Sales_as_at_22_Dec_2016
    
## The Data 

The data contains several columns that could factor into the sales figures (millions of units) like Critic_score,
User_score, platform, publisher, Rating  etc. 

## Data Cleaning and EDA

There were a lot of columns with null values in this dataset, some of rows with null values were dropped for the columns of interest including name, year of release, genre, and publisher and some of the columns with large number of null values were dropped including critic count and user count. 
As part of EDA, we looked at the distribution of global sales and NA sales, and dropped some of the outliers. One game Wii sports had over 80 (million units sold) which was dropped due to it being a large outlier. 
We also visualized relationship between the features and target variable (NA sales) as well as correaltion between different features, and found linearilty between various 'sales' columns and NA sale which was expected. 

We also looked at the highest values counts of some of the features and found some interesting results like the most sold units belong to PS2 and DS platform.

## Data Pre-processing

During the Pre-processing we began by doing a train test split. Due to a large number of null values from some of the columns, we imputed some of the columns with Iterative imputer with Linear regression for the numerical columns. Afterwards, we dummified our categorical features and used Standard Scaler to scale numerical features for Linear Regression models. 


## Modeling/Prediction

We started with Linear Regression model and got really high score which indicated we might have some multicollinearity. We then did VIF to find the highly correlated features and dropped them. We looked into any features that had a vif score higher than 5 and one of them was critic score. After looking at the vif, we then continued to fit Linear Regression, Ridge and Random Forest.


## Findings/Recommendations

Our best model is Random Forest with training R2 score of 0.77 and testing R2 score of 0.46 with RMSE of 0.69. Even though there was overfit seen from the training and testing score, the RMSE did better than the baseline model which was 0.93. 

The baseline testing R2 score is -0.00013 and RMSE is 0.94.


## Potential Areas for Model Improvement
Our best model still has low testing R2 score and is over-fit.
The model can be improved by adding in the 'Rating' column which might have added value in predictions. 
Several other regression modeling techniques can be tried like AdaBoot, GradientBoost etc.



---

