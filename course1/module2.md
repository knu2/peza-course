# Module 2: Working with Data Structures and AI (5 Hours)

*Master Python's core data structures and learn how to use AI to manipulate and analyze collections of data*

## Table of Contents
- [Objective](#objective)
- [Topics and Content Breakdown](#topics-and-content-breakdown)
  - [1. Lists](#1-lists-creating-indexing-and-modifying-1-hour-)
  - [2. Dictionaries](#2-dictionaries-key-value-pairs-for-structured-data-1-hour-)
  - [3. Loops](#3-loops-iterating-over-data-with-for-loops-1-hour-)
  - [4. Using AI to Simplify](#4-using-ai-to-simplify-data-structure-tasks-1-hour-)
  - [5. Mini-Project](#5-mini-project-analyzing-temperature-data-with-ai-assistance-1-hour-30-minutes-)
  - [6. Check Your Understanding](#6-check-your-understanding-module-2-review-15-minutes-)
- [Visual Learning Aids](#visual-learning-aids)
- [Additional Resources](#additional-resources)

## Objective
By the end of this module, you'll understand Python's core data structures (lists and dictionaries) and how to use loops to process data efficiently. You'll also learn how to leverage your AI assistant to manipulate and analyze these structures, setting the foundation for more advanced data analytics tasks in later modules.

## Topics and Content Breakdown

### 1. Lists: Creating, Indexing, and Modifying (1 hour)
- **What You'll Learn**: How to work with lists—Python's versatile data structure for storing collections of items in a specific order.
- **Content**:
  - **What are Lists?**: Ordered collections of items that can store different data types.
    - Example: `sales = [100, 200, 150]` (a list of sales figures)
    - Example: `products = ["apples", "bananas", "oranges"]` (a list of product names)
  - **Creating Lists**:
    - Basic syntax: `my_list = [item1, item2, item3]`
    - Empty list: `empty_list = []`
    - Lists with mixed types: `user_data = ["Alex", 25, True]` (name, age, active status)
  - **Accessing List Elements**:
    - Indexing (starts at 0): `products[0]` gives `"apples"`
    - Negative indexing: `products[-1]` gives `"oranges"` (last item)
    - Slicing: `products[0:2]` gives `["apples", "bananas"]` (first two items)
  - **Modifying Lists**:
    - Adding items: `products.append("grapes")` adds to the end
    - Inserting items: `products.insert(1, "pears")` adds at position 1
    - Removing items: `products.remove("bananas")` or `del products[1]`
    - Updating items: `products[0] = "green apples"`
  - **List Methods**:
    - `len(products)` - get list length
    - `products.sort()` - sort alphabetically/numerically
    - `products.reverse()` - reverse order
    - `", ".join(products)` - convert to string with separator
  - **Data Analytics Connection**: Lists are fundamental for storing datasets like sales figures, customer names, or product inventories. They're often the starting point for data analysis.
- **Activity** (40 min):
  - **Checkpoint 1** (15 min): Create a list of 5 monthly sales figures and perform these operations:
    - Print the first and last sales figures
    - Add a new month's sales
    - Calculate the total sales (hint: use `sum()`)
    - Find the highest sales month (hint: use `max()`)
  - **Checkpoint 2** (15 min): Ask your AI assistant: "Write code to find the average value in this list: [23, 45, 67, 89, 43, 56]" and explain how it works.
  - **Checkpoint 3** (10 min): Create a list of product names and prices (as separate lists), then ask your AI assistant to help you access corresponding elements (e.g., "How do I get the price of the 2nd product?").

### 2. Dictionaries: Key-Value Pairs for Structured Data (1 hour)
- **What You'll Learn**: How to use dictionaries to store and retrieve data using descriptive keys instead of numeric indices.
- **Content**:
  - **What are Dictionaries?**: Collections of key-value pairs where each key acts as a unique identifier for its associated value.
    - Example: `product_sales = {"apples": 50, "bananas": 30, "oranges": 45}`
    - Keys are typically strings, but can be any immutable type
    - Values can be any data type (numbers, strings, lists, other dictionaries)
  - **Creating Dictionaries**:
    - Basic syntax: `my_dict = {"key1": value1, "key2": value2}`
    - Empty dictionary: `empty_dict = {}`
    - Dictionary with mixed value types: `user = {"name": "Alex", "age": 25, "active": True}`
  - **Accessing Dictionary Values**:
    - Using keys: `product_sales["apples"]` gives `50`
    - Using `.get()`: `product_sales.get("apples")` (safer, returns `None` if key doesn't exist)
    - Checking if a key exists: `if "apples" in product_sales:`
  - **Modifying Dictionaries**:
    - Adding/updating items: `product_sales["grapes"] = 25`
    - Removing items: `del product_sales["bananas"]` or `product_sales.pop("bananas")`
    - Clearing all items: `product_sales.clear()`
  - **Dictionary Methods**:
    - `product_sales.keys()` - get all keys
    - `product_sales.values()` - get all values
    - `product_sales.items()` - get key-value pairs as tuples
  - **Nested Dictionaries**: Dictionaries within dictionaries for complex data.
    ```python
    store_sales = {
        "store1": {"apples": 50, "bananas": 30},
        "store2": {"apples": 40, "bananas": 35}
    }
    ```
  - **Data Analytics Connection**: Dictionaries are perfect for structured data like sales by product, customer information, or survey responses. They make it easy to look up values by meaningful names rather than positions.
- **Activity** (40 min):
  - **Checkpoint 1** (15 min): Create a dictionary of product prices:
    ```python
    prices = {"apple": 1.20, "banana": 0.50, "orange": 0.80, "grape": 2.50, "kiwi": 1.00}
    ```
    Then:
    - Print the price of oranges
    - Add a new product with its price
    - Calculate the total price of buying 2 apples, 3 bananas, and 1 kiwi
  - **Checkpoint 2** (15 min): Ask your AI assistant: "Write code to find the most expensive product in this dictionary" and explain the solution.
  - **Checkpoint 3** (10 min): Create a nested dictionary for weekly sales by product, then ask your AI assistant to help you access specific values (e.g., "How do I get the sales of bananas on Wednesday?").

### 3. Loops: Iterating Over Data with For Loops (1 hour)
- **What You'll Learn**: How to process collections of data efficiently by repeating operations on each item.
- **Content**:
  - **What are Loops?**: Programming constructs that repeat a block of code multiple times.
  - **For Loops with Lists**:
    ```python
    products = ["apples", "bananas", "oranges"]
    for product in products:
        print(f"We sell {product}")
    ```
  - **For Loops with Dictionaries**:
    ```python
    # Looping through keys
    for product in product_sales:
        print(product)
        
    # Looping through key-value pairs
    for product, sales in product_sales.items():
        print(f"We sold {sales} {product}")
    ```
  - **Range Function**: Generate sequences of numbers for loops.
    ```python
    # Print numbers 0 to 4
    for i in range(5):
        print(i)
        
    # Print numbers 1 to 5
    for i in range(1, 6):
        print(i)
    ```
  - **List Comprehensions**: Concise way to create lists based on existing lists.
    ```python
    # Double each number in a list
    numbers = [1, 2, 3, 4, 5]
    doubled = [num * 2 for num in numbers]
    # Result: [2, 4, 6, 8, 10]
    ```
  - **Common Loop Patterns**:
    - Summing values: `total = sum(sales)` or with a loop
    - Finding maximum/minimum: `max_sale = max(sales)` or with a loop
    - Filtering data: Keep only items that meet certain criteria
    - Transforming data: Apply operations to each item
  - **Data Analytics Connection**: Loops are essential for data processing tasks like calculating statistics, cleaning data, or transforming datasets. They allow you to automate repetitive operations across large datasets.
- **Activity** (40 min):
  - **Checkpoint 1** (15 min): Write a loop to calculate the total cost of items in a shopping list:
    ```python
    prices = {"apple": 1.20, "banana": 0.50, "orange": 0.80}
    shopping_list = ["apple", "apple", "banana", "orange", "banana"]
    ```
  - **Checkpoint 2** (15 min): Ask your AI assistant: "Write a loop that counts how many times each item appears in this list: ['apple', 'banana', 'apple', 'orange', 'apple', 'banana']" and explain the solution.
  - **Checkpoint 3** (10 min): Use a list comprehension to create a list of squared numbers from 1 to 10. Ask your AI assistant for help if needed.

### 4. Using AI to Simplify Data Structure Tasks (1 hour)
- **What You'll Learn**: How to leverage your AI assistant to generate, manipulate, and clean data structures.
- **Content**:
  - **AI-Assisted Data Structure Creation**:
    - Generating sample data: "Create a list of 10 random sales figures"
    - Creating complex nested structures: "Generate a dictionary of store locations with product sales"
  - **AI-Assisted Data Cleaning**:
    - Removing duplicates: "Write code to remove duplicates from this list"
    - Fixing data types: "Convert these string numbers to integers"
    - Handling missing values: "Replace None values with zeros in this list"
  - **AI-Assisted Data Transformation**:
    - Converting between structures: "Convert this list of tuples to a dictionary"
    - Restructuring data: "Reorganize this nested dictionary by product instead of by store"
    - Filtering data: "Keep only the products with sales over 100"
  - **AI-Generated Loop Solutions**:
    - Complex iterations: "Write a loop to process this nested data structure"
    - Optimized solutions: "What's a more efficient way to calculate these statistics?"
  - **Effective Prompting for Data Tasks**:
    - Be specific about your data structure: "I have a list of dictionaries where each dictionary has 'name' and 'sales' keys"
    - Describe the desired outcome: "I want to group sales by product category"
    - Ask for explanations: "Explain how this list comprehension works"
  - **Data Analytics Connection**: AI can dramatically speed up data preparation tasks, allowing you to focus on analysis and insights rather than coding mechanics.
- **Activity** (40 min):
  - **Checkpoint 1** (15 min): Ask your AI assistant to generate a messy dataset (a list with duplicates, missing values, and incorrect types), then ask for help cleaning it.
  - **Checkpoint 2** (15 min): Have your AI assistant convert a dataset between formats (e.g., from a list of lists to a list of dictionaries) and explain the transformation.
  - **Checkpoint 3** (10 min): Ask your AI assistant to write a complex loop that performs multiple operations on a dataset (e.g., filtering, transforming, and summarizing sales data).

### 5. Mini-Project: Analyzing Temperature Data with AI Assistance (1 hour 30 minutes)
- **What You'll Learn**: How to apply lists, dictionaries, and loops to analyze a real dataset with AI help.
- **Content**:
  - **Scenario**: You have daily temperature readings for a month and want to analyze patterns and statistics.
  - **The Dataset**:
    ```python
    temperatures = {
        "week1": [72, 75, 78, 79, 81, 80, 83],
        "week2": [81, 79, 77, 76, 78, 80, 82],
        "week3": [82, 83, 85, 86, 83, 81, 79],
        "week4": [76, 77, 75, 74, 73, 72, 74]
    }
    ```
  - **Analysis Tasks**:
    1. Calculate the average temperature for each week
    2. Find the hottest and coldest days of the month
    3. Count days above 80 degrees
    4. Determine which week had the most consistent temperatures (lowest standard deviation)
  - **AI's Role**: Ask the AI to help write code for specific analyses, explain statistical concepts, or suggest additional insights.
- **Activity** (1 hr 20 min):
  - **Checkpoint 1** (15 min): Set up the temperature dataset and ask your AI assistant to help calculate the average temperature for each week.
  - **Checkpoint 2** (20 min): Ask your AI assistant to write code to find the hottest and coldest days, including which weeks they occurred in.
  - **Checkpoint 3** (20 min): Have your AI assistant help you count the number of days in each temperature range (e.g., <75°F, 75-80°F, >80°F).
  - **Checkpoint 4** (15 min): Ask your AI assistant to explain how to calculate standard deviation and help you determine which week had the most consistent temperatures.
  - **Final Analysis** (10 min): Combine all your analyses into a summary report with key findings. Ask your AI assistant to help format the results clearly.

### 6. Check Your Understanding: Module 2 Review (15 minutes)
- **Self-Assessment Quiz**:
  1. What's the difference between a list and a dictionary in Python?
  2. How would you access the third element in a list? What about the last element?
  3. If you have `product_sales = {"apples": 50, "bananas": 30}`, how would you add a new product "oranges" with 45 sales?
  4. Write a for loop that prints each character in the string "Python".
  5. What's a list comprehension and when might you use one?
- **Looking Ahead**: In Module 3, we'll build on these data structures by introducing Pandas, a powerful library that combines the best features of lists and dictionaries into DataFrame objects specifically designed for data analysis.

## Visual Learning Aids

```
# List vs Dictionary
LIST                          DICTIONARY
┌─────┬─────┬─────┬─────┐    ┌─────────┬───────┐
│ 0   │ 1   │ 2   │ 3   │    │ "apple" │ 1.20  │
├─────┼─────┼─────┼─────┤    ├─────────┼───────┤
│ 100 │ 200 │ 150 │ 300 │    │"banana" │ 0.50  │
└─────┴─────┴─────┴─────┘    ├─────────┼───────┤
  Accessed by position        │"orange" │ 0.80  │
  sales[2] → 150             └─────────┴───────┘
                               Accessed by key
                               prices["apple"] → 1.20
```

```
# For Loop Execution Flow
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ Start with  │     │ Execute     │     │ Move to     │
│ first item  │ ──> │ code block  │ ──> │ next item   │
└─────────────┘     └─────────────┘     └─────────────┘
                           │                   │
                           │                   │
                           ▼                   │
                    ┌─────────────┐           │
                    │ Any more    │ No        │
                    │ items?      │◄──────────┘
                    └─────────────┘
                           │
                           │ Yes
                           ▼
                    ┌─────────────┐
                    │ Repeat with │
                    │ next item   │
                    └─────────────┘
```

```
# Nested Data Structures
store_sales = {
    "store1": {"apples": 50, "bananas": 30},
    "store2": {"apples": 40, "bananas": 35}
}

Access: store_sales["store1"]["apples"] → 50
```

## Additional Resources
- [Python Data Structures Tutorial](https://docs.python.org/3/tutorial/datastructures.html)
- [Real Python - Python Lists and Dictionaries](https://realpython.com/python-lists-tuples/)
- [W3Schools Python Lists](https://www.w3schools.com/python/python_lists.asp)
- [W3Schools Python Dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)
- [Python for Data Analysis (Book by Wes McKinney)](https://wesmckinney.com/book/)