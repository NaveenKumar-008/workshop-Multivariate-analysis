# workshop-Multivariate-analysis  

## AIM:   

To Perform Multivariate Analysis  

## ALGORITHM:  

1.Read the given data  

2.Get information from the data  

3.Perform the Multivariate Analysis  

4.Save the clean data to file  

## PROGRAM:  
~~~  
Developed by: Naveen Kumar.M   
Regno: 212221040113  
~~~  
~~~  
import pandas as pd  


import numpy as np  


import matplotlib.pyplot as plt  


import seaborn as sns  


df=pd.read_excel("/content/FlightInformation.xlsx")  

~~~  

## Types of Bivariate Analysis:  

## (i) Numerical & Numerical  
sns.scatterplot(x='Duration',y='Dep_Time',data=df)

![w1](https://user-images.githubusercontent.com/128135244/229690310-365e6bff-9c2d-4970-be32-f38057c082eb.png)

## (ii) Numerical & Categorical
sns.barplot (x=df['Duration'],y=df['Price'])

![w2](https://user-images.githubusercontent.com/128135244/229690368-62ef3313-9f7c-4969-aab3-04c3a28e5de3.png)

sns.barplot(x=df["Arrival_Time"],y=df["Price"],data=df)

![w3](https://user-images.githubusercontent.com/128135244/229690385-2f2e4b12-71f9-466a-9ab9-fb82179d311f.png)

states=df.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()

![w4](https://user-images.githubusercontent.com/128135244/229690417-f768d2f4-ea32-425d-b249-264b3e5a52b8.png)

## Multivariate Analysis    

data = np.random.randint(low = 1, high = 100, size = (10, 10))  

hm = sns.heatmap(data = data)  

plt.show()  
![w5](https://user-images.githubusercontent.com/128135244/229690441-7ac1040b-6ec7-42e7-b029-ffe0b45e72c7.png)


## RESULT:  
Thus, Bivariate/Multivariate Analysis is performed  successfully.  





