# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE
### Developed by:Kavinesh M
### Register No:212222230064
```python
import pandas as pd
df=pd.read_csv("SAMPLEDS - Sheet1.csv");
df
df.shape
df.info()
df.head()
df.tail()
df.isnull().sum()
df.dropna(how='any').shape
x=df.dropna(how='any')
x

y=df.dropna(how='all')
y
tot=df.dropna(subset=['TOTAL'],how='any')
tot
t1=df.dropna(subset=['M1','M2','M3','M4'])
t1
df.fillna(0)
df.fillna(method='ffill')
df.fillna(method='bfill')
mn=df.TOTAL.mean()
mn
df.TOTAL.fillna(mn,inplace=True)
df
i=df.M1.interpolate()
i
df.M1.fillna(i,inplace=True)
df
md=df.M2.median()
md
m=df.M2.mode()
m
df.M2.fillna(md,inplace=True)
df
df.duplicated()
df.drop_duplicates(inplace=True)
df
df['cd']=pd.to_datetime(df['DOB'])
df

for x in df.index:
  if df.loc[x,"AVG"]>100:
    df.drop(x,inplace=True)
df


```
# OUTPUT
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/b04bc09b-aad9-4e08-bb4f-ffc33d0a57bd)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/e9191dd7-fd76-49cf-9572-6a95c1fdec31)
<br>


![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/fc5646bc-5f09-4449-a810-d1a96af0e759)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/ca663b59-7790-4de7-8813-0ba1e9a2f20d)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/459aae91-2394-4437-bd3e-fd769c0b19c1)
<br>
 



