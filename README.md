<H3>ENTER YOUR NAME: BHAVATHARANI S</H3>
<H3>ENTER YOUR REGISTER NO: 212223230032</H3>
<H3>EX. NO.1</H3>
<H3>DATE: 25.08.2025</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
## Import Libraries
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```

## Read the dataset
```
df=pd.read_csv("Churn_Modelling.csv")
print(df)
```
## Checking data
```
df.head()
df.tail()
df.columns
```

## Handling missing data
```
df.isnull().sum()
```

## Duplicate values
```
df.duplicated()
```

## checking for Outliers:
```
df.describe
```

## Dropping string values data from dataset
```
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
data.head()
```

## Normalize the dataset
```
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```
## Splitting the dataset
```
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```

## Training and testing model

```
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```

## OUTPUT:
## Original Dataset:

<img width="1181" height="711" alt="image" src="https://github.com/user-attachments/assets/42919919-b3bf-4e58-9ed3-2ff59cede3e2" />

## Missing data:

<img width="438" height="305" alt="image" src="https://github.com/user-attachments/assets/1b97a5ab-1011-43d8-be8c-a941c40e175e" />


## Duplicated data:

<img width="408" height="269" alt="image" src="https://github.com/user-attachments/assets/270f55f4-1d64-416f-a77a-65232b4d0bdc" />


## Outliers:

<img width="682" height="277" alt="image" src="https://github.com/user-attachments/assets/722a77fd-78f2-4f14-8723-fa5b841bc27c" />


## Normalizing data:

<img width="755" height="551" alt="image" src="https://github.com/user-attachments/assets/8605023f-81bb-49b0-b8c7-014ba67956fa" />

## spliting dataset:

<img width="648" height="301" alt="image" src="https://github.com/user-attachments/assets/778e0c99-e701-4115-8f1c-b9b10b53d31e" />

## Training and testing dataset:

<img width="682" height="687" alt="image" src="https://github.com/user-attachments/assets/69d4bf61-eaa8-4792-8dea-351dfb71c55e" />

## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


