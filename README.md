# data-cleaning

House Prices Data Cleaning & Missing Value Analysis

This project focuses on **Exploratory Data Analysis (EDA)** and **missing value handling** using the famous **House Prices: Advanced Regression Techniques** dataset from Kaggle.

The notebook demonstrates how to:
- Load and inspect real-world datasets
- Identify missing values
- Calculate missing value percentages
- Visualize missing data using heatmaps
- Clean unnecessary columns
- Prepare data for future Machine Learning tasks

---

# Project Overview

In this notebook, the dataset is analyzed step by step using:

- **Pandas** for data manipulation
- **NumPy** for numerical operations
- **Matplotlib** for plotting
- **Seaborn** for data visualization

The main focus of this lesson is understanding:
- Dataset structure
- Null values
- Data cleaning techniques
- Basic EDA workflow

---

# Technologies Used

```python
pandas
numpy
matplotlib
seaborn
opendatasets
```

---

# Dataset

Dataset used:
**House Prices: Advanced Regression Techniques**

Source:
Kaggle Competition Dataset

The dataset contains information about house features such as:
- Lot area
- Year built
- Garage information
- Basement details
- Sale price
- And many more property-related features

---

# Topics Covered

## 1. Dataset Loading

The dataset is downloaded using `opendatasets` and loaded into a Pandas DataFrame.

```python
df = pd.read_csv("train.csv")
```

---

## 2. Basic Dataset Inspection

The notebook explores:
- Dataset shape
- Data types
- Statistical summary
- General dataset information

Functions used:
```python
df.head()
df.info()
df.describe()
```

---

## 3. Missing Value Analysis

The notebook identifies columns with missing values using:

```python
df.isnull().sum()
```

Missing value percentages are also calculated:

```python
(df.isnull().sum()/len(df)*100).round(2)
```

---

## 4. Missing Data Visualization

A heatmap is created using Seaborn to visually inspect null values.

```python
sns.heatmap(df.isnull(), cbar=True, cmap="Reds")
```

This helps understand:
- Which columns contain missing data
- The density of missing values
- Overall dataset quality

---

## 5. Data Cleaning

Columns with excessive missing values are removed from the dataset.

Example:

```python
df.drop(['PoolQC', 'MiscFeature', 'Alley'], axis=1, inplace=True)
```

---

# Learning Outcomes

After completing this notebook, you will understand how to:
- Perform basic EDA
- Detect missing values
- Calculate null percentages
- Visualize missing data
- Clean datasets effectively
- Prepare data for Machine Learning workflows

---

# Project Structure

```bash
lesson6.ipynb
README.md
```

---

# Future Improvements

Possible next steps for this project:
- Feature engineering
- Handling categorical variables
- Data encoding
- Model training
- Regression analysis
- House price prediction

---

# Author
Zaxro Madrimova

Created as part of a Data Science / Machine Learning learning journey focused on:
- Python
- Data Analysis
- Visualization
- Machine Learning fundamentals
