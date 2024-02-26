<H3>NAME : HARINI V</H3>
<H3>REGISTER NO. 212222230044</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
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
#### importing libraries
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
```

#### Reading the dataset
```
df=pd.read_csv("/content/Churn_Modelling.csv", index_col="RowNumber")
df
```

#### Dropping the unwanted Columns
```
df.drop(['CustomerId'],axis=1,inplace=True)
df.drop(['Surname'],axis=1,inplace=True)
df.drop('Age',axis=1,inplace=True)
df.drop('Geography',axis=1,inplace=True)
df.drop('Gender',axis=1,inplace=True)
df
```
#### Checking for null values
```
df.isnull().sum()
```
#### Checking for duplicate values
```
df.duplicated()
```
#### Describing the dataset
```
df.describe()
```
#### Scaling the dataset
```
scaler=StandardScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
df1
```
#### Allocating X and Y attributes
```
x=df1.iloc[:,:-1].values
x
y=df1.iloc[:,-1].values
y
```
#### Splitting the data into training and testing dataset
```
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(x_train)
print(len(x_train))
print(x_test)
print(len(x_test))
```

## OUTPUT:
#### DATASET:

![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/1a830cc7-f5aa-4867-99b7-0903d8434760)



#### DROPPING THE UNWANTED DATASET:

![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/fe756e77-c0c1-47c6-a247-d0c2fa3a4ab8)



#### CHECKING NULL VALUES:

![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/1e08b3b1-e273-4c70-b16e-ccd43590788c)
#### CHECKING FOR DUPLICATION:

![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/328bfd2f-e57c-4af5-b97d-d0586f2fb26f)


#### DESCRIBING THE DATASET:

![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/129508fe-dd43-46ce-b1f2-2ddaf24ea920)


#### SCALING THE DATASET:
![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/808e4cd1-10b8-48e6-92aa-fc5327a901cd)


#### X FEATURES:

![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/0b41cf3a-d01a-49ee-8fb8-51ef0260f69c)


#### Y FEATURES:



![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/1adc2797-aae5-4867-8b3e-397472324263)


#### SPLITTING THE TRAINING AND TESTING DATASET:
![image](https://github.com/harini1006/Ex-1-NN/assets/113497405/0c6f0396-5397-42ff-a3de-338c6ba062b5)


## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


