# EXNO2DS
# Name:Dinesh m
# Register no:212222043002
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
## CODING
      import pandas as pd
      df = pd.read_csv("titanic_dataset (1).csv")
      df.head()
## OUTPUT
<img width="1215" height="779" alt="Screenshot 2026-03-09 142423" src="https://github.com/user-attachments/assets/7e08f574-3c32-4190-8c30-84e70b250b69" />

## CODING 
      df.info()
## OUTPUT
<img width="1112" height="495" alt="Screenshot 2026-03-09 142540" src="https://github.com/user-attachments/assets/538ee2b5-8fb1-4b09-a3a9-276ab52f3a47" />

## CODING
      df.dtypes

## OUTPUT
<img width="982" height="625" alt="Screenshot 2026-03-09 142601" src="https://github.com/user-attachments/assets/08f1ed37-1e93-4f54-8607-21a585c28035" />

## CODING
      df.value_counts()

## OUTPUT
<img width="1213" height="909" alt="Screenshot 2026-03-09 142655" src="https://github.com/user-attachments/assets/3803319a-c214-47b8-8ddb-71c10d00d5ef" />

## CODING
      df['Age'].value_counts()

## OUTPUT
<img width="774" height="663" alt="Screenshot 2026-03-09 142717" src="https://github.com/user-attachments/assets/0c9f1244-8100-4e71-9fbf-b33fe5428787" />


## CODING
      df.shape

# OUTPUT
<img width="344" height="99" alt="Screenshot 2026-03-09 142734" src="https://github.com/user-attachments/assets/f06eecd7-93c8-40ac-b1e1-17168979c6bb" />

## CODING
      df.set_index("PassengerId",inplace=True)
      df.describe()

## OUTPUT
<img width="943" height="452" alt="Screenshot 2026-03-09 142753" src="https://github.com/user-attachments/assets/a5643349-3603-4841-83d7-22e0a409358e" />

## CODING
      df.nunique()

## OUTPUT
<img width="557" height="587" alt="Screenshot 2026-03-09 142812" src="https://github.com/user-attachments/assets/51b1c6a1-9726-49cd-89f1-556d461352f8" />

## CODING
      sns.countplot(data=df,x="Survived")

## OUTPUT
<img width="1080" height="632" alt="Screenshot 2026-03-09 142832" src="https://github.com/user-attachments/assets/c6ab1265-7bc9-4e44-950d-db2649302725" />

## CODING
      df.Pclass.unique()

## OUTPUT
<img width="450" height="130" alt="Screenshot 2026-03-09 142849" src="https://github.com/user-attachments/assets/03756578-b011-4ec1-a5c5-532b72cd3f4b" />

## CODING
      df.rename(columns={'Sex':'Gender'},inplace=True)
      df

## OUTPUT
<img width="1230" height="889" alt="Screenshot 2026-03-09 142916" src="https://github.com/user-attachments/assets/eebab618-9cca-4442-96a8-f592575809d1" />

## CODING
      sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)

## OUTPUT
<img width="1069" height="701" alt="Screenshot 2026-03-09 142941" src="https://github.com/user-attachments/assets/d60f044a-3997-4c97-88ee-f67d44cc3104" />


## CODING
      df.boxplot(column="Age",by="Survived")

## OUTPUT
<img width="965" height="660" alt="Screenshot 2026-03-09 143006" src="https://github.com/user-attachments/assets/3d47fab7-ade8-4b71-974e-7efa35c3347e" />

## CODING
      sns.scatterplot(x=df["Age"],y=df["Fare"])

## OUTPUT
<img width="964" height="627" alt="Screenshot 2026-03-09 143035" src="https://github.com/user-attachments/assets/f865738a-841e-48df-b383-549da1089ab9" />

## CODING
      fig, ax1 =plt.subplots(figsize=(8,5))
      plt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=df)

## OUTPUT
<img width="1021" height="662" alt="Screenshot 2026-03-09 143056" src="https://github.com/user-attachments/assets/2578ceed-4bfe-462e-a674-42021a47faf7" />

## CODING
      sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")

## OUTPUT
<img width="1211" height="631" alt="Screenshot 2026-03-09 143136" src="https://github.com/user-attachments/assets/6fc631a1-fe2b-4fdb-8af2-a859d6e63495" />

## CODING
      corr = df.select_dtypes(include=np.number).corr()
      sns.heatmap(corr,annot=True)

## OUTPUT
<img width="898" height="637" alt="Screenshot 2026-03-09 143155" src="https://github.com/user-attachments/assets/cfbebcf7-9b2e-4dab-8052-fa69659baffa" />

# RESULT
Experiment is successfull
