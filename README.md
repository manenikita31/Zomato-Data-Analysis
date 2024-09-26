# **Overview**
This project involves analyzing a dataset from Zomato to understand various aspects of restaurant ratings, types, and ordering preferences. The analysis is conducted using Python with libraries such as Pandas, NumPy, Matplotlib, and Seaborn.

# **Table of Contents**
+ Project Structure
+ Dependencies
+ Dataset
+ Analysis Steps
+ Conclusions
+ Usage

# **Project Structure**
+ Zomato_Analysis│
  - Zomato data.csv                   # Dataset used for analysis
  - dataanalysis.py                   # Python script containing the analysis code
  - README.md                         # Project documentation

# **Dependencies**
To run this project, ensure you have the following libraries installed:

+ pandas
+ numpy
+ matplotlib
+ seaborn

# **Dataset**
The dataset used in this analysis is Zomato data.csv. It contains information about restaurants, including:

+ Ratings
+ Votes
+ Types of cuisine
+ Approximate costs
+ Online ordering options

# **Analysis Steps**
**1. Import Libraries:** Load the necessary libraries for data manipulation and visualization.

**2. Load Data:** Read the CSV file into a Pandas DataFrame.

**3. Data Cleaning:** Convert the 'rate' column into a numeric format for analysis.

**4. Visualization:**
+ Count the number of restaurants by type.
+ Analyze the total votes received by each type of restaurant.
+ Examine the distribution of ratings.
+ Analyze spending behavior for couples.
+ Compare ratings based on online and offline ordering modes.
+ Create a heatmap to visualize the relationship between restaurant type and online ordering.

# **Conclusions**
+ Restaurant Type: The majority of restaurants fall into the dining category.
+ Votes Received: Dining restaurants receive the maximum votes compared to other types.
+ Rating Distribution: Most restaurants have ratings ranging from 3.5 to 4.
+ Couples' Spending: The majority of couples prefer to spend around 300 rupees.
+ Order Mode Ratings: Online orders receive higher ratings compared to offline orders.
+ Ordering Preferences: Dining restaurants mainly accept offline orders, while cafes tend to receive more online orders.

# **Usage**
To run the analysis, execute the dataanalysis.py script:

python dataanalysis.py
Make sure the dataset (Zomato data.csv) is in the same directory as the script.

# **Acknowledgments**
This project is based on publicly available data from Zomato. The insights drawn from this analysis can help stakeholders understand customer preferences and improve their service offerings.



