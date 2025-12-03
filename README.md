Stroke Risk Prediction using Logistic Regression in R

Project Overview

Stroke is one of the leading causes of death and disability worldwide. In this project, I developed a logistic regression model to predict the likelihood of stroke based on patient demographic and clinical attributes. The goal was to understand meaningful risk factors and build a model that can support early identification and prevention strategies.

About the Dataset
The dataset includes the following variables:
gender
age
hypertension
heart_disease
ever_married
work_type
Residence_type
avg_glucose_level
bmi
smoking_status
stroke (target: 0 = no stroke, 1 = stroke)
Note: Stroke cases are only about 5% of the dataset, requiring class imbalance handling (used ROSE package to handle the imbalancing).

⚙️ Methods & Workflow

1. Data Cleaning & Preprocessing
Converted categorical variables to factors
Converted BMI to numeric and handled missing values
Removed anomalies (e.g., “Other” gender category)
2. Exploratory Data Analysis (EDA)
Age distribution
Glucose level distribution
Stroke occurrence by health factors
Correlation / relationships
3. Handling Class Imbalance
Since stroke = only ~5%, I used the ROSE (Random Over Sampling Examples) technique to generate a balanced training set.
4. Model Building
Used Logistic Regression:
stroke ~ age + hypertension + heart_disease + avg_glucose_level + ...
5. Model Evaluation
Confusion matrix
Sensitivity & specificity
ROC curve
AUC score

Results
Accuracy ≈ 75%
ROC–AUC = 0.846

Good sensitivity in identifying stroke cases

Key predictors were:
Age
Hypertension
Average glucose level
Smoking status
Heart disease (weak predictor)

Key Insights
Stroke risk rises with age
Higher glucose levels correlate with stroke
Existing heart disease and hypertension increase risk
Smoking history is a relevant risk factor

Files in This Repository
File	Description
StrokePrediction_AishwaryaKrishnamohan.Rmd	---> R Markdown file with full analysis
StrokePrediction_AishwaryaKrishnamohan.html	---> Rendered project report
healthcare-dataset-stroke-data.csv ---> Dataset used
README.md	---> Project description

Running the Project
Requirements:
Install packages in R:
install.packages("tidyverse")
install.packages("caret")
install.packages("ROSE")
install.packages("pROC")

Load libraries:
library(tidyverse)
library(caret)
library(ROSE)
library(pROC)

Then open this R Markdown file below and knit:
StrokePrediction_AishwaryaKrishnamohan.Rmd 

Skills Demonstrated

- R programming
- Data preprocessing
- Imbalanced data handling
- Logistic regression modeling
- Statistical inference
- ROC–AUC analysis
- Reproducible reporting with R Markdown
- GitHub documentation best practices
  
Future Improvements
- Try tree-based models (Random Forest, XGBoost)
- Build a Shiny app for interactive prediction
- Add model explainability (SHAP values)


Author

Aishwarya Krishnamohan

PhD in Cell & Molecular Biology

Data Science focus in biomedical analytics
