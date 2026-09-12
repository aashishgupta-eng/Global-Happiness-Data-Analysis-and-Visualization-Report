# Global Happiness Data Analysis

## Project Overview

The **Global Happiness Data Analysis** project is a Python-based data analysis and visualization project.

The main purpose of this project is to analyze the **Happiness Scores of different countries** and identify countries with the highest average Happiness Scores.

The project uses **Pandas, NumPy, Matplotlib, and Seaborn** for data loading, cleaning, analysis, and visualization.

Different visualization techniques are used to make the analysis easier to understand, including:

* Bar Chart
* Horizontal Bar Chart
* Pie Chart
* Line Chart
* Scatter Plot
* Combined Dashboard

---

## Objectives

The main objectives of this project are:

1. Analyze the Global Happiness dataset.
2. Understand the structure and information present in the dataset.
3. Check missing values and duplicate records.
4. Analyze Happiness Scores country-wise.
5. Find the top 10 happiest countries.
6. Compare Happiness Scores between different countries.
7. Create different visualizations for better understanding.
8. Present the analysis through a combined dashboard.

---

## Technologies Used

The project is developed using Python and the following libraries:

* **Python**
* **Pandas** – Data loading, cleaning, grouping, and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical data visualization
* **Jupyter Notebook** – Development and analysis environment

---

## Dataset

The project uses the **Global Happiness Report dataset**.

The dataset contains country-wise information related to **Happiness Scores**.

The Happiness Score is used to compare the happiness levels of different countries.

---

## Data Analysis

The following data analysis operations are performed:

### Dataset Overview

The dataset is examined using:

```python
confirmed_df.shape
confirmed_df.info()
confirmed_df.describe()
confirmed_df.columns
```

These operations help understand:

* Number of rows and columns
* Data types
* Statistical information
* Column names

### Data Cleaning

The project checks for missing values and duplicate records:

```python
confirmed_df.isnull().sum()
confirmed_df.duplicated().sum()
```

Column names are also renamed for easier use:

```python
confirmed_df.rename(columns={
    'Province/State': 'province',
    'Country/Region': 'Country'
}, inplace=True)
```

---

## Exploratory Data Analysis

The project performs Exploratory Data Analysis (EDA) to understand the Happiness Scores.

Some of the analysis includes:

* Number of unique Happiness Scores
* Total Happiness Score
* Maximum Happiness Score
* Minimum Happiness Score
* Country with the highest Happiness Score
* Country with the lowest Happiness Score
* Country-wise Happiness Score
* Top 10 happiest countries

Example:

```python
happiness_score = confirmed_df.groupby('Country')['Happiness_Score'].sum()

happiness_score.sort_values(
    ascending=False
).head(10)
```

---

## Countries Analyzed

The project also checks Happiness Scores for selected countries, including:

* India
* United States
* Ireland
* China

---

## Data Visualization

### 1. Horizontal Bar Chart

The horizontal bar chart displays the **Top 10 Happiest Countries** based on their average Happiness Score.

This visualization makes it easy to compare the Happiness Scores of different countries.

Finland appears with the highest average Happiness Score among the selected countries.

---

### 2. Pie Chart

The pie chart displays the percentage share of the average Happiness Score among the **Top 5 Happiest Countries**.

The chart highlights the contribution of each country to the total score of the selected countries.

---

### 3. Line Chart

A line-based visualization is used to display the average Happiness Score of the **Top 10 Happiest Countries**.

Each point represents the average Happiness Score of a country.

---

### 4. Bar Chart

A vertical bar chart is used to compare the average Happiness Scores of the top 10 countries.

The values are also displayed above the bars for easier comparison.

---

### 5. Scatter Plot

The scatter plot displays the average Happiness Score of the top 10 happiest countries.

Each point represents one country and its corresponding average Happiness Score.

---

## Dashboard

The project also contains a **Combined Visualization Dashboard**.

The dashboard combines multiple visualizations in a single view to provide a quick overview of the Happiness Scores.

It helps in:

* Comparing countries
* Understanding rankings
* Observing score differences
* Viewing the top happiest countries
* Understanding the distribution of Happiness Scores

---

## Project Structure

```text
Global-Happiness-Data-Analysis/
│
├── Global Happiness Data Analysis.ipynb
│
├── global_happiness_report_analysis_200k.csv
│
└── README.md
```

---

## How to Run the Project

### Step 1: Install Python

Make sure Python is installed on your system.

### Step 2: Install Required Libraries

Open Command Prompt or Terminal and run:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Step 3: Open Jupyter Notebook

Run:

```bash
jupyter notebook
```

### Step 4: Open the Notebook

Open:

```text
Global Happiness Data Analysis.ipynb
```

### Step 5: Load the Dataset

Make sure the dataset file is available and update the CSV file path if required.

Example:

```python
confirmed_df = pd.read_csv("global_happiness_report_analysis_200k.csv")
```

### Step 6: Run the Cells

Run the notebook cells from top to bottom to perform the complete analysis and generate the visualizations.

---

## Key Findings

The analysis identifies the countries with the highest average Happiness Scores.

Based on the analysis in the notebook:

1. **Finland** has the highest average Happiness Score among the selected top countries.
2. **Denmark** is among the top happiest countries.
3. **Iceland** is also among the top countries.
4. **Norway** appears among the highest-scoring countries.
5. **Switzerland** is included in the top 5 countries.
6. The differences between the Hap
