# 💎 Diamonds Data Analysis using Python

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on a Diamonds dataset using Python.

The main objective is to understand the structure and characteristics of diamond data, analyze different diamond attributes, identify distributions, and explore relationships between variables such as **carat, price, depth, cut, color, clarity, and dimensions**.

The analysis is performed using **Pandas, NumPy, and Matplotlib** in a Jupyter Notebook.

---

## 🎯 Objectives

The project focuses on:

- Understanding the structure of the Diamonds dataset
- Inspecting rows, columns, data types, and statistical summaries
- Checking the dataset for data-quality issues
- Removing unnecessary columns
- Analyzing categorical variables
- Studying diamond price distribution
- Exploring the relationship between carat and price
- Exploring the relationship between depth and price
- Analyzing diamond cut distribution
- Visualizing diamond dimensions
- Identifying invalid dimensional values such as zero values

---

## 🗂️ Dataset

The project uses a **Diamonds dataset** containing information about diamonds and their physical and quality characteristics.

Important columns used in the analysis include:

| Column | Description |
|---|---|
| `carat` | Weight of the diamond |
| `cut` | Quality of the diamond cut |
| `color` | Diamond color grade |
| `clarity` | Diamond clarity grade |
| `depth` | Total depth percentage |
| `table` | Width of the top of the diamond relative to its widest point |
| `price` | Price of the diamond in USD |
| `x` | Length in mm |
| `y` | Width in mm |
| `z` | Depth in mm |

---

## 🛠️ Technologies & Libraries

- 🐍 Python
- 🐼 Pandas
- 🔢 NumPy
- 📊 Matplotlib
- 📓 Jupyter Notebook

---

## 🔍 Analysis Performed

### 1. Dataset Inspection

The notebook uses:

```python
df.head()
df.tail()
df.shape
df.columns
df.info()
df.dtypes
df.describe()
```

These commands are used to understand the dataset's structure, dimensions, columns, data types, and statistical characteristics.

---

### 2. Data Cleaning

An unnecessary `Unnamed: 0` column was removed:

```python
df1 = df.drop(columns='Unnamed: 0')
```

The analysis also identifies records where diamond dimensions contain zero values:

```python
df.loc[(df['x'] == 0) | (df['y'] == 0) | (df['z'] == 0)]
```

These records are removed before further analysis.

---

### 3. Categorical Analysis

Frequency distributions were calculated for:

- Carat
- Cut
- Color
- Clarity
- Table
- Price

For example:

```python
df1['cut'].value_counts()
```

This helps understand how frequently different diamond quality categories occur.

---

## 📊 Visualizations

### 💰 Diamond Price Distribution

A histogram is used to analyze the distribution of diamond prices.

```python
plt.hist(df1["price"], bins=200)
```

This helps identify the concentration and spread of diamond prices.

---

### 💎 Carat vs Price

A plot is created to investigate the relationship between diamond weight and price.

```python
plt.plot(df1['price'], df1['carat'])
```

This provides a visual comparison between **diamond carat and price**.

---

### 📐 Depth vs Price

The notebook examines the relationship between diamond depth and price.

```python
plt.plot(df1['price'], df1['depth'])
```

---

### ✨ Diamond Cut Distribution

The distribution of diamond cuts is visualized using:

- Bar chart
- Pie chart

```python
cut_count.plot(kind='bar')
```

and

```python
cut_count.plot(kind='pie')
```

These visualizations show how the different cut categories are distributed within the dataset.

---

### 📏 Diamond Dimensions

A scatter plot is used to explore the relationship between the `x` and `y` dimensions:

```python
plt.scatter(df1['x'], df1['y'])
```

---

## 📈 Key Analysis Areas

The notebook explores the following relationships and distributions:

```text
Diamond Data
     │
     ├── Data Inspection
     │
     ├── Data Cleaning
     │
     ├── Carat Analysis
     │
     ├── Cut Analysis
     │
     ├── Color Analysis
     │
     ├── Clarity Analysis
     │
     ├── Price Analysis
     │
     ├── Depth Analysis
     │
     └── Dimension Analysis
          ├── X
          ├── Y
          └── Z
```

---

## 📁 Project Structure

```text
Diamonds-Data-Analysis/
│
├── diamonds.csv
├── lecture_22_08_26.ipynb
└── README.md
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/harshsevkani/<repository-name>.git
```

### 2. Open the project

Open the notebook using Jupyter Notebook or JupyterLab.

```bash
jupyter notebook
```

### 3. Run the notebook

Open:

```text
lecture_22_08_26.ipynb
```

and execute the cells sequentially.

---

## 💡 Skills Demonstrated

This project demonstrates practical experience with:

- Python programming
- Pandas DataFrame operations
- NumPy
- Data inspection
- Data cleaning
- Missing/data-quality checking
- Descriptive statistics
- Frequency analysis
- Categorical data analysis
- Data visualization
- Exploratory Data Analysis (EDA)
- Jupyter Notebook

---

## 🔮 Future Improvements

The project can be extended by adding:

- Correlation analysis
- Seaborn visualizations
- Box plots for outlier detection
- Scatter plots with better trend analysis
- Price analysis by cut, color, and clarity
- GroupBy-based business insights
- Statistical analysis
- Interactive Power BI dashboard
- Machine Learning models for diamond price prediction

---

## 👨‍💻 Author

**Harsh Sevkani**

🎓 BCA | Pursuing MCA at GLS University

🔗 LinkedIn:  
https://www.linkedin.com/in/harsh-sevkani-717612285/

💻 GitHub:  
https://github.com/harshsevkani

---

## ⭐ Conclusion

This project demonstrates the use of Python-based data analysis techniques to explore and visualize a Diamonds dataset. It provides hands-on practice with **data cleaning, statistical exploration, categorical analysis, and visualization**, forming a strong foundation for further work in **Data Analytics and Data Science**.
