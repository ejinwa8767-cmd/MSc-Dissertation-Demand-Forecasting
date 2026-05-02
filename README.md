# Retail Business Demand Forecasting Using Machine Learning Models

## Project Overview
This project investigates whether machine learning models can improve the accuracy and reliability of retail business demand forecasting. The study uses historical Walmart retail sales data and follows the CRISP-DM framework to support a structured process from data understanding to deployment.
The project compares a traditional time-series baseline with machine learning models and develops a practical forecasting prototype for retail decision-making.

## Research Question
Can machine learning models improve the accuracy and reliability of retail demand forecasting compared to traditional approaches?

## Aim
This study evaluates whether machine learning models improve the accuracy and reliability of retail demand forecasting.

## Objectives
1. To prepare and validate historical retail sales data for time-series forecasting  
2. To develop three forecasting models: Prophet, Random Forest, and XGBoost  
3. To apply feature engineering techniques  
4. To evaluate model performance using RMSE, MAE, and MAPE  
5. To compare machine learning models with a traditional time-series baseline  
6. To develop a practical forecasting framework for retail decision-making  

## Methodology (CRISP-DM)
The project follows the CRISP-DM framework:
- Business Understanding  
- Data Understanding  
- Data Preparation  
- Modelling  
- Evaluation  
- Deployment  

A quantitative research design was adopted using historical retail sales data. Primary feedback was also collected using KoboToolbox to evaluate the usability of the forecasting prototype.

## Dataset
The study uses the Walmart retail sales dataset, consisting of 6,435 observations across 13 variables, including:
- Store  
- Date  
- Weekly_Sales  
- Holiday_Flag  
- Temperature  
- Fuel_Price  
- CPI  
- Unemployment  

## Feature Engineering
To improve forecasting performance, the following features were created:
- lag_1 (previous week sales)  
- lag_4 (sales from four weeks prior)  
- rolling_mean_4 (4-week moving average)  
- rolling_std_4 (4-week rolling standard deviation)  
- Year, Month, Week (calendar features)  

## Models Developed
### Prophet
A traditional time-series model used as a baseline to capture trend and seasonality.

### Random Forest
An ensemble machine learning model designed to capture nonlinear relationships in retail demand.

### XGBoost
A gradient boosting model that iteratively improves predictive performance and captures complex demand patterns.

## Model Performance

| Model          | RMSE         | MAE          | MAPE (%) | R²     |
|----------------|-------------|--------------|----------|--------|
| XGBoost        | 1,270,983.7 | 918,514.8    | 1.98     | 0.4793 |
| Prophet        | 1,403,605.4 | 1,078,463.1  | 2.30     | 0.3650 |
| Random Forest  | 1,815,156.9 | 1,444,502.9  | 3.14     | -0.062 |

### Performance Ranking
XGBoost > Prophet > Random Forest

## Key Findings
- XGBoost achieved the highest forecasting accuracy  
- Prophet captured trend and seasonality but smoothed short-term fluctuations  
- Random Forest showed the weakest performance  
- Feature engineering significantly improved predictive capability  

## Deployment
The best-performing model (XGBoost) was implemented in a forecasting prototype that:
- Generates weekly demand predictions  
- Compares actual vs predicted sales  
- Classifies demand into Low, Moderate, and High categories  
- Supports retail decision-making  

## Usability Evaluation
A usability evaluation was conducted using KoboToolbox:

- Mean usability score: 3.21  
- Users found outputs clear and informative  
- Interface design requires improvement  

## Project Structure
```
MSc-Dissertation-Demand-Forecasting/
│
├── notebooks/
│   ├── EDA.ipynb
│   ├── Data_Preparation.ipynb
│   ├── Modelling.ipynb
│   ├── Deployment.ipynb
│   └── Usability_Evaluation.ipynb
│
└── README.md
```
## Tools & Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn)  
- Scikit-learn  
- XGBoost  
- Prophet  
- Statsmodels  
- Google Colab  
- KoboToolbox  
- Google Drive  

## Conclusion
The study demonstrates that machine learning models, particularly XGBoost, significantly improve retail demand forecasting accuracy. Temporal feature engineering played a critical role in capturing demand patterns, and the developed prototype shows strong potential for real-world retail decision support.

## Limitations
- Use of a single dataset limits generalisability  
- Small usability sample size  
- Prototype remains at demonstration level  
- External variables showed weaker predictive influence  

## Recommendations
- Evaluate additional retail datasets  
- Explore deep learning approaches  
- Improve prototype interface design  
- Conduct larger-scale usability testing  

## Author
Chinwe Nkiruka Ajagu  
MSc Dissertation  
Leeds Beckett University  

## Academic Use
This repository is for academic purposes only.

