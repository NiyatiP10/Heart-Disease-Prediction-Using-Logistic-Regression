# Heart Disease Prediction Using Logistic Regression

## Overview

This project aims to predict the likelihood of cardiovascular disease (CVD) within a 10-year period using Logistic Regression. It leverages a dataset from the Framingham Heart Study, containing patient data with 15 attributes across over 4,000 records. The objective is to analyze and predict coronary heart disease (CHD) occurrences based on patient-specific attributes such as age, cholesterol levels, smoking habits, and blood pressure.

This analysis also explores the data through visualization, evaluates the predictive performance of the Logistic Regression model, and provides insights into potential risk factors contributing to CHD.

---

## About Logistic Regression

Logistic Regression is a statistical method used for binary or multi-class classification problems. It predicts a dependent variable (outcome) based on one or more independent variables (features). This method estimates the probability of an event occurring and is ideal for binary classification tasks like this one.

---

## Dataset Information

The dataset used in this project originates from the **Framingham Heart Study**, which focuses on cardiovascular health. The dataset includes attributes such as:

- **Age**: Age of the patient
- **Sex_male**: Gender of the patient (1 = Male, 0 = Female)
- **CigsPerDay**: Number of cigarettes smoked per day
- **TotChol**: Total cholesterol level
- **SysBP**: Systolic blood pressure
- **Glucose**: Glucose level
- **TenYearCHD**: Binary target variable indicating whether the patient is at risk of CHD in the next 10 years (1 = Yes, 0 = No)

The dataset was cleaned to remove missing values, resulting in a total of **3,751 records** and **15 attributes** after preprocessing.

---

## Steps of the Project

### 1. **Data Preparation**
   - Loaded the dataset using pandas.
   - Renamed columns for clarity and dropped unnecessary attributes like `education`.
   - Handled missing values by removing rows with null entries.

### 2. **Exploratory Data Analysis (EDA)**
   - Conducted visualizations to identify trends and patterns in the dataset.
   - Counted the number of patients affected by CHD and created a bar chart using `seaborn`.
   - Analyzed the distribution of the target variable `TenYearCHD`.

### 3. **Feature Selection**
   - Selected relevant features (`age`, `Sex_male`, `cigsPerDay`, `totChol`, `sysBP`, and `glucose`) for prediction based on correlation analysis.

### 4. **Data Normalization and Splitting**
   - Normalized feature data using `StandardScaler` to improve model performance.
   - Split the data into training (70%) and testing (30%) subsets using `train_test_split`.

### 5. **Logistic Regression Model**
   - Implemented a Logistic Regression model using `scikit-learn`.
   - Trained the model on the training dataset and made predictions on the test dataset.

### 6. **Model Evaluation**
   - Evaluated model performance using metrics such as:
     - **Accuracy**: Overall performance of the model.
     - **Precision**: True positive predictions relative to all positive predictions.
     - **Recall**: True positive predictions relative to all actual positives.
     - **F1-Score**: Weighted harmonic mean of precision and recall.
   - Visualized the confusion matrix using `seaborn` for a detailed breakdown of predictions.

---

## Key Results

- **Accuracy of the Model**: 84.90%
- **Precision for CHD Prediction**: 61%
- **Recall for CHD Prediction**: 8%
- **F1-Score**: 0.14

These results highlight the challenges of dealing with imbalanced datasets, as the model struggled to recall positive CHD cases accurately despite achieving high overall accuracy.

---

## Visualizations

### 1. **Bar Chart of CHD Cases**
   This plot shows the distribution of patients with and without CHD:
   - 0 = Not Affected
   - 1 = Affected

### 2. **Confusion Matrix**
   A confusion matrix visualization highlights the model’s true positive, true negative, false positive, and false negative predictions.

---

## Tools and Libraries Used

- **Python**: Programming language for the project.
- **Pandas**: For data loading, cleaning, and manipulation.
- **NumPy**: For numerical computations.
- **Seaborn and Matplotlib**: For data visualization.
- **Scikit-Learn**: For model building, training, and evaluation.

---

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Extract the zip file to obtain the `heartdata.csv` dataset.
3. Install the necessary libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```
4. Run the project file:
   ```bash
   python "Heart Disease Prediction Using Logistic Regression.py"
   ```

---
