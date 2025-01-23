# Predicting-Recidivism-Based-On-Previous-Criminal-History

**Recidivism:**
Recidivism refers to the tendency of a convicted criminal to reoffend after having been previously punished or released from Prism.

This Analysis is part of the National Institute of Justice (NIJ) Recidivism Forecasting Challenge, which focuses on improving recidivism prediction using advanced data analysis to support fair and effective criminal justice outcomes.

**Dataset Description:**

The dataset used in the NIJ Recidivism Forecasting Challenge consists of records from the State of Georgia, covering individuals released from prison to parole supervision between 2013 and 2015. 

The dataset contains  various attributes related to individuals released from prison. Below is a brief description of the key columns:
**Race:** Categorical data representing the racial background of individuals (e.g., BLACK, WHITE).

**Age_at_Release:** Age group category at the time of release (e.g., 33-37, 48 or older).

**Gang_Affiliated:** Boolean value indicating whether the individual was associated with a gang (True/False).

**Supervision_Level_First:** The initial level of supervision assigned upon release (e.g., Standard, High, Specialized).

**Education_Level:** Educational attainment before incarceration (e.g., Less than HS diploma, At least some college).

**Dependents:** Number of dependents the individual has (e.g., 1, 3 or more).

**Prison_Offense:** Type of offense leading to imprisonment (e.g., Drug, Violent/Non-Sex, Property).

**Prison_Years:** Length of imprisonment (e.g., 1-2 years, More than 3 years).

**Prior_Arrest_Episodes_Felony:** Number of prior felony arrest episodes (e.g., 4, 6 or more).

**Prior_Arrest_Episodes_Misd:** Number of prior misdemeanor arrest episodes.

**Prior_Arrest_Episodes_Drug:** Number of prior drug-related arrest episodes.

**Prior_Conviction_Episodes_Felony:** Number of prior felony convictions.

**Prior_Conviction_Episodes_Misd:** Number of prior misdemeanor convictions.

**Prior_Conviction_Episodes_Drug:** Number of prior drug-related convictions.

**Residence_Changes:** Number of changes in residence during supervision.

**Recidivism_Within_3years:** Boolean indicating whether the individual reoffended within three years (True/False).

**Drug_Test_Positive:** Boolean indicating if the individual tested positive for drugs during supervision.

**Employment_Status:** Employment status after release (e.g., Employed, Unemployed).

**Problem Statement:** 

Determine factors that are most significant in predicting recidivism three years after being released from prison.

**Approach:**

![image](https://github.com/user-attachments/assets/bcdc1387-6d8f-4574-aaad-c47e2f90cca8)

￼
**Data Preprocessing:**

The dataset was loaded into Excel, where data cleaning tasks such as handling missing values and standardizing data were performed using power Query editor.

**Exploratory Data Analysis (EDA):**

The dataset was loaded into Power BI, where an interactive dashboard was developed to analyze key trends and patterns related to recidivism. 

Necessary calculated columns and measures were created using DAX (Data Analysis Expressions) in Power BI to enhance data insights and support the development of meaningful visual representations.

**Power BI Dashboard:**

<img width="572" alt="Power BI Dashboard_Recidivism Analysis" src="https://github.com/user-attachments/assets/febf1048-8de4-42fc-817d-c326f0ce7cac" />


**Feature Selection:**

Three different methods were used to select the most important features influencing recidivism:

Random Forest Feature Importance: A Random Forest model was trained, and the top 10 significant features were selected.

Chi-Square Test: Statistical significance of categorical variables was tested to determine their impact on recidivism.

Stepwise Regression: A forward and backward stepwise selection approach was applied to identify the most relevant predictors.

**Model Development**

Different logistic regression models were built using selected features from each feature selection method.

The dataset was split into training (80%) and testing (20%) sets to validate model performance.

Logistic regression was used to predict recidivism outcomes.

**Model Evaluation**

AUC (Area Under the Curve): AUC values were compared for different models to determine the best-performing approach.

Based on the AUC and accuracy metrics, the logistic regression model built by stepwise feature selection was chosen as the final model.

**Results and Conclusion:**

The most significant factors in predicting recidivism three years after being released from prison include:

Age at Release: Younger individuals are more likely to re-offend, with those in older age groups showing a lower chance of re-offending.

Gang Affiliation: People who are part of gangs have a higher chance of committing crimes again after being released.

Prior Arrests: Individuals with a history of more arrests, especially for serious crimes, are more likely to re-offend.

Prison Offense Type: Those convicted of property crimes are more likely to re-offend, while those convicted of violent or sexual offenses 
tend to have a lower chance of re-offending.

Employment Status: Unemployed individuals are more likely to re-offend, as having a job seems to lower the risk of re-offending.

Prison Time Served: Those who served less than a year in prison are more likely to re-offend, while those who served between 2 to 3 years show a slightly reduced risk.

Residence Changes: People who changed residences multiple times after release are more likely to re-offend, with those having three or more moves showing the highest risk.

Supervision Level: Individuals under standard supervision have a lower chance of re-offending, suggesting that more supervision reduces the likelihood of recidivism.


