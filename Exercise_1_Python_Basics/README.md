# Exercise 1 — Python Basics for Process Intensification

This hands-on exercise introduces the Python tools used for process-intensification data analysis. The workbook follows a step-by-step structure and can be used during a taught session or for independent study in Google Colab.

You will use a small process-intensification example to become familiar with:

1. Python variables, calculations, conditional statements, lists, loops, and functions;
2. NumPy arrays and descriptive statistics;
3. pandas data loading, inspection, selection, and filtering;
4. Matplotlib plots for engineering data.

## Learning objectives

After completing this exercise, you will be able to:

- **Identify** variables, strings, lists, NumPy arrays, and pandas DataFrames in Python code.
- **Explain** the purpose of NumPy, pandas, and Matplotlib in a data-analysis workflow.
- **Apply** Python syntax to define variables, perform calculations, use conditional statements, and repeat calculations with a loop.
- **Construct** and call simple functions that accept arguments and return calculated values.
- **Construct** NumPy arrays and **calculate** descriptive statistics from process data.
- **Use** pandas to load the provided CSV file and to select and filter observations.
- **Plot** process variables with appropriate labels, units, titles, and legends.
- **Compare** conventional and intensified reactor data and **examine** the relationship between conversion, residence time, and energy demand.

## Before you begin

1. Download this repository to your computer.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload `Exercise_1_Workbook.ipynb` to Colab.
4. In the Colab **Files** panel, upload `process_intensification_data.csv`.

No local Python installation is required. NumPy, pandas, and Matplotlib are already available in Google Colab.

## How to use the workbook

Work through the notebook from top to bottom. During a taught session, complete each step as it is introduced. When studying independently, read the explanation above each code cell and attempt the step before consulting the solution. You will complete code marked with comments such as:

```python
#TO DO
#Generate a list with residence times 3.2, 4, and 6 minutes
#residence_times_min = ...
```

Uncomment the incomplete line and replace `...` with the required code. Run each completed cell before moving to the next one because later cells use variables created earlier.

## Files in this folder

- `Exercise_1_Workbook.ipynb`: the notebook containing the explanations and incomplete coding steps.
- `process_intensification_data.csv`: the dataset you must upload to the Colab session.
- `Exercise_1_Solution.ipynb`: the completed notebook for checking your work after attempting each step.

## About the dataset

The dataset is synthetic and was created only for this exercise. Its values illustrate plausible process trends but do not represent a particular experimental system. Do not use these data for research, process design, safety decisions, or commercial applications.
