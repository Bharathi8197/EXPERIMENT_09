Exp 9: Case Study on a Dataset with EDA and Visualization Techniques 

AIM:
To apply various exploratory data analysis (EDA) and visualization techniques on a case study dataset, derive insights, and present an analytical summary.

EQUIPMENTS REQUIRED:
Python
Libraries: pandas, matplotlib, seaborn, numpy

ALGORITHM:
Import the dataset using pandas from the URL.
Clean the data – handle missing values.
Perform univariate, bivariate, and multivariate analysis.
Use appropriate visualizations like bar charts, heatmaps, boxplots, etc.
Derive meaningful insights related to survival based on features like age, gender, and class.

PROGRAM:

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

# Step 1: Load Dataset
url = "https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv"
df = pd.read_csv(url)

# Step 2: Display Dataset Info
print(df.head())
print(df.info())

# Step 3: Handle Missing Values
df['Age'].fillna(df['Age'].median(), inplace=True)
df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)

# Step 4: Univariate Analysis
plt.figure(figsize=(8, 5))
sns.countplot(x='Survived', data=df, palette='Set2')
plt.title('Survival Distribution')
plt.xticks([0, 1], ['Not Survived', 'Survived'])
plt.show()

# Step 5: Bivariate Analysis - Gender vs Survival
plt.figure(figsize=(8, 5))
sns.countplot(x='Sex', hue='Survived', data=df, palette='pastel')
plt.title('Survival Count by Gender')
plt.show()

# Step 6: Bivariate Analysis - Pclass vs Survival
plt.figure(figsize=(8, 5))
sns.countplot(x='Pclass', hue='Survived', data=df, palette='Set3')
plt.title('Survival Count by Passenger Class')
plt.show()

# Step 7: Multivariate Analysis - Heatmap
plt.figure(figsize=(12, 6))
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
plt.title('Correlation Heatmap')
plt.show()

# Step 8: Age Distribution by Survival
plt.figure(figsize=(8, 5))
sns.histplot(data=df, x='Age', hue='Survived', multiple='stack', bins=30, palette='husl')
plt.title('Age Distribution by Survival')
plt.show()


EXPECTED OUTPUT:
A bar plot showing total survivors vs non-survivors.
Visual comparison of survival based on gender and class.
A heatmap showing correlations between numerical features.
Histogram of age distribution split by survival status.

RESULT:
Through this case study on the Titanic dataset:
Females had a significantly higher survival rate.
Passengers in 1st class had better chances of survival.
Age and Fare had a mild influence on survival.
We applied key EDA techniques to extract valuable insights from the dataset.

