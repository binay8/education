# Socioeconomic Factors Associated with ACT Scores
> 


## Project Overview

This project analyses the relationship between socio-economic factors and student ACT scores. We will be looking at various factors like median income, unemployment rate, household status, college attainment as well as participation in free or reductd lunch are associated with student academic performance.
The analysis uses exploratory data analysis (EDA), simple linear regression, and multiple linear regression. Results indicate that free/reduced-price lunch participation has the strongest negative adjusted association among the five socioeconomic predictors examined. The full regression model explains approximately 61.8% of the observed variation in average ACT scores.
  
- **Domain:** Education, Socio-economic impact
- **Key Techniques:** Exploratory Data Analysis, Regression Analysis.

---
## Project Structure

```
├── code/                 # Jupyter notebooks and Python scripts
├── data/                 # Raw and processed data
├── reports/              # Generated reports and visualizations
├── .gitignore            # Files and directory to be omitted in github
├── README.md             # Project documentation
└── requirements.txt      # Dependencies
 
```


## Data

EdGap: This dataset contains school average ACT scores as well as socio-economic indicators. **Source:** [EdGap](https://www.edgap.org/)
National Center for Education Statistics (NCES): This dataset has information about schools like state, school type, charter status, zipcode along with other categorical information. **Source:** [NCES](https://nces.ed.gov/ccd/pubschuniv.asp)

## Analysis
The analysis is organized into three Jypyter notebooks:
1. Data Preparation:
The data preparation process involved importing, investigating, cleaning, and merging the EdGap and school information datasets. Relevant variables were selected and renamed using consistent naming conventions. The datasets were merged using the school id, and missing values and potentially invalid numerical observations were investigated.
Observations with missing ACT scores were removed, while missing numerical predictor values were imputed using “IterativeImputer”, with predefined minimum and maximum bounds to maintain data validity. The resulting dataset contains 7,857 schools and 14 numerical and categorical variables, with no missing values in the selected analytical variables. The prepared data were exported as “education_final.csv” for exploration data analysis and regression modeling.
[Data Preparation Notebook Link](https://github.com/binay8/education/blob/master/code/01_data_preparation.ipynb)

2. Exploratory Data Analysis (EDA):
Exploratory data analysis was conducted using descriptive statistics and data visualizations to investigate distributions and potential relationship among various variables. Primarily histograms and boxplots were used to investigate distributions, central tendency, skewedness and outliers. Additionally, pair plots were used to access relationship between numerical variables. Finally, correlation analysis was conducted to investigate linear relationship among numerical predictors and average ACT scores.
[EDA Notebook Link](https://github.com/binay8/education/blob/master/code/02_exploratory_data_analysis.ipynb)

3. Regression Analysis:
Simple linear regression was conducted to investigate the relationship between lunch participation and average ACT scores. Multiple linear regression was used to analyze all numerical socio-economic predictors. Additionally, a categorical variable, charter status of school was used to analyze relationship to average ACT scores. Finally, we compared our regressions models using R-squared, Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
[Regression Analysis Notebook Link](https://github.com/binay8/education/blob/master/code/03_regression_analysis.ipynb)

## Results
Free/reduced-price lunch participation demonstrated the strongest negative association among the five socioeconomic predictors. The simple regression model explained approximately 60.5% of the observed variation in ACT scores, while the multiple regression model explained 61.8%. Unemployment rate, adult college attainment, and lunch participation were statistically significant predictors, whereas median household income and family structure were not significant after adjusting for other socioeconomic factors.
Charter-school status was statistically significant in the unadjusted model but was no longer significant after accounting for socioeconomic predictors. Among the four models compared, the reduced three-predictor model (M3), consisting of unemployment rate, adult college attainment, and lunch participation, provided a reasonable balance between simplicity and explanatory performance, with results nearly identical to the full five-predictor model. Overall, the findings highlight strong associations between socioeconomic conditions and academic achievement, particularly lunch participation, although these observational relationships do not establish causation.

## Authors

- Binay Raut - [@binay8](https://github.com/binay8)

## License


## Acknowledgements

- Python libraries used include pathlib, pandas, matplotlib.pyplot, numpy, seaborn, sklearn, statsmodels and scipy 

