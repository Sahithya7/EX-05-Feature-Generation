# EX-05-Feature-Generation
## AIM
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
# CODE
# data.csv
import pandas as pd   
import seaborn as sbn 
df=pd.read_csv("/content/data.csv") 
df.info() 
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() 
df['Ord_2'] = le.fit_transform(df['Ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Ord_2'])
from sklearn.preprocessing import OneHotEncoder 
enc = OneHotEncoder() 
enc = enc.fit_transform(df[['City']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
df = pd.concat([df, encoded_colm], axis=1) 
df = df.drop(['City'], axis=1) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2']) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1']) 
df.head(10)
# encoding.csv
import pandas as pd 
import seaborn as sbn 
data=pd.read_csv("/content/Encoding Data.csv") 
data.info() 
data.isnull().sum() from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() data['ord_2'] = le.fit_transform(data['ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(data['ord_2']) from sklearn.preprocessing import OneHotEncoder 
en = OneHotEncoder() 
en = en.fit_transform(data[['nom_0']]).toarray() 
encoded_colm = pd.DataFrame(en) 
data= pd.concat([data, encoded_colm], axis=1) 
data= data.drop(['nom_0'], axis=1) 
data.head(10) 
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2']) 
data.head(10)
# titanic.csv
import pandas as pd 
import seaborn as sbn 
dt=pd.read_csv("/content/titanic_dataset.csv") 
dt.info() 
dt.isnull().sum() 
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean()) 
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0]) 
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0]) 
dt.isnull().sum( ) from sklearn.preprocessing import LabelEncoder 
lc = LabelEncoder() 
df['Sex'] = lc.fit_transform(df['Sex']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Sex']) from sklearn.preprocessing import OneHotEncoder 
enc= OneHotEncoder() 
enc= enc.fit_transform(dt[['Name']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
dt= pd.concat([dt, encoded_colm], axis=1) 
dt= dt.drop(['Name'], axis=1) 
dt.head(10) 
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket']) 
df.head(10) 
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked']) 
df.head(10)
# OUPUT
# Data.csv
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/b83c4668-a9e0-4324-bc25-9c6fcab17d09)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/77691bfb-7c8e-43ed-af8b-f62806c88d80)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/ef9ee5df-2b41-4214-ae49-db30551cd6ea)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/f1488992-6e92-4897-b5b5-c774e3f2dcbf)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/892f6dd2-ca99-4572-b773-1f9a11aab2e6)
# Encoding.csv
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/bd6376e0-8889-4e61-bfe4-3d3694b036da)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/e955c14b-033e-4b7e-895e-03bbbeda1c8d)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/52700f89-a94d-4354-a5c2-466a8f6e95e5)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/4b2f8a56-8d24-40d2-b1fa-f73a6d7d53d3)
# Titanic.csv
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/04afaa87-d71e-4958-87b9-2b5f8cb73152)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/e20353c6-4fe7-4532-a5dc-1516ac1e5579)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/55f4ebd3-d44c-4012-9f72-8a788f2a1e78)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/32640ea0-ef42-4280-9bae-154c9deb3d5e)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/5b095c09-e1c0-40f4-8538-ce673fcf1855)
![image](https://github.com/Sahithya7/EX-05-Feature-Generation/assets/133002193/1fa3e417-a065-4c3f-a28b-7c2273d1591c)
# RESULT:
Thus the program for Feature Generation is executed successfully.
