**Exp 9: Case Study on a Dataset with EDA and Visualization Techniques**

**AIM:**
To apply various exploratory data analysis (EDA) and visualization techniques on a case study dataset, derive insights, and present an analytical summary.

**EQUIPMENTS REQUIRED:**
Python
Libraries: pandas, matplotlib, seaborn, numpy

**ALGORITHM:**
1)Import the dataset using pandas from the URL.
2)Clean the data – handle missing values.
3)Perform univariate, bivariate, and multivariate analysis.
4)Use appropriate visualizations like bar charts, heatmaps, boxplots, etc.
5)Derive meaningful insights related to survival based on features like age, gender, and class.

**PROGRAM:**

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

# Step 1: Load Dataset
url = "https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv"
df = pd.read_csv(url)







**EXPECTED OUTPUT:**
**Note** : The output shold be as follows
    A bar plot showing total survivors vs non-survivors.
    Visual comparison of survival based on gender and class.
    A heatmap showing correlations between numerical features.
    Histogram of age distribution split by survival status.

**RESULT**:
  Through this case study on the Titanic dataset:
  Females had a significantly higher survival rate.
  Passengers in 1st class had better chances of survival.
  Age and Fare had a mild influence on survival.
  We applied key EDA techniques to extract valuable insights from the dataset.

