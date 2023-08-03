# SalesData Analysis with Python

<h2>Description</h2>
In this project, I have aimed to examine and perform analytics on the sales history of a Supermarket Store, which ultimately led us to extract insights on its sales performance as well as to identify the potential improvement metrics for business, marketing & subsequent teams to be implemented. I have inculcated <b>Python Libraries</b> to perform analytical operations on our data. <br></br>The goal of the project was to gain a hands-on understanding of <b>Data Analysis Techniques</b> and showcase my skills in Data Manipulation, Visualization, and Interpretation.
</br>

## Steps
 1. Data Cleaning & Manipulation 
 2. Explanatory Data Analysis (EDA) 

## Technologies Used

- <b>Python 3.9.13</b>
- <b>Jupyter Notebook</b>
- <b>Pandas</b>
- <b>NumPy</b>
- <b>Matplotlib</b>
- <b>Seaborn</b>

## Dataset 
The dataset is available [HERE](https://github.com/KAnurag27/SalesData_Analysis_with_Python/blob/main/Sales%20Data.csv). It contains information about product purchases by 11251 Customers, their data has been gathered and categorized in terms of Gender, Age, Marital Status, Origin State, Occupation, etc.
<br />
<br />
Below attached is a quick snapshot, providing dataType description from our data. <br></br>
<img src="https://i.imgur.com/o6SN9VB.png"/>

## Python Code 
The code file can be accessed [HERE](https://github.com/KAnurag27/SalesData_Analysis_with_Python/blob/main/SalesData_Analysis.ipynb). Below is the glimpse of code written in <b>Jupyter Notebook</b>: 
<br></br><b>Libraries & Loading Data</b>
```python
# import python libraries
import numpy as np 
import pandas as pd 
import matplotlib.pyplot as plt # visualizing data
%matplotlib inline
import seaborn as sns
```
```python
# import csv file
df = pd.read_csv('Diwali Sales Data.csv', encoding= 'unicode_escape')
```
</br><b>Data Cleaning & Manipulation</b>
```python
#drop unrelated/blank columns
df.drop(['Status', 'unnamed1'], axis=1, inplace=True)
```
```python
#check for null values
pd.isnull(df).sum()
```
```python
# drop null values
df.dropna(inplace=True)
```
```python
# drop null values
df.dropna(inplace=True)
```
```python
# change data type
df['Amount'] = df['Amount'].astype('int')
```





## Skills 
 <b>Data Cleaning | Data Analysis | Hypothesis Testing | Data Visualization</b> 

