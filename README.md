# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
import pandas as pd

import numpy as np

import seaborn as sns

df=pd.read_csv("/content/titanic_dataset.csv")

df

df.info()

df.describe()

df.dtypes

df.shape

df['Age'].value_counts()

df.set_index("PassengerId", inplace=True)

df

df.nunique()

sns.countplot(data=df,x="Age")

df.rename(columns={'Sex':'Gender'},inplace=True)

df

sns.catplot(x="Gender",col="Survived",kind="count",data=df)

df.boxplot(column="Age",by="Survived")

sns.scatterplot(x=df["Age"],y=df["Fare"])

plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)

sns.catplot(x='Pclass',y='Age',hue='Gender',col='Survived',kind='box',data=df)

corr=df.corr(numeric_only=True)

sns.heatmap(corr,annot=True)

<img width="1273" height="467" alt="1" src="https://github.com/user-attachments/assets/6b258665-4743-499b-b00a-f6819e9348a4" />
<img width="390" height="344" alt="2" src="https://github.com/user-attachments/assets/27e0f98b-ca0f-4468-b040-043360222ee0" />
<img width="794" height="302" alt="3" src="https://github.com/user-attachments/assets/d8645fbd-7b52-4f2c-9667-80775ba52814" />
<img width="404" height="454" alt="4" src="https://github.com/user-attachments/assets/1c548fee-f6c5-4ed1-a635-2377ee9571c1" />
<img width="1247" height="484" alt="5" src="https://github.com/user-attachments/assets/5a1fa0e7-7272-4ddc-ab13-aa358ae31d60" />
<img width="1247" height="484" alt="6" src="https://github.com/user-attachments/assets/e8d4688e-be08-4816-ae48-b208d84b93f5" />
<img width="1201" height="457" alt="8" src="https://github.com/user-attachments/assets/22a98f66-91ee-4d45-8edc-646045a9dbb6" />
<img width="456" height="428" alt="9" src="https://github.com/user-attachments/assets/01a6dc39-cb1e-4886-afd6-307be23f0b27" />
<img width="657" height="466" alt="10" src="https://github.com/user-attachments/assets/bc786519-0940-4e2a-ae4d-703307b162ba" />
<img width="1198" height="450" alt="11" src="https://github.com/user-attachments/assets/48c7ce7f-0b56-4cf8-af0b-a8fcd46e7317" />
<img width="1082" height="524" alt="12" src="https://github.com/user-attachments/assets/8aea3a5b-de75-4238-bf1d-e1e644df9eef" />
<img width="633" height="492" alt="13" src="https://github.com/user-attachments/assets/0f3b8490-662f-4e46-b72f-6baf1aca19e6" />
<img width="644" height="465" alt="14" src="https://github.com/user-attachments/assets/765b2990-6a8c-4b4c-95f7-c2ea82f40f69" />
<img width="646" height="444" alt="15" src="https://github.com/user-attachments/assets/d2ebd1cb-674d-4f08-b735-7cd4d83b3406" />
<img width="1153" height="522" alt="16" src="https://github.com/user-attachments/assets/3bfcd12a-870b-474f-8d8e-09924be94d19" />
<img width="604" height="448" alt="17" src="https://github.com/user-attachments/assets/c4cfb011-f040-4202-b576-0e92e22b4338" />

# RESULT
        Thus the program to implement the data analysis has been successfully completed. 

