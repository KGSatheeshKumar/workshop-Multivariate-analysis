# workshop-Multivariate-analysis
## Aim
To perform Multivariate EDA on the given data set.

## Explanation
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## Algorithm
## Step1
Import the built libraries required to perform EDA and outlier removal.

## Step2
Read the given csv file.

## Step3
Convert the file into a dataframe and get information of the data.

## Step4
Return the objects containing counts of unique values using (value_counts()).

## Step5
Plot the counts in the form of Histogram or Bar Graph.

## Step6
Use seaborn the bar graph comparison of data can be viewed.

## Step7
Find the pairwise correlation of all columns in the dataframe.corr()

## Step8
Save the final data set into the file.

## Types of bivariate analyis
1)Numerical & Numerical(Scatter plot)
2)Numerical & Categorical(Bar plot,Box plot,Dist plot)
## PROGRAM
```
Developed by : DHARSHAN V
Registration Number : 212222230031
```
```
import pandas as pd
df=pd.read_excel("/content/FlightInformation.xlsx")
df
df.info()
import seaborn as sns
sns.scatterplot(x=df['Dep_Time'],y=df['Arrival_Time'])
import matplotlib.pyplot as plt
states=df.loc[:,["Dep_Time","Price"]]
states=states.groupby(by=["Dep_Time"]).sum().sort_values(by="Price")
plt.figure(figsize=(17,7))
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("Dep_Time")
plt.ylabel=("Price")
plt.show()
import numpy as np
data=np.random.randint(low=5,high=110,size=(10,10))
print("The data to be plotted:\n")
print(data)
h=sns.heatmap(data=data)
plt.show
```
## OUTPUT
![Screenshot 2023-04-04 161624](https://user-images.githubusercontent.com/113497491/229770247-037d8d1a-b8be-4a3a-a708-ac8b7170c6db.png)

![Screenshot 2023-04-04 161632](https://user-images.githubusercontent.com/113497491/229770753-6714b556-c80a-4470-bd7b-328f48d701b7.png)

![Screenshot 2023-04-04 161642](https://user-images.githubusercontent.com/113497491/229770328-d1a643ab-4cfc-47e8-9d94-a8634c35f871.png)

![Screenshot 2023-04-04 161700](https://user-images.githubusercontent.com/113497491/229770378-613d46ce-da64-44cf-b814-14848b948a17.png)

![Screenshot 2023-04-04 161720](https://user-images.githubusercontent.com/113497491/229770422-7ace9704-ae78-4a5c-894c-425675502d90.png)

## RESULT
Thus we have performed Multivariate EDA on the given data set.
