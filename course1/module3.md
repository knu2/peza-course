# Module 3: Introduction to Data Analytics with Pandas and AI (6 Hours)

*Learn how to analyze real-world data using Python's most popular data analysis library*

## Table of Contents
- [Objective](#objective)
- [Topics and Content Breakdown](#topics-and-content-breakdown)
  - [1. What is Data Analytics?](#1-what-is-data-analytics-real-world-examples-30-minutes-)
  - [2. Installing and Importing Pandas](#2-installing-and-importing-pandas-30-minutes-)
  - [3. Loading Data](#3-loading-data-csv-files-or-simple-tables-1-hour-)
  - [4. Basic Pandas Operations](#4-basic-pandas-operations-filtering-sorting-and-summarizing-1-hour-30-minutes-)
  - [5. AI Assistance](#5-ai-assistance-using-ai-to-write-pandas-code-for-specific-tasks-1-hour-)
  - [6. Mini-Project](#6-mini-project-analyze-a-small-sales-dataset-with-ai-help-1-hour-30-minutes-)
  - [7. Check Your Understanding](#7-check-your-understanding-module-3-review-15-minutes-)
- [Visual Learning Aids](#visual-learning-aids)
- [Additional Resources](#additional-resources)

## Objective
By the end of this module, you'll be able to use Pandas—a powerful Python library—to load, clean, and explore datasets with the help of your AI assistant. Building on the Python fundamentals from Module 1 and data structures from Module 2, this module introduces you to data analytics, teaching you how to handle real-world data like sales records, preparing you for visualization in Module 4 and predictive tasks in Module 5.

### Learning Outcomes
- **Understand** the fundamentals of data analytics and its real-world applications
- **Install and import** Pandas in your Python environment
- **Load and create** DataFrames from various data sources
- **Manipulate data** using filtering, sorting, and grouping operations
- **Calculate statistics** and generate summaries from your datasets
- **Leverage AI assistance** to accelerate your data analysis workflow
- **Apply your skills** to analyze a realistic sales dataset

> **Key Skills**: Data loading, DataFrame manipulation, filtering, sorting, statistical analysis, AI-assisted data exploration

## Topics and Content Breakdown

### 1. What is Data Analytics? Real-World Examples (30 minutes) 📊
**What You'll Learn**: Data analytics is about extracting insights from data to make decisions, and Python with Pandas makes it accessible.

**Content**:
- **Definition**: Turning raw data (numbers, text) into meaningful information (trends, summaries).
- **Examples**:
  - Businesses analyze sales data to identify top products.
  - Researchers study survey results to understand preferences.
  - Weather analysts summarize temperature data for forecasts.
- **Why Pandas?**: 
  - Built on NumPy, it simplifies data manipulation with DataFrames (like spreadsheets in Python).
  - Perfect for beginners transitioning from lists/dictionaries to structured data analysis.
- **Quick Demo**: Imagine analyzing sales data—Pandas can load it, filter it, and summarize it in a few lines!

```python
import pandas as pd
sales = pd.DataFrame({"product": ["apple", "banana"], "sales": [50, 30]})
print(sales["sales"].mean())  # Average sales: 40
```

**Activity (15 min)**:
- **Reflect**: Write down one real-world question you'd like to answer with data (e.g., "Which of my expenses is growing fastest?" or "What's my best-selling item?"). No coding yet—just ideas!

### 2. Installing and Importing Pandas (30 minutes) 🛠️
**What You'll Learn**: How to add Pandas to your Python environment and start using it.

**Content**:
- **Installation**:
  - Google Colab: Already included, no setup needed.
  - Local Install: Open a terminal and run `pip install pandas` (or `pip3 install pandas` on some systems).
  - Test it: `import pandas`—if no error, you're set!
- **Importing**:
  - Standard convention: `import pandas as pd` (shortens commands like `pd.read_csv()`).
- **Basic Check**:

```python
import pandas as pd
print(pd.__version__)  # Shows Pandas version, e.g., "2.0.3"
```

- **Why This Matters**: Pandas is your bridge to data analytics—it turns messy data into organized tables you can analyze.

**Activity (20 min)**:
- In your notebook, run `import pandas as pd` and print the version.
- Ask your AI assistant: "What's the latest version of Pandas, and why does it matter?" Note the response.

### 3. Loading Data: CSV Files or Simple Tables (1 hour) 📥
**What You'll Learn**: How to bring data into Python using Pandas for analysis.

**Content**:
- **What's a CSV?**: Comma-separated values file, a common data format (like a spreadsheet saved as text).
- **Loading a CSV**:

```python
import pandas as pd
df = pd.read_csv("sales_data.csv")  # Replace with your file path
print(df)  # Displays the table
```

- **Creating Data Manually**:

```python
data = {"product": ["apple", "banana", "orange"], "sales": [50, 30, 45]}
df = pd.DataFrame(data)
print(df)
```

- **Exploring the DataFrame**:
  - `df.head()` - See first 5 rows
  - `df.columns` - List column names
  - `df.shape` - Rows and columns count (e.g., (3, 2))
- **AI's Role**: If you don't have a CSV, ask the AI: "Generate a sample CSV with product names and sales."
- **Data Analytics Connection**: Loading data is the first step to analysis—Pandas makes it easy to work with real datasets.

**Activity (40 min)**:
- **Checkpoint 1 (15 min)**: Ask your AI assistant to create a small sales dataset as a dictionary (e.g., 5 products with sales figures), then convert it to a DataFrame and print it.
- **Checkpoint 2 (15 min)**: Ask your AI assistant: "Write code to load this CSV data into a DataFrame and show the first 3 rows." Use a sample CSV the AI generates if you don't have one.
- **Checkpoint 3 (10 min)**: Explore your DataFrame—print its shape and column names.

### 4. Basic Pandas Operations: Filtering, Sorting, and Summarizing (1 hour 30 minutes) 🔍
**What You'll Learn**: How to manipulate and summarize data with Pandas for insights.

**Content**:
- **Filtering**:
  - Select columns: `df["product"]` or `df[["product", "sales"]]`
  - Filter rows: `df[df["sales"] > 40]` (rows where sales exceed 40)
- **Sorting**:
  - Sort by column: `df.sort_values("sales")` (ascending) or `df.sort_values("sales", ascending=False)` (descending)
- **Summarizing**:
  - `df.describe()` - Stats like mean, min, max for numeric columns
  - `df["sales"].sum()` - Total sales
  - `df["sales"].mean()` - Average sales
- **Grouping**:

```python
# Assuming a "category" column
df.groupby("category")["sales"].sum()  # Total sales by category
```

- **AI Assistance**:
  - "Filter rows where sales are above 100."
  - "Sort this DataFrame by sales and show the top 5."
  - "Calculate the average sales for me."
- **Data Analytics Connection**: These operations let you answer questions like "What's my top product?" or "Which categories perform best?"

**Activity (1 hr)**:
- **Checkpoint 1 (20 min)**: Using your DataFrame, filter for products with sales over 40 and print the result.
- **Checkpoint 2 (20 min)**: Sort your DataFrame by sales (highest to lowest) and ask your AI assistant to explain the code.
- **Checkpoint 3 (20 min)**: Summarize your data—calculate total sales, average sales, and use `describe()`. Ask your AI assistant to interpret the results.

### 5. AI Assistance: Using AI to Write Pandas Code for Specific Tasks (1 hour) 🤖
**What You'll Learn**: How to use your AI assistant to simplify complex Pandas operations.

**Content**:
- **Common Pandas Tasks with AI**:
  - Cleaning: "Remove rows with missing sales values."
  - Merging: "Combine these two DataFrames by product name."
  - Analysis: "Find the top 3 products by sales."
- **Prompting Examples**:
  - "Write Pandas code to find rows where sales exceed the average."
  - "Show me how to group sales by product and calculate totals."
  - "Fix this error: 'KeyError: sales' in my DataFrame."
- **Iterating with AI**:
  - If the code fails, refine your prompt: "The column is 'revenue', not 'sales'—fix it."
  - Ask for alternatives: "Show me another way to filter this data."
- **Data Analytics Connection**: AI accelerates analytics by handling syntax and errors, letting you focus on insights.

**Activity (40 min)**:
- **Checkpoint 1 (15 min)**: Ask your AI assistant to write code to find the top-selling product in your DataFrame.
- **Checkpoint 2 (15 min)**: Introduce an error (e.g., use a wrong column name) and ask your AI assistant to debug it.
- **Checkpoint 3 (10 min)**: Ask your AI assistant for a creative analysis idea (e.g., "How could I analyze trends in this data?") and implement it.

### 6. Mini-Project: Analyze a Small Sales Dataset with AI Help (1 hour 30 minutes) 🚀
**What You'll Learn**: Apply Pandas and AI to explore and summarize a sales dataset.

**Content**:
- **Scenario**: You're a small business owner analyzing last month's sales.
- **The Dataset**:

```python
import pandas as pd
data = {
    "product": ["apple", "banana", "orange", "grape", "kiwi"],
    "price": [1.20, 0.50, 0.80, 2.50, 1.00],
    "quantity": [50, 80, 60, 20, 30]
}
df = pd.DataFrame(data)
```

- **Analysis Tasks**:
  - Calculate total revenue per product (price × quantity)
  - Identify the top-selling product by quantity and revenue
  - Summarize average price and total revenue across all products
  - Filter for products with revenue above $50
- **AI's Role**: Ask for code snippets, explanations, or fixes as needed.

**Activity (1 hr 20 min)**:
- **Checkpoint 1 (15 min)**: Set up the dataset and calculate revenue per product (add as a new column).
- **Checkpoint 2 (20 min)**: Ask your AI assistant to help identify the top product by quantity and revenue.
- **Checkpoint 3 (20 min)**: Summarize the dataset (total revenue, average price) and ask your AI assistant to format the output clearly.
- **Checkpoint 4 (15 min)**: Filter high-revenue products and ask your AI assistant to suggest one additional insight (e.g., "Which product has the best price-to-quantity ratio?").
- **Final Review (10 min)**: Compile your findings into a short report (e.g., "Top product by revenue: X, Total revenue: Y").

### 7. Check Your Understanding: Module 3 Review (15 minutes) ✅
**Self-Assessment Quiz**:
1. What's the difference between a Python dictionary and a Pandas DataFrame?
2. How would you load a CSV file named "data.csv" into a DataFrame?
3. If df is a DataFrame, how do you find the average of the "price" column?
4. What does `df.describe()` do?
5. How might you ask an AI assistant to help with a Pandas error?

**Looking Ahead**: In Module 4, we'll use Matplotlib to visualize this data, turning numbers into charts for deeper insights.

## Visual Learning Aids

### DataFrame Structure
```
   ┌──────────┬───────┬─────────┐
   │ product  │ price │ quantity│ <- Column names
   ├──────────┼───────┼─────────┤
0  │ apple    │ 1.20  │ 50      │ <- Row index
1  │ banana   │ 0.50  │ 80      │
2  │ orange   │ 0.80  │ 60      │
   └──────────┴───────┴─────────┘
```
- Access: `df["price"]` → [1.20, 0.50, 0.80]
- Filter: `df[df["quantity"] > 50]` → Rows for banana, orange

### Pandas Workflow
```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ Load data   │ ──> │ Clean and   │ ──> │ Analyze and │
│ into a      │     │ manipulate  │     │ summarize   │
│ DataFrame   │     │ with Pandas │     │ with Pandas │
└─────────────┘     └─────────────┘     └─────────────┘
```

### AI-Assisted Pandas
```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ You ask AI  │ ──> │ AI provides │ ──> │ You run and │
│ for Pandas  │     │ code or     │     │ refine the  │
│ help        │     │ fixes       │     │ analysis    │
└─────────────┘     └─────────────┘     └─────────────┘
```

## Additional Resources

### Documentation and Tutorials
- [Pandas Official Documentation](https://pandas.pydata.org/docs/) - Comprehensive reference
- [Real Python - Pandas Basics](https://realpython.com/pandas-python-explore-dataset/) - Practical tutorial with examples
- [W3Schools Pandas Tutorial](https://www.w3schools.com/python/pandas/default.asp) - Interactive learning
- [Kaggle Pandas Course](https://www.kaggle.com/learn/pandas) - Free course with exercises

### Practice Datasets
- [Kaggle Datasets](https://www.kaggle.com/datasets) - Thousands of real-world datasets
- [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php) - Classic datasets for practice

### Cheat Sheets
- [Pandas Cheat Sheet (PDF)](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf) - Quick reference guide