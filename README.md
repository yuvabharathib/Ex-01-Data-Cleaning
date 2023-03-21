# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
```
import pandas as pd
df=pd.read_csv("/content/Loan_data (1).csv")
print(df)
df.head(10)
df.info()
df.isnull()
df.isnull().sum()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
df.info()
df.isnull().sum()
```
# OUPUT
### DATA:
![WhatsApp Image 2023-03-21 at 10 59 41 AM](https://user-images.githubusercontent.com/113497404/226526402-b632196b-18be-4be0-8717-908e0d9fa832.jpeg)
### NON NULL BEFORE:
### df.info:
![df info after (1)](https://user-images.githubusercontent.com/113497404/226526921-9ec63345-4522-4ae4-8e4b-17275701aecb.jpg)
### MODE:
![modeee (1)](https://user-images.githubusercontent.com/113497404/226527149-56e0ecd5-698e-4594-88d0-6368336d9000.jpg)
### MEAN:
![MEAN (1)](https://user-images.githubusercontent.com/113497404/226527300-54472e60-23c2-463e-a1dc-f075dce5d5e0.jpg)
### MEDIAN:
![median](https://user-images.githubusercontent.com/113497404/226527388-e1789008-a8dd-4868-80b3-a4e491453b7d.jpg)
### NON NULL AFTER:
### df.info:
![df info after (3)](https://user-images.githubusercontent.com/113497404/226527580-d85098ce-a2e8-4aeb-96da-2af103e70048.jpg)
### df.isnull().sum():
![dh isnull()  (1)](https://user-images.githubusercontent.com/113497404/226527771-11f3244c-5de0-40d5-b64c-428ec88bf8ae.jpg)
### RESULT:
Thus the given data is read,cleansed and the cleaned data is saved into the file.









