# 🚢 Titanic Passengers Survival Prediction
A beginner data science project using Python and machine learning to explore the factors associated with passenger survival on the Titanic and build a model to predict whether a passenger survived.

## 📌 Project Overview

This project analyzes the Titanic passenger dataset and develops a machine learning classification model to predict whether a passenger survived or did not survive the Titanic disaster.

The project follows a complete data analysis and machine learning workflow, including data cleaning, exploratory data analysis (EDA), visualization, feature preparation, model training, and evaluation.

## 🎯 Problem Statement

The main question I focused on was:

> **What factors were associated with passenger survival on the Titanic, and can we use these factors to predict whether a passenger survived?**

Understanding these relationships provides an opportunity to apply the complete data science process, from data cleaning and exploratory data analysis to visualization and machine learning.

## 📂 Dataset

The dataset contains information about 891 Titanic passengers.
Some of the important columns used in the analysis include:
- `Survived` – Whether the passenger survived (0 = No, 1 = Yes)
- `Pclass` – Passenger class
- `Sex` – Passenger's sex
- `Age` – Passenger's age
- `SibSp` – Number of siblings/spouses aboard
- `Parch` – Number of parents/children aboard
- `Fare` – Passenger fare
- `Embarked` – Port where the passenger boarded


 🔎 My Approach

I followed a basic data science workflow consisting of four main stages:

## 🧹STAGE 1: Data Cleaning and Preparation

I first inspected the dataset for missing values and other data quality issues.
Missing values were handled before building the machine learning model. The `Age` column contained missing values, so the missing ages were replaced using the median age.The `Cabin` column contained a large number of missing values and was therefore excluded from the analysis.
Below is the workflow;
- Checked for missing values.
- Checked for duplicate records.
- Handled missing Age values using the median.
- Handled missing Embarked values using the mode.
- Removed the Cabin column because of its high proportion of missing values.
- Removed PassengerId before modeling because it is an identifier rather than a meaningful predictive feature.
- Encoded categorical variables.
- Split the dataset into training and testing sets.
- Standardized numerical features before model training.

## 🔍STAGE 2: Exploratory Data Analysis

I explored the dataset to understand the characteristics of the passengers and identify relationships between passenger information and survival.
### Key Statistics
- Total passengers: **891**
- Passengers who survived: **342**
- Passengers who did not survive: **549**
- Overall survival rate: **38.38%**
- Average age: **29.36 years**
- Average fare: **32.20**

## 📊 My Findings

### Survival by Sex
Female passengers had a survival rate of 74.20%, compared with 18.89% for male passengers.
### Survival by Passenger Class
| Passenger Class | Survival Rate |
|---|---:|
| 1st Class | 62.96% |
| 2nd Class | 47.28% |
| 3rd Class | 24.24% |
The analysis shows a substantial association between passenger class and survival rate.
### Survival by Age
The average age of passengers who survived was 28.29 years, while passengers who did not survive had an average age of 30.03 years. The median age for both groups was 28 years.

## 📈 STAGE 3: Data Visualizations
I created different charts using Matplotlib and Seaborn to make the patterns in the dataset easier to understand.
Some of the visualizations included:

![Age Distribution](Age_Distribution.png) - Helped understand the age distribution of passengers.
![Survival by Sex](survival_by_sex.png) - Showed a clear difference in survival between male and female passengers.
![Survival by Class](survival_by_class.png) - Showed differences in survival across 1st, 2nd, and 3rd class passengers.
![Confusion Matrix](Confusion%20Matrix%20-%20Titanic_survival.png) - Helped to evaluate how well the classification model is performing on the prediction model against the actual outcomes

## 🤖 STAGE 4: Machine Learning Model
Since the target variable, `Survived`, is binary (0 or 1), I used **Logistic Regression** as the machine learning model.
The dataset was prepared by converting categorical variables into a format suitable for machine learning and splitting the data into training and testing sets.
- `0` = Did Not Survive
- `1` = Survived
## 📊 Model Evaluation
The Logistic Regression model achieved an overall accuracy of:
### **80.45%**
The confusion matrix was:
[[98 12]
 [23 46]]
The confusion matrix helped me evaluate how well the model distinguished between passengers who survived and those who did not.
Rather than relying only on accuracy, the confusion matrix provided a more detailed view of the model's predictions, including correct and incorrect classifications.

 
 ## 💡 Key Findings
One of the major findings from the exploratory analysis was that **sex and passenger class were strongly associated with survival**.
Female passengers generally had a much higher survival rate (74.20%) than male passengers (18.89%).
Passenger class also showed an important relationship with survival. Passengers in higher classes generally had better survival outcomes than passengers in lower classes.
This demonstrates how exploratory data analysis can reveal meaningful patterns before applying a machine learning model.

### Most Interesting Finding
The most interesting finding from this project was the difference in survival outcomes between male and female passengers.
The analysis showed that survival was not evenly distributed across the passenger population, with female passengers having substantially better survival outcomes.

### 🚀 What I Would Do Next

If I continued working on this project, I would:
Try other classification models such as Random Forest and Decision Tree.
Compare the performance of different models.
Perform hyperparameter tuning to improve model performance.
Engineer additional features from the existing passenger information.
Evaluate the model using additional metrics such as precision, recall, and F1-score.
Use cross-validation to obtain a more reliable estimate of model performance.

### 📚 What I Learned
This project helped me understand the practical steps involved in a data science workflow.
Through the project, I gained hands-on experience in:
Loading and inspecting a dataset
Identifying and handling missing data
Performing exploratory data analysis
Creating data visualizations
Identifying relationships between variables
Preparing data for machine learning
Training a classification model
Evaluating model performance
Communicating data-driven findings

### 🏁 Conclusion
The analysis demonstrates that passenger characteristics such as sex, passenger class, age, and fare contain useful information for predicting Titanic survival. The Logistic Regression model achieved an accuracy of 80.45%, indicating reasonably good predictive performance on the test dataset. The confusion matrix and classification metrics provide additional insight into the types of errors made by the model. These findings describe associations within the dataset and should not be interpreted as proof that any individual characteristic directly caused survival.

### 🛠️ Tools and Technologies
The following Python libraries and tools were used:
-Python
-Pandas – Data manipulation and analysis
-NumPy – Numerical computations
-Matplotlib – Data visualization
-Seaborn – Statistical visualization
-Scikit-learn – Machine learning
-Jupyter Notebook
-VS Code
-Git & GitHub

### 👩‍💻 Author
Eya Chinyere Euphemia
Data Science Learner | Power Distribution Operations Professional
