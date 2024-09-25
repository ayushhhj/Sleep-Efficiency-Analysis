# Predicting Sleep Efficiency

## Project Overview

This project focuses on predicting sleep efficiency using a dataset sourced from Kaggle. Sleep efficiency is a critical measure of sleep quality, representing the proportion of time in bed spent sleeping. Through this analysis, we aim to understand the factors that most significantly impact sleep efficiency, providing valuable insights for improving sleep habits.

## Dataset

The dataset used in this project can be found on Kaggle: [Sleep Efficiency Dataset](https://www.kaggle.com/datasets/equilibriumm/sleep-efficiency). It includes 100 entries collected through self-reported surveys, actigraphy, and polysomnography.

### Variables in the Dataset

- **Response Variable:**

  - **Sleep Efficiency**: A numerical variable ranging from 0 to 1, representing the proportion of time in bed spent sleeping.

- **Explanatory Variables:**
  - **Age**: A numerical variable ranging from 6 to 69.
  - **Gender**: A categorical variable with 50% male and 50% female participants.
  - **Sleep Duration**: The total time spent sleeping (in hours).
  - **REM Sleep Percentage**: The percentage of total sleep time spent in the REM sleep stage.
  - **Deep Sleep Percentage**: The percentage of total sleep time spent in the deep sleep stage.
  - **Light Sleep Percentage**: The percentage of total sleep time spent in the light sleep stage.
  - **Awakenings**: The number of times a participant wakes up during the night.
  - **Caffeine Consumption**: The amount of caffeine consumed (in mg) 24 hours prior to bedtime.
  - **Alcohol Consumption**: The amount of alcohol consumed (in oz) 24 hours prior to bedtime.
  - **Smoking Status**: Whether the participant smokes or not.
  - **Exercise Frequency**: The number of times the participant exercises each week.

## Exploratory Data Analysis (EDA)

Exploratory analysis was performed on a training set (70% of the data). Notably:

- The gender ratio is balanced.
- Alcohol and caffeine consumption, as well as exercise frequency, show some skewness.
- **Collinearity**: A high correlation (0.975) was found between deep sleep percentage and light sleep percentage, leading to the exclusion of light sleep percentage from the models.

## Model Building

We developed several linear regression models to predict sleep efficiency. The final selected model includes the following predictors:

- **Age**
- **Deep Sleep Percentage**
- **REM Sleep Percentage**
- **Smoking Status**
- **Awakenings**
- **Exercise Frequency**

### Key Findings:

- A significant interaction was found between **Deep Sleep Percentage** and **Smoking Status**, improving the model's accuracy.
- **Adjusted R²**: 0.8418
- **RMSE**: 0.05519

The model demonstrates that **deep sleep**, **age**, **REM sleep**, and **exercise** positively affect sleep efficiency, while **smoking** and frequent **awakenings** have negative impacts.

## Results & Conclusions

The study revealed that selecting appropriate predictors is crucial for accurate model performance. Among the variables, **gender**, **caffeine consumption**, and **alcohol consumption** were less impactful in predicting sleep efficiency. Future improvements could involve collecting more detailed data, especially for alcohol consumption.

Overall, the model successfully highlights the importance of healthy lifestyle habits, including avoiding smoking and ensuring consistent exercise, to enhance sleep efficiency.
