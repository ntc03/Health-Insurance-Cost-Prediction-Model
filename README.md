# Health Insurance Cost Prediction Model

## Overview
This project explores a health insurance dataset to understand the factors affecting insurance charges. The primary goal is to analyze and visualize the relationships between features such as age, BMI, smoking status, and insurance costs. The insights gained from this exploratory data analysis (EDA) serve as a foundation for building predictive models.

## Dataset
### Features
- age: Age of the individual.
- sex: Gender of the individual.
- bmi: Body Mass Index (BMI) of the individual.
- children: Number of children covered by health insurance.
- smoker: Smoking status of the individual (yes or no).
- region: Geographic region where the individual resides.
- charges: Health insurance charge of the individual.
### Source 
[Kaggle US Health Insurance Dataset](https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset)

## Project Goals
- Perform an exploratory data analysis (EDA) to understand the dataset.
- Identify key factors driving health insurance costs.
- Train and evaluate a machine learning model to predict insurance charges.

## Key Insights from EDA
- 3 distinct trends between: nonsmokers, nonobese smokers, obese smokers
- Age, BMI, and smoking all have significant relationships with health insurance costs
- BMI does not impact the costs for nonsmokers; however, it does for smokers
- Smokers with a BMI of 30 or greater (obese), have an instant increase in insurance costs compared to nonobese smokers

## Model and Performance
Random Forest Regression model chosen to handle potentially non-linear relationships 
### Feature Engineering 
Added:
- BMI/Smoking Interaction Term
- Obesity Status: Indicator for individuals with BMI ≥ 30.
- Smoker's Obesity Status
### Filter Method / Tuning
- Used RFECV as a robust means of filtering method to search for important variables
- GridSearchCV to identify optimal hyperparameters for tuning prediction model 
### Evaluation Metrics
Baseline Model: 
- Mean Squared Error (MSE): 171117708 (untuned model with no feature engineering)
Optimized Model:
- MSE: 23102335
- R² Score: 0.86

## Next Steps
- Implement additional machine learning algorithms (e.g. XGBoost, Gradient Boosting, LightGBM)
- Achieve better performance with new algorithms
