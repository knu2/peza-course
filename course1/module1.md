# Module 1: Getting Started with Python and AI (4 Hours)

*Learn Python basics and discover how to use AI as your coding partner*

## Table of Contents
- [Objective](#objective)
- [Topics and Content Breakdown](#topics-and-content-breakdown)
  - [1. Introduction to Python](#1-introduction-to-python-what-it-is-and-why-its-great-for-data-analytics-30-minutes-)
  - [2. Setting Up Your Environment](#2-setting-up-your-environment-python-notebook-options-and-local-install-30-minutes-)
  - [3. Meeting Your AI Assistant](#3-meeting-your-ai-assistant-how-to-ask-for-code-examples-explanations-and-fixes-30-minutes-)
  - [4. Basic Syntax](#4-basic-syntax-variables-printing-and-simple-operations-1-hour-)
  - [5. Mini-Project](#5-mini-project-use-ai-to-write-a-script-that-analyzes-weekly-expenses-1-hour-30-minutes-)
  - [6. Check Your Understanding](#6-check-your-understanding-module-1-review-15-minutes-)
- [Visual Learning Aids](#visual-learning-aids)
- [Additional Resources](#additional-resources)

## Objective
By the end of this module, you'll understand the basics of Python, set up a coding environment, and learn how to use an AI assistant to write and understand code. This module lays the foundation for using Python and AI together for data analytics, enabling you to start building the skills needed for real-world data analysis tasks.

## Topics and Content Breakdown

### 1. Introduction to Python: What It Is and Why It's Great for Data Analytics (30 minutes)
- **What You'll Learn**: Python is a versatile, beginner-friendly programming language widely used in data analytics for tasks like data cleaning, visualization, and modeling.
- **Content**:
  - **What is Python?**: A high-level language created by Guido van Rossum in 1991, known for its readability and massive community support.
  - **Why Python for Data Analytics?**:
    - Simple syntax makes it easy to learn.
    - Powerful libraries like Pandas (data manipulation), Matplotlib (visualization), and NumPy (numerical operations) are perfect for analytics.
    - AI integration (e.g., tools like Grok!) simplifies coding tasks.
  - **Real-World Example**: Companies like Netflix use Python to analyze viewing trends and recommend shows—your first step toward that!
  - **Data Analytics Preview**: Brief demonstration of a simple data analysis you'll be able to perform by the end of the course:
    ```python
    # This is what you'll be able to do later in the course!
    import pandas as pd
    import matplotlib.pyplot as plt
    
    # Load and analyze sales data
    sales = pd.read_csv('sales_data.csv')
    monthly_sales = sales.groupby('month')['amount'].sum()
    
    # Visualize the results
    monthly_sales.plot(kind='bar')
    plt.title('Monthly Sales Performance')
    plt.show()
    ```
- **Activity** (10 min):
  - Reflect: Write down one way you think Python could help with a real-life data task (e.g., tracking expenses, analyzing survey results, identifying patterns in customer behavior). No coding yet—just ideas!

### 2. Setting Up Your Environment: Python Notebook Options and Local Install (30 minutes)
- **What You'll Learn**: How to get Python running so you can start coding.
- **Content**:
  - **Option 1: Cloud Notebooks** (Recommended for Beginners):
    - **Google Colab**: Free, cloud-based platform requiring no installation.
      - Open [colab.google](https://colab.research.google.com/), sign in with a Google account, and create a new notebook.
    - **Kaggle Notebooks**: Another free option with built-in datasets for practice.
      - Visit [kaggle.com](https://www.kaggle.com/) and create an account.
    - **JupyterLite**: Browser-based option that doesn't require Google login.
      - Access at [jupyterlite.github.io/demo](https://jupyterlite.github.io/demo/)
    - **Understanding Notebook Cells**:
      - Code cells: Where you write and run Python code (hit Shift+Enter to execute)
      - Markdown cells: For notes and documentation
  - **Option 2: Local Install** (For those who want it on their computer):
    - Download Python from [python.org](https://www.python.org/downloads/) (version 3.9+ recommended).
    - Install it, then open an IDE like VS Code (free at [code.visualstudio.com](https://code.visualstudio.com/)).
    - Test it: Open a terminal in VS Code, type `python --version`, and then `print("Hello, Python!")` in a `.py` file.
    - *Advanced*: Consider using virtual environments (`venv`) to manage packages.
  - **Why This Matters**: A working setup is your sandbox for coding and analytics. Notebooks are particularly useful for data analytics as they allow you to mix code, visualizations, and explanations.
- **Activity** (20 min):
  - Set up Google Colab (or alternative if preferred). 
  - Create a new notebook with two cells:
    - A code cell with `print("I'm ready to code!")`
    - A markdown cell with "# My First Python Notebook"
  - Run the code cell and confirm it works. Take a screenshot or note the output.

### 3. Meeting Your AI Assistant: How to Ask for Code Examples, Explanations, and Fixes (30 minutes)
- **What You'll Learn**: How to use an AI assistant (like Grok!) as your coding partner.
- **Content**:
  - **What Can an AI Do?**:
    - Generate code: "Write a script to add two numbers."
    - Explain code: "What does `x = 5` mean?"
    - Debug errors: "Why does this code fail?"
    - Suggest improvements: "How can I make this code more efficient?"
  - **Effective Prompting Techniques**:
    - Be specific: "Show me how to print my name" vs. "Help with printing."
    - Provide context: "I'm a beginner trying to analyze sales data."
    - Ask for explanations: "Explain this code line by line: [code]"
    - Request examples: "Show me 3 different ways to calculate an average."
    - Iterate: If the AI's answer isn't perfect, refine your question!
  - **Example Interactions**:
    ```
    You: Write code to print 'Hello, world!'
    AI: print("Hello, world!")
    
    You: Explain what this code does line by line:
    x = 10
    y = 5
    result = x * y
    print(result)
    
    AI: Line 1: Creates a variable 'x' and assigns it the value 10.
    Line 2: Creates a variable 'y' and assigns it the value 5.
    Line 3: Multiplies x and y, then stores the result (50) in a variable called 'result'.
    Line 4: Prints the value stored in 'result' to the screen, which is 50.
    ```
  - **Handling AI Limitations**:
    - AI might make mistakes in complex code
    - If code doesn't work, ask for simpler alternatives
    - Always test AI-generated code before relying on it
  - **Why This Matters**: The AI will speed up your learning and help with analytics later (e.g., writing Pandas code for data cleaning or visualization).
- **Activity** (15 min):
  - Try these prompts with your AI assistant:
    1. "Write a Python script to print 'I'm learning Python!'" 
    2. "Explain what `print()` does in Python and give 3 different examples."
    3. "What's the difference between `=` and `==` in Python?"
  - Run the code from the first prompt and note how the AI explains concepts.

### 4. Basic Syntax: Variables, Printing, and Simple Operations (1 hour)
- **What You'll Learn**: Core Python building blocks for storing and manipulating data.
- **Content**:
  - **Variables**: Containers for data.
    - Example: `x = 5` (stores the number 5 in `x`).
    - Try: `name = "Alex"` (stores text, aka a string).
    - **Data Analytics Connection**: Variables store values like sales figures, customer counts, or product names.
  - **Printing**: Display output with `print()`.
    - Example: `print(x)` outputs `5`.
    - Combine: `print("My name is", name)` outputs `My name is Alex`.
    - **Data Analytics Connection**: Printing helps verify data and display analysis results.
  - **Simple Operations**:
    - Addition: `x + 3` (if `x = 5`, this is 8).
    - Multiplication: `y = 2 * 3` (stores 6 in `y`).
    - Strings: `"Hello" + " Python"` becomes `"Hello Python"`.
    - **Data Analytics Connection**: These operations let you calculate totals, averages, percentages, etc.
  - **Data Types in Python**:
    - Numbers: `int` (whole numbers), `float` (decimals)
    - Text: `str` (strings)
    - **Data Analytics Connection**: Different data types represent different kinds of information in your datasets.
  - **Why This Matters**: These are the basics for handling data (e.g., sales numbers, customer information) in any analysis.
- **Activity** (40 min):
  - Write and run:
    - `age = 25`
    - `print(age + 5)` (What's the output?)
    - `print("I am", age, "years old")`
  - Ask your AI assistant: "Show me how to calculate the average of 3 numbers and print the result." Run the code and tweak it (e.g., change the numbers).
  - **Debug Challenge**: Fix this code with AI help:
    ```python
    price = 9.99
    quantity = "3"
    total = price * quantity
    print("Total cost:", total)
    ```

### 5. Mini-Project: Use AI to Write a Script That Analyzes Weekly Expenses (1 hour 30 minutes)
- **What You'll Learn**: Combine variables, operations, and AI help for a practical data analysis task.
- **Content**:
  - **Scenario**: You want to track and analyze weekly spending across different categories.
  - **Steps**:
    1. Define variables for expenses: `food = 30`, `transport = 15`, `entertainment = 20`, etc.
    2. Calculate total: `total = food + transport + entertainment + ...`
    3. Calculate percentages: `food_percent = (food / total) * 100`
    4. Print analysis: `print(f"Food accounts for {food_percent:.1f}% of your expenses")`
  - **AI's Role**: Ask the AI to write the script, explain the calculations, or fix mistakes.
  - **Stretch Goal**: Add conditional analysis (e.g., "Your biggest expense category is X")
- **Activity** (1 hr 20 min):
  - **Checkpoint 1** (15 min): List 4-5 expense categories from your week with estimated amounts.
  - **Checkpoint 2** (20 min): Ask your AI assistant: "Write a Python script to add these expenses: [your numbers]." Run it in your environment.
  - **Checkpoint 3** (20 min): Ask your AI assistant to modify the script to calculate what percentage each category represents of the total.
  - **Checkpoint 4** (25 min): Add code to identify and print which category has the highest expense. Ask your AI for help if needed.
  - **Final Review** (10 min): Ask your AI assistant to explain how the final script works and how it relates to data analytics.

### 6. Check Your Understanding: Module 1 Review (15 minutes)
- **Self-Assessment Quiz**:
  1. What would `print(5 + "hello")` do in Python? Why?
  2. If `x = 10` and `y = 3`, what is the value of `x / y`?
  3. Name two advantages of using Python for data analytics.
  4. What's the difference between a code cell and a markdown cell in a notebook?
  5. How would you ask an AI assistant to help debug a Python error?
- **Looking Ahead**: In Module 2, we'll build on these basics to work with more complex data structures like lists and dictionaries, which are essential for organizing and analyzing larger datasets.

## Visual Learning Aids

```
# How Python Processes Code
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ You write   │     │ Python      │     │ Output      │
│ code        │ ──> │ interprets  │ ──> │ appears     │
│             │     │ code        │     │             │
└─────────────┘     └─────────────┘     └─────────────┘
```

```
# Working with an AI Assistant
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│ You ask     │     │ AI generates│     │ You run     │
│ AI for help │ ──> │ code or     │ ──> │ and modify  │
│             │     │ explanation │     │ the code    │
└─────────────┘     └─────────────┘     └─────────────┘
```

```
# Variables Store Data
name = "Alex"  ┌─────────┐
               │  Alex   │ <- Value
               └─────────┘
                   ▲
                   │
                  name    <- Variable name
```

## Additional Resources
- [Python Official Documentation](https://docs.python.org/3/)
- [Google Colab Tutorial](https://colab.research.google.com/notebooks/intro.ipynb)
- [W3Schools Python Tutorial](https://www.w3schools.com/python/)
- [Real Python - Python Basics](https://realpython.com/python-basics/)