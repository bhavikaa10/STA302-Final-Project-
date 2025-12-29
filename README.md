# STA302 Final Project- Exploring the Effects of Lifestyle Habits on HDL Cholesterol Levels

## Project Overview
This project examines whether lifestyle choices—specifically smoking, physical activity, sleep duration, and alcohol consumption—significantly affect HDL (high-density lipoprotein) cholesterol levels in U.S. adults, while controlling for demographic characteristics such as sex, race, and age.

HDL cholesterol is an important component of blood lipids and plays a crucial role in cardiovascular health. Prior research suggests that increases in HDL cholesterol are associated with reductions in heart disease risk. Given the continued prevalence of cardiovascular disease in the United States, this project aims to better understand how modifiable lifestyle behaviors relate to HDL cholesterol levels using nationally representative health data.

This project was completed as part of **STA302 (Applied Statistics), Fall 2025**, at the University of Toronto.

---

## Research Question
Do lifestyle behaviors—smoking status, physical activity, sleep duration, and alcohol consumption—have a significant effect on HDL cholesterol levels in U.S. adults after controlling for demographic factors such as sex, race, age, income, and diabetes status?

---

## Data Description
### Data Source
The analysis uses data from the **2009–2010 National Health and Nutrition Examination Survey (NHANES)**, collected by the U.S. Centers for Disease Control and Prevention (CDC). The NHANES dataset combines household interviews, standardized physical examinations, and laboratory tests to monitor national health and nutrition trends.

The data were accessed using the **NHANES R package**.

### Sample
After filtering for adult respondents, the dataset contains over 1,000 observations.

### Variables
- **Response Variable**
  - Direct HDL Cholesterol (mmol/L)

- **Predictor Variables**
  - Smoking status
  - Physical activity (days active per week)
  - Sleep duration (hours per night)
  - Alcohol consumption (drinks per drinking day)
  - Demographic and health controls, including:
    - Sex
    - Race
    - Age
    - Household income
    - Diabetes status

---

## Methodology
The study employs a **multiple linear regression model** to quantify the relationship between HDL cholesterol and several predictors simultaneously. This approach allows for the isolation of each lifestyle factor’s effect on HDL cholesterol while holding other variables constant.

The analysis includes:
- Exploratory data analysis using summary statistics, histograms, scatterplots, and boxplots
- Multiple linear regression with both continuous and categorical predictors
- Inclusion of a **gender × alcohol consumption interaction term**, motivated by both prior literature and observed differences in fitted slopes
- Residual diagnostics to assess:
  - Linearity
  - Normality
  - Constant variance
- Use of t-tests to assess individual predictors and F-tests to compare models

---

## Preliminary Results
Preliminary regression results indicate that several demographic and lifestyle variables are associated with HDL cholesterol levels. Gender, age, income, diabetes status, and physical activity emerge as significant predictors in the initial model. While smoking, alcohol consumption, and sleep duration are not individually significant once other variables are included, the interaction between gender and alcohol consumption is statistically significant, suggesting differing HDL responses between men and women.

Residual diagnostics reveal mild violations of normality and potential non-constant variance, particularly related to alcohol consumption.

---

## Planned Model Refinements
To address diagnostic issues observed in the preliminary model, the following steps are planned:
- Apply a **Box–Cox transformation** to the response variable (Direct HDL Cholesterol) to improve normality and linearity
- Reassess model assumptions using residual plots
- Examine **multicollinearity** using Variance Inflation Factors (VIFs)
- Use partial F-tests to compare reduced and full models
- Select a final model with improved assumption validity and narrower confidence intervals

---

## Ethics Considerations
The data used in this project come from NHANES, a federally administered survey that ensures participant consent, privacy, and confidentiality. All data are de-identified and collected using standardized procedures. The NHANES study is overseen by an Ethics Review Board, and the dataset is widely used by government agencies, academics, and public health researchers. These factors support the ethical and reliable use of the data for statistical analysis.

---

## Presentation
A link to the project presentation is provided below:

https://utoronto-my.sharepoint.com/:v:/g/personal/vedika_patil_mail_utoronto_ca/IQA72GHGWufvRpnqQvF7mwNJARPxkAdojD8e_-tfJ3kCs0E?e=HSDsBa&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

---

## Authors
- Vedika Patil
- Mariana Garcia Mejia
- Bhavikaa Goenka

