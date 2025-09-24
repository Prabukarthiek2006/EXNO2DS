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
```
python
import pandas as pd
import numpy as np
import matplotlib.pyplot as pltimport seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df
```
## Output
<img width="1147" height="410" alt="image" src="https://github.com/user-attachments/assets/fb6208ca-d7bf-40fa-ad24-21bbe73833f3" />
```
python
 df.describe()
```
## Output
<img width="695" height="295" alt="image" src="https://github.com/user-attachments/assets/a02dd7bd-d159-44df-a38c-e5ae9ee68f57" />
```
python
df.dtypes
```
## Output
<img width="183" height="443" alt="image" src="https://github.com/user-attachments/assets/b08975ec-0b7c-42f7-87c7-08912db2aad5" />
```
python
df.shape
```
## Output
<img width="94" height="34" alt="image" src="https://github.com/user-attachments/assets/510ac8c4-7006-4437-b409-1f336efb52a4" />
```
python
df.value_counts()
```
## Output
<img width="1198" height="441" alt="image" src="https://github.com/user-attachments/assets/5d500538-a9ac-44e9-9d2d-3f6822614676" />
```
python
df['Age'].value_counts()
```
## Output
<img width="129" height="438" alt="image" src="https://github.com/user-attachments/assets/9981b13e-9537-4288-a0da-ed90c1ffd9ee" />
```
python
df.set_index("PassengerId", inplace=True)
df
```
## Output
<img width="1122" height="402" alt="image" src="https://github.com/user-attachments/assets/c798d4f5-b460-4a98-bc98-2c9b54f07dfc" />
```
python
df.nunique()
```
## Output
<img width="145" height="417" alt="image" src="https://github.com/user-attachments/assets/38567fbc-8870-4a29-8fce-9e28b9a863fa" />
```
python
sns.countplot(data=df,x='Survived')
```
## Output
<img width="585" height="460" alt="image" src="https://github.com/user-attachments/assets/81a211f4-2802-490d-8e8f-055655cac32b" />
```
python
df.rename(columns={'Sex':'Gender'},inplace=True)
df
```
## Output
<img width="1119" height="434" alt="image" src="https://github.com/user-attachments/assets/1600fdb9-3f7c-416b-b62d-52cd8f780ce5" />
```
python
sns.catplot(x="Gender",col="Survived",kind="count",data=df)
```
## Output
<img width="1016" height="512" alt="image" src="https://github.com/user-attachments/assets/f133f432-864c-4853-8731-3f7be1e9e56a" />
```
python
df.boxplot(column="Age",by="Survived")
```
## Output
<img width="569" height="487" alt="image" src="https://github.com/user-attachments/assets/4660e87c-4e2a-4f87-a684-2be4704e1eb6" />
```
python
sns.scatterplot(x=df["Age"],y=df["Fare"])
```
## Output
<img width="586" height="453" alt="image" src="https://github.com/user-attachments/assets/5591900f-1a03-4dd6-ac94-f9b7fc0228b2" />
```
python
fig, axl=plt.subplots(figsize=(8,5))
 plt=sns.boxplot(ax=axl,x='Pclass',y='Age',hue='Gender',data=df)
```
## Output
<img width="693" height="454" alt="image" src="https://github.com/user-attachments/assets/e990ada3-ed94-493b-a19c-6276864ddce0" />
```
python
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
```
## Output
<img width="566" height="436" alt="image" src="https://github.com/user-attachments/assets/758d9740-3757-4525-9d49-85dbc3d143e0" />


# RESULT
Hence, the given commands and the output have been verified successfully.
