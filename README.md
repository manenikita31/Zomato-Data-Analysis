# Zomato-Data-Analysis
#Analysis of the Zomato Data
#Step 1 : Importing Libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

#Step 2 : Create the dataframe
dataframe = pd.read_csv("Zomato data .csv")

#Convert the datatype of column -rate
def handleRate(value):
    value = str(value).split('/')
    value = value[0];
    return float(value)
dataframe['rate']=dataframe['rate'].apply(handleRate)
print(dataframe.head())

#Type of restaurant
sns.countplot(x=dataframe['listed_in(type)'])
plt.xlabel("Type of Restaurant")
plt.show()

#Conclusion - majority of the restaurant falls in dinning category

grouped_data = dataframe.groupby('listed_in(type)')['votes'].sum()
result = pd.DataFrame({'votes': grouped_data})
plt.plot(result,c="red",marker="o")
plt.xlabel("Type of Restaurant", c="red", size =20)
plt.ylabel("Votes",c="red" ,size=20)
plt.show()

#Conclusion - dinning restaurant has recieved maximum votes

plt.hist(dataframe["rate"],bins=5)
plt.title("Ratings Distribution")
plt.show()

#Conclusion - The Majority restaurant recieved ratings from 3.5 to 4

#Average order spending by couples
couple_data = dataframe['approx_cost(for two people)']
sns.countplot(x=couple_data)
plt.show()

#Conclusion - the majority of couples prefer with an approximate cost of 300 rupees

#Which mode receives maximum ratings
plt.figure(figsize=(6,6))
sns.boxenplot(x='online_order',y='rate', data= dataframe)
plt.show()

#Conclusion - Offline order recieved lower rating in comparison to online order
pivot_table = dataframe.pivot_table(index='listed_in(type)',columns='online_order',aggfunc='size',fill_value=0)
sns.heatmap(pivot_table,annot= True, cmap="YlGnBu", fmt='d')
plt.title("Heatmap")
plt.xlabel("Online Order")
plt.ylabel("Listed In (Type)")
plt.show()

#Conclusion: Dinning restaurants primarily accept offline orders, whereas cafes primarily receive online orders. This suggests that clients prefer offline order in person at restaurants, but prefer online orders at cafes.
