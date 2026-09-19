# Veda-Technology-Task-12
# Task 12: Missing Value Identification

**Internship:** Veda Technology, Data Analytics Track
**Intern:** Akshat Srivastava

## About This Task

In this task I checked a dataset for missing values and summarized where they occur. This is a basic inspection step that should be done before cleaning or analyzing any data.

I used the **Titanic dataset** (891 rows, 12 columns). I picked it over Iris because Iris has no missing values, while Titanic has real missing data to practice on.

## Tools Used

- Google Colab
- Python
- Pandas
- Matplotlib

## Files in This Repository

| File | Description |
|------|-------------|
| `Task12_Missing_Values.ipynb` | Colab notebook with the code and summary |
| `titanic.csv` | Dataset used in this task |
| `missing_value_summary.csv` | Missing value summary saved from the notebook |
| `Task12_Missing_Value_Report.pdf` | Short report of the task |
| `README.md` | This file |

## How I Did It

1. Loaded the dataset with `pd.read_csv()` and checked its shape and first rows.
2. Used `df.info()` to see data types and non-null counts.
3. Counted the nulls in each column with `df.isnull().sum()` and calculated the percentage.
4. Kept only the columns that have missing values and sorted them from highest to lowest.
5. Plotted the percentages as a bar chart and saved the summary as a CSV file.

## Results

| Column | Missing Count | Missing % |
|--------|---------------|-----------|
| Cabin | 687 | 77.1% |
| Age | 177 | 19.87% |
| Embarked | 2 | 0.22% |

The other 9 columns have no missing values.

## Key Findings

- **Cabin** has the most missing values (about 77%). Most passengers have no cabin number recorded, so this column is not very useful as it is.
- **Age** has about 20% missing. This is a big gap, but age is important, so it can be filled later, for example with the median.
- **Embarked** has only 2 missing values, so its effect on the data is very small.

No values were removed or filled in this task, because the goal was only to identify the missing values. I will decide how to handle them in the next steps.



## Dataset Source

Titanic dataset from the [datasciencedojo/datasets](https://github.com/datasciencedojo/datasets) repository on GitHub.
