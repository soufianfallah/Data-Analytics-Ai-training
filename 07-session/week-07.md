# Week 07 – Python for Data Analysis: Challenges, Data Types, Pandas, and Visualization

## 📚 Topics Covered
- Python foundations for data analytics  
- Coding challenges to practice logic, loops, conditions, and functions  
- Understanding Python data types: lists, tuples, dictionaries, sets  
- Introduction to Pandas for data manipulation  
- Basics of data visualization using Matplotlib and Seaborn  
- Working with real datasets to explore insights  

## 🧰 Tools & Setup
- Python 3.x environment  
- VS Code + Jupyter Notebooks  
- Pandas for data cleaning and transformation  
- Matplotlib and Seaborn for visualizations  
- Sample CSV files for hands-on exercises  

## 🧑‍💻 Code / Example
```python
import pandas as pd

df = pd.read_csv("sales.csv")
df.head()

# Basic stats
df.describe()

# Grouping example
monthly_sales = df.groupby("month")["revenue"].sum()
print(monthly_sales)
# Simple visualization
import matplotlib.pyplot as plt
import seaborn as sns

sns.barplot(data=df, x="month", y="revenue")
plt.title("Monthly Revenue")
plt.show()
```
🔍 Case Studies / Exercises

Solved Python logic puzzles to improve problem-solving

Practiced manipulating lists, dictionaries, and nested structures

Loaded datasets with Pandas and explored .head(), .info(), .describe()

Cleaned missing values, filtered rows, created new columns

Built basic visualizations: bar charts, line charts, and distributions

Combined Pandas + Seaborn to analyze patterns in a dataset

💡 Insights

Python becomes powerful when combined with libraries like Pandas

Understanding data types makes data cleaning MUCH easier

Visualization is essential for spotting patterns before modeling

Pandas is the backbone of most data analytics workflows

Clean and well-structured data makes AI and ML much more reliable

