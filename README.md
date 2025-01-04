# HeartGuard Insights

**HeartGuard Insights** is a predictive system that determines the likelihood of an individual having heart disease based on various medical attributes. The system uses machine learning techniques to build a logistic regression model for prediction.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Steps Performed](#steps-performed)
- [Conclusion](#conclusion)

## Overview
**HeartGuard Insights** uses a dataset containing various medical attributes such as age, sex, cholesterol levels, and more to predict the possibility of heart disease. The project demonstrates how to preprocess data, train a model, evaluate performance, and use the model for predictions.

## Features
- Data preprocessing and exploration
- Logistic regression model training
- Evaluation of model performance on training and test datasets
- Predictive system for individual cases
- Model serialization using pickle for reuse

## Dataset
The dataset used in this project is stored in `heart.csv` and includes the following features:

| Feature    | Description                                              |
|------------|----------------------------------------------------------|
| age        | Age of the individual                                    |
| sex        | Gender (1 = male, 0 = female)                            |
| cp         | Chest pain type (0-3)                                    |
| trestbps   | Resting blood pressure (mm Hg)                           |
| chol       | Serum cholesterol (mg/dl)                                |
| fbs        | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)    |
| restecg    | Resting electrocardiographic results (0-2)               |
| thalach    | Maximum heart rate achieved                              |
| exang      | Exercise-induced angina (1 = yes, 0 = no)                |
| oldpeak    | ST depression induced by exercise                        |
| slope      | Slope of the peak exercise ST segment                    |
| ca         | Number of major vessels (0-4) colored by fluoroscopy     |
| thal       | Thalassemia (0-3)                                        |
| target     | Target variable (1 = defective heart, 0 = healthy heart) |

## Technologies Used
- **Python** for data processing and model implementation
- **Pandas** for data handling
- **Scikit-learn** for machine learning algorithms and evaluation
- **Pickle** for model serialization

## Steps Performed

1. **Data Collection and Processing**  
   The dataset was loaded using Pandas.  
   Basic exploratory data analysis (EDA) was performed to understand the dataset.  
   Checked for missing values and verified that there are no null entries.  
   Generated statistical summaries using `describe()`.

2. **Splitting the Data**  
   Features (X) and target (Y) were separated.  
   The dataset was split into training and testing sets using an 80-20 ratio, ensuring stratified sampling.

3. **Model Training**  
   A logistic regression model was used.  
   The model was trained on the training dataset.

4. **Model Evaluation**  
   Accuracy scores were calculated for both the training and test datasets.  
   Training Accuracy: 85.24%  
   Test Accuracy: 80.49%

5. **Building a Predictive System**  
   A predictive system was built to take user input and predict whether the person has heart disease.  
   Example input: `(62, 0, 0, 140, 268, 0, 0, 160, 0, 3.6, 0, 2, 2)` resulted in the output:  
   *The Person does not have a Heart Disease.*

6. **Saving the Model**  
   The trained model was saved using Python's **pickle** module for future use.

## Conclusion

In this project, we developed a predictive system called **HeartGuard Insights**, which utilizes a logistic regression model to determine the likelihood of an individual having heart disease based on medical attributes. By following a systematic approach of data preprocessing, splitting, model training, and evaluation, we achieved good performance with an accuracy of **85.24%** on the training set and **80.49%** on the test set.

The model was further integrated into a user-friendly predictive system that can take individual inputs and predict whether a person is at risk of heart disease. Additionally, the trained model was saved using Python's **pickle** module to facilitate future use and deployment.

This project demonstrates how machine learning can be applied to healthcare for early detection and prediction, potentially helping in the prevention of heart disease by providing quick and reliable insights based on medical data.
