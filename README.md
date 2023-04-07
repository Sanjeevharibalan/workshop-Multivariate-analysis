# WORKSHOP - MULTIVARIATE ANALYSIS

## AIM:

   To Perform Multivariate Analysis
## ALGORITHM:

1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file

## PROGRAM:

Types of Bivariate Analysis:

(i) Numerical & Numerical

Scatter plot

import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib as plt

df = pd.read_csv("/content/FlightInformation.csv")

sns.scatterplot (df['Price'],df['Arrival_Time'])

![Screenshot (174)](https://user-images.githubusercontent.com/86832944/194212468-20074106-79e1-499e-bbad-e3a742c75f4d.png)

ii) Numerical & Categorical

Bar Plot

import pandas as pd

import seaborn as sns

sns.barplot (x=df['Duration'],y=df['Price'])

![Screenshot (175)](https://user-images.githubusercontent.com/86832944/194212626-380f5284-6225-4cf2-b44d-2c006bc12672.png)

sns.barplot(x=df["Arrival_Time"],y=df["Price"],data=df)

![Screenshot (176)](https://user-images.githubusercontent.com/86832944/194212682-8ae8c7ae-e3bc-4721-98c7-4f661c8f7e0d.png)

states=df.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

import matplotlib.pyplot as plt

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()

![Screenshot (177)](https://user-images.githubusercontent.com/86832944/194212789-8c453aab-572d-4569-97f5-b04aa6812cf8.png)

Multivariate Analysis

df.corr()

![Screenshot (178)](https://user-images.githubusercontent.com/86832944/194212899-f3114575-857a-42b0-a471-82e9d2a7b6c4.png)

Categorical & Categorical Heatmap

import numpy as np

import seaborn as sn

import matplotlib.pyplot as plt

data=pd.read_csv("/content/FlightInformation.csv")

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sn.heatmap(data = data)

plt.show()

![Screenshot (179)](https://user-images.githubusercontent.com/86832944/194213017-2139a100-5954-4f14-9d20-6285a5c2619d.png)

## RESULT:
Thus, Bivariate/Multivariate Analysis is performed  successfully.








