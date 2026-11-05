
# Exploratory Data Analysis (EDA) - Titanic Dataset

## 1. Project Overview

This project performs Exploratory Data Analysis (EDA) on the Titanic
passenger dataset. The objective is to understand passenger information,
identify missing values, clean the data, detect outliers, and investigate
factors associated with passenger survival.

## 2. Dataset Information

- Dataset: Titanic Dataset
- Source: Kaggle Titanic Competition
- File analyzed: train.csv
- Total records: 891
- Original columns: 12
- Target variable: Survived

### Dataset Features

- PassengerId: Unique passenger identifier
- Survived: Survival status (0 = No, 1 = Yes)
- Pclass: Passenger class
- Name: Passenger name
- Sex: Passenger gender
- Age: Passenger age
- SibSp: Number of siblings/spouses aboard
- Parch: Number of parents/children aboard
- Ticket: Ticket number
- Fare: Ticket fare
- Cabin: Cabin information
- Embarked: Port of embarkation

## 3. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

## 4. Data Cleaning and Preprocessing

The following operations were performed:

1. Checked dataset structure, data types, and missing values.
2. Filled missing Age values using the median (28).
3. Filled missing Embarked values using the mode (S).
4. Created a HasCabin feature to indicate whether cabin information
   was available.
5. Removed the original Cabin column because approximately 77.1%
   of its values were missing.
6. Checked for duplicate records. No duplicate rows were found.
7. Detected potential outliers using the Interquartile Range (IQR)
   method.
8. Retained potential outliers because extreme values may represent
   genuine passenger characteristics rather than data errors.

## 5. Exploratory Data Analysis

The following analyses and visualizations were performed:

1. Numerical feature distributions
2. Categorical feature distributions
3. Boxplots for outlier detection
4. Correlation heatmap
5. Pairwise scatter plots
6. Survival count by gender
7. Survival count by embarkation port

All seven high-resolution visualization images are saved in the
visualizations folder.

## 6. Key Findings

### Gender and Survival

- Female survival rate: 74.20%
- Male survival rate: 18.89%

Female passengers had a substantially higher survival rate than
male passengers in this dataset.

### Passenger Class and Survival

- First class survival rate: 62.96%
- Second class survival rate: 47.28%
- Third class survival rate: 24.24%

Survival rates decreased from first class to third class.

### Embarkation Port and Survival

- Cherbourg (C): 55.36%
- Queenstown (Q): 38.96%
- Southampton (S): 33.90%

Cherbourg had the highest survival percentage, while Southampton
had the lowest.

### Correlation Analysis

Important observed correlations include:

- Survived and Pclass: approximately -0.34
- Survived and Fare: approximately +0.26
- Survived and HasCabin: approximately +0.32
- Pclass and Fare: approximately -0.55

These correlations indicate statistical associations, not proof
of causation. PassengerId is an identifier and is not a meaningful
predictive feature by itself.

### Outlier Analysis

The IQR method identified potential outliers in Age, Fare, SibSp,
and Parch. These observations were retained because they may be
valid passenger records.

## 7. Conclusion

The analysis indicates that survival outcomes in the Titanic dataset
were associated with passenger gender, passenger class, fare, and
embarkation port.

Female passengers and first-class passengers had higher survival
rates than male and third-class passengers.

The project demonstrates an EDA workflow covering data ingestion,
profiling, cleaning, missing-value treatment, outlier detection,
statistical analysis, and visualization.

## 8. Project Structure

- Titanic_EDA.ipynb: Jupyter Notebook containing the EDA analysis.
- README.md: Project documentation and summary of findings.
- titanic.zip: Original downloaded dataset archive.
- titanic_data/: Extracted dataset files.
  - train.csv
  - test.csv
  - gender_submission.csv
- visualizations/: Folder containing seven high-resolution PNG charts.

## 9. Dataset Source

Kaggle Titanic Competition:

https://www.kaggle.com/competitions/titanic/data
