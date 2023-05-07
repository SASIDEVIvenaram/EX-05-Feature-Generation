# EX-05-Feature-Generation


# AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# PROGRAM:
```
Devloped by: SASIDEVI V
Register No.: 212222230136
```
Encoding Data.csv
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
data.csv
```
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
titanic_dataset.csv
```
df2 = pd.read_csv("titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```


# OUPUT:
## Encoding Data.csv
### df.head()
![ds51](https://user-images.githubusercontent.com/118707332/236667110-6b002d29-8854-4a54-93e2-9badad530521.png)


### Ordinal encoder
![ds52](https://user-images.githubusercontent.com/118707332/236667113-d2012339-7d86-418f-8aa9-da4d3d4cbd20.png)


### Label encoder
![ds53](https://user-images.githubusercontent.com/118707332/236667116-bffa6e2e-bdd0-410a-827d-935a5bf370ec.png)


### Binary encoder

![ds54](https://user-images.githubusercontent.com/118707332/236667120-e925542e-1822-4cad-a666-28f3830866b6.png)

![ds55](https://user-images.githubusercontent.com/118707332/236667125-5573c8db-b013-408c-a451-e413618229a2.png)
## data.csv
### df.head()
![ds56](https://user-images.githubusercontent.com/118707332/236667329-32e1d773-57df-4ddb-bbef-6489d64fcb57.png)


### Ordinal encoder
![ds57](https://user-images.githubusercontent.com/118707332/236667332-88389971-df63-42bc-8539-0745e28776a0.png)
![ds58](https://user-images.githubusercontent.com/118707332/236667334-2ec8afcb-9e0e-4cd8-8ed4-7ff67940b249.png)


### Label encoder

![ds59](https://user-images.githubusercontent.com/118707332/236667338-be13d50e-d45b-4c19-b159-0f16b0bdd1c2.png)


### Binary encoder
![ds510](https://user-images.githubusercontent.com/118707332/236667348-b50185b0-cdd8-4540-9329-3e03e4fddab3.png)
![ds511](https://user-images.githubusercontent.com/118707332/236667350-ab48dbb5-8c51-40f6-8736-d160942f18c2.png)
## titanic_dataset.csv
### df.head()
![ds512](https://user-images.githubusercontent.com/118707332/236667442-ed1d05b5-b438-49e3-81d0-f5599e6e3ea2.png)


### Binary encoder

![ds513](https://user-images.githubusercontent.com/118707332/236667445-6d290c86-e540-4d01-9381-d2cf213f0690.png)
# RESULT:
The Feature Generation process was performed and saved the data to a file.
