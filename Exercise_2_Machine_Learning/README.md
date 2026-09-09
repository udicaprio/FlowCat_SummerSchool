# Exercise 2 — Machine Learning for Carbon-Capture Process Design

This hands-on exercise introduces an end-to-end machine-learning workflow for a process-intensification problem. You will train a data-driven surrogate model for a packed carbon-capture column, evaluate its predictions on unseen data, and combine it with differential evolution to optimize operating conditions.

The workbook follows a step-by-step structure and can be used during a taught session or for independent study in Google Colab.

## Learning objectives

After completing this exercise, you will be able to:

- **Formulate** a supervised regression problem by separating process inputs from model outputs.
- **Inspect** a process dataset and **examine** the ranges and distributions of its variables.
- **Partition** data into training and test sets while explaining the role of unseen test data.
- **Apply** scaling without using information from the test set during model training.
- **Construct** and train a reproducible multi-output neural-network regression model with Keras.
- **Calculate** and **interpret** the coefficient of determination and root mean squared error for each predicted output.
- **Apply** differential evolution to optimize operating conditions within bounds represented by the training data.
- **Evaluate** an optimized condition using physical limits and process-engineering considerations.
- **Optionally compare** the neural network with a linear-regression baseline using numerical metrics.

## Before you begin

1. Download this repository to your computer.
2. Open [Google Colab](https://colab.research.google.com/).
3. Upload `Exercise_2_Workbook.ipynb` to Colab.
4. In the Colab **Files** panel, upload `carbon_capture_data.csv`.

No local Python installation is required. The notebook uses NumPy, pandas, Matplotlib, SciPy, scikit-learn, TensorFlow, and Keras.

## How to use the workbook

Work through the notebook from top to bottom. Most of the code is already provided so that you can focus on the main decisions in the machine-learning workflow. During a taught session, add the requested lines as each concept is introduced. When studying independently, attempt each marked task before consulting the solution.

Incomplete code uses the following format:

```python
#TO DO
#Use df to select the columns listed in feature_names and store them in X
#X = ...
```

Uncomment the indicated line and replace `...` when it is present. The surrounding completed code shows how the new line fits into the workflow. Run each completed cell before moving to the next one because later cells use variables created earlier.

Each task is accompanied by a **Suggestion** menu. The menus are closed by default so that you can first attempt the task yourself. If you need support, click the menu to reveal a short approach and one possible code solution.

The final linear-regression baseline and model comparison are optional. They can be completed after the main Keras workflow if time permits or used as an extension for independent study.

## Process variables

| Column | Meaning | Unit |
|---|---|---|
| `GFR` | Gas flow rate per column area | m³/(m²·h) |
| `LFR` | Liquid flow rate per column area | L/(m²·h) |
| `Temp` | Operating temperature | °C |
| `CO2alpha` | Initial CO₂ loading in the liquid | mol CO₂/mol amine |
| `CO2pp` | CO₂ partial pressure | kPa |
| `Height` | Packed-column height | m |
| `kGa` | Volumetric mass-transfer coefficient | Dataset units |
| `eta` | CO₂ capture efficiency | Fraction |

The six operating and design variables are the model inputs. The mass-transfer coefficient and capture efficiency are the two model outputs.

## Files in this folder

- `Exercise_2_Workbook.ipynb`: the notebook containing explanations and incomplete coding steps.
- `carbon_capture_data.csv`: the dataset that must be uploaded to the Colab session.
- `Exercise_2_Solution.ipynb`: the completed notebook for checking your work after attempting each step.
- `neural_network_architecture.svg`: represenation of the neural network used in the exercise.

## About the dataset

The dataset contains synthetic, in-silico observations created for teaching. Its values illustrate plausible relationships between column conditions and carbon-capture performance, but they do not represent experimental validation of a particular process.

Do not use the data or resulting models for research conclusions, equipment design, safety decisions, or commercial applications.
