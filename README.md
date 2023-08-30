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
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/7a74c202-8c08-4e34-bf58-0d74a6592a1f)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/04f9e304-b435-4e93-85ba-4c07407b3424)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/50d5dd78-1448-44f9-91dc-e73daaaf32ba)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/f84ee951-285d-4c8b-acc9-0f3a3f575fc5)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/d0a40e81-1a2a-4d3e-bf07-9c9e5ef53609)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/96705cb6-fbb7-49bc-9760-8d21a9f68afc)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/95c12089-8421-4ed5-8f0a-406df11fe301)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/51a38697-0154-47c6-8a19-deae3f27fc03)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/4227fcf7-13fc-449c-81dc-f7f636b9f24d)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/89333abe-f635-4dbb-8883-33facbfce7fa)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/4fe12bc3-8493-4219-b10d-5c2bdc9227fb)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/c8d2bf8b-6a27-4dfd-bb96-60c6dbfce3c6)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/decae851-1b73-4f34-8495-38b23aeb6a6e)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/c18987d5-1c58-4c04-a13d-dfc1aa474d1d)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/6d413529-a351-492b-9812-ea04110bb6f2)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/3ac63188-fe54-4bd0-944a-48f460cf5bdb)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/b08e8841-7e81-4fd6-b47e-ea1b5da72310)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/725b9178-0e45-4dde-9a15-86849618a668)
![image](https://github.com/kavinesh8476/ODD2023-Datascience-Ex01/assets/118466561/1512188d-b0e6-4eea-be7f-5827e8e270dc)
## RESULT:
Thus the given data is read,cleansed and the cleaned data is saved into the file.
 



