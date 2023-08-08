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

## Skills 
 <b>Data Cleaning | Data Analysis | Hypothesis Testing | Data Visualization</b> 

## Dataset 
The dataset is available [HERE](https://github.com/KAnurag27/SalesData_Analysis_with_Python/blob/main/Sales%20Data.csv). It contains information about product purchases by <b>11251</b> Customers in the last quarter of the year 2022, their data has been gathered and categorized in terms of Gender, Age, Marital Status, Origin State, Occupation, etc.
<br />
<br />
Below attached is a quick snapshot, providing dataType description from our data. <br></br>
<img src="https://i.imgur.com/o6SN9VB.png"/>

## Python Code 
The code file can be accessed [HERE](https://github.com/KAnurag27/SalesData_Analysis_with_Python/blob/main/SalesData_Analysis.ipynb). Below is the glimpse of code written in <b>Jupyter Notebook</b>: 
<br></br><b>Library Installations & Data Loading </b>
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
</br>
```

## Exploratory Data Analysis
Multiple attributes were used to identify patterns, trends & correlations among the data, such as:
  - Gender & Age 
  - State (Geography) </br>
  - Marital Status, Gender & Purchasing Power </br>
  - Occupation & Purchasing Power </br>
  - Product Category</br>

 Key visualizations are attached below along with the written code:
 ### Gender & Age 
 ```python
ax = sns.countplot(data = df, x = 'Age Group', hue = 'Gender')
for bars in ax.containers:
    ax.bar_label(bars)
```
<img src="https://i.imgur.com/AC0QsMx.png"/>

### State (Geography)

```python
#total number of orders from top 10 states
sales_state = df.groupby(['State'], as_index=False)['Orders'].sum().sort_values(by='Orders', ascending=False).head(10)
sns.set(rc={'figure.figsize':(15,5)})
sns.barplot(data = sales_state, x = 'State',y= 'Orders')
```
<img src="https://i.imgur.com/FsiiHVb.png"/>

### Marital Status, Gender & Purchasing Power 

```python
sales_state = df.groupby(['Marital_Status', 'Gender'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False)
sns.set(rc={'figure.figsize':(6,5)})
sns.barplot(data = sales_state, x = 'Marital_Status',y= 'Amount', hue='Gender')
```
<img src="https://i.imgur.com/ThW6ax1.png"/>

### Occupation & Purchasing Power 

```python
sales_state = df.groupby(['Occupation'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False)
sns.set(rc={'figure.figsize':(20,5)})
sns.barplot(data = sales_state, x = 'Occupation',y= 'Amount')
```
<img src="https://i.imgur.com/IOSH8Iw.png"/>

### Product Category

```python
sales_state = df.groupby(['Product_Category'], as_index=False)['Amount'].sum().sort_values(by='Amount', ascending=False).head(10)
sns.set(rc={'figure.figsize':(20,5)})
sns.barplot(data = sales_state, x = 'Product_Category',y= 'Amount')
```
<img src="https://i.imgur.com/2y2HrRO.png"/>

### Data Insights
During the last quarter of 2022, Married women from age group <b>26-35 yrs</b> and who are from <b>Uttar Pradesh, Maharastra</b> and <b>Karnataka</b> working in <b>IT, Healthcare</b> and <b>Aviation</b> are more likely to buy products from <b>Food, Clothing</b> and <b>Electronics category</b>.

## Concluding Remarks
- Identifying these key metrics can be utilized as a business opportunity to focus on the outperforming segments.
- Embarking on the benchmark for inventory management and prioritizing efforts will help in better decision-making.   
