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

# CODING AND OUTPUT
```
import pandas as pd
df=pd.read_csv("titanic_dataset.csv")
print(df)
```
<img width="648" height="687" alt="image" src="https://github.com/user-attachments/assets/3323d295-cf33-4c44-97a0-a4d793a11c99" />

```
df.info()
```

<img width="417" height="335" alt="image" src="https://github.com/user-attachments/assets/1ff331c3-c9ea-44ce-8fab-0d729cf10e71" />

```
df.describe()
```

<img width="933" height="383" alt="image" src="https://github.com/user-attachments/assets/28bb0d2b-bef3-4fd6-bfff-391727730172" />

```
df.shape
```

<img width="190" height="35" alt="image" src="https://github.com/user-attachments/assets/2276b5b4-9eb7-48f2-9aa6-aee8fae4e39e" />

```
df.dtypes
```

<img width="320" height="233" alt="image" src="https://github.com/user-attachments/assets/7ceed50a-3aaa-46ef-bd90-513996ffac84" />


```
df["Survived"].value_counts()
```

<img width="503" height="102" alt="image" src="https://github.com/user-attachments/assets/2b1bf54f-2261-4ac3-86ad-c1237da8d30f" />
```
df.nunique()
```
<img width="455" height="365" alt="image" src="https://github.com/user-attachments/assets/2748ca28-c3bf-4623-b908-530a2353824f" />
```
import seaborn as sns
sns.countplot(data=df,x="Survived")
```
<img width="685" height="472" alt="image" src="https://github.com/user-attachments/assets/5dc117aa-40a3-496f-994c-46a3ba88c9c5" />
```
sns.boxplot(data=df,x="Age")
```
<img width="688" height="471" alt="image" src="https://github.com/user-attachments/assets/bdd6cf9a-bd55-42af-afe2-ce161dce5002" />

```
sns.histplot(data=df,x="Age")
```


```
df.rename(columns={'Sex':'Gender'},inplace=True)
print(df)
```


```
sns.catplot(x='Survived',hue="Gender",data=df,kind='count')
```


```
df.boxplot(column="Age",by="Survived")
```

<img width="681" height="493" alt="image" src="https://github.com/user-attachments/assets/ba2bff4a-8f3c-48cb-af6a-7bdc01216811" />



# Categorical data analysis



# Bivariate Analysis



# Multivariate Analysis

# Co-relation

# RESULT
        <<INCLUDE YOUR RESULT HERE>>
