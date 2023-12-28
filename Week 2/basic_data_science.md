# Basic Data Science Workflow

Data Science combines domain expertise, programming skills, and knowledge of mathematics and statistics to extract meaningful insights from data. This workflow typically involves three key steps: Data Collection, Data Cleaning, and Data Wrangling, each detailed below with examples.

## 1. Data Collection

Data collection is the first step, involving gathering data from various sources like databases, files, external APIs, or web scraping.

### Techniques and Example
- **APIs**: Gathering data from services.
- **Web Scraping**: Extracting data from web pages.
- **Databases**: Retrieving data from SQL or NoSQL databases.
- **Excels, CSVs, jsons**: Retrieving data spreadsheets, csvs and jsons.

```python
import requests
response = requests.get('https://api.example.com/data')
data = response.json()
# Assuming response.json() returns [{'value': 1}, {'value': 2}]
```


```python
import pandas as pd

# Reading data from an Excel file
excel_data = pd.read_excel('path/to/your/excelfile.xlsx')
excel_data.head()

# Reading data from an Excel file
csv_data = pd.read_csv('path/to/your/excelfile.csv')
csv_data.head()

# Reading data from a JSON file
json_data = pd.read_json('path/to/your/datafile.json')
json_data.head()
```

## 2. Data Cleaning

Data cleaning transforms raw data into a format suitable for analysis.

### Techniques
- **Handling Missing Values**: Impute or remove missing values.
- **Filtering Outliers**: Identify and handle outliers.
- **Data Formatting**: Standardize data formats.

#### Example: Handling Missing Values

```python
import pandas as pd
df = pd.DataFrame({'A': [1, 2, None, 4], 'B': [None, 2, 3, 4]})
print("Before Cleaning:\n", df)
df.fillna(method='bfill', inplace=True)
print("\nAfter Cleaning:\n", df)
```

**Before Cleaning:**

|   A   |   B   |
|:-----:|:-----:|
|   1   |  NaN  |
|   2   |   2   |
|  NaN  |   3   |
|   4   |   4   |

**After Cleaning (Backfill):**

|   A   |   B   |
|:-----:|:-----:|
|   1   |   2   |
|   2   |   2   |
|   4   |   3   |
|   4   |   4   |

## 3. Data Wrangling

Data wrangling transforms and maps raw data into a more suitable format for analysis.

### Techniques
- **Merging Data**: Combining data from different sources.
- **Data Transformation**: Changing the shape or structure of data.
- **Data Aggregation**: Summarizing data.

#### Example: Merging Data

```python
df1 = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
df2 = pd.DataFrame({'C': [7, 8, 9], 'D': [10, 11, 12]})
print("DataFrame 1:\n", df1)
print("\nDataFrame 2:\n", df2)

merged_df = pd.concat([df1, df2], axis=1)
print("\nAfter Merging:\n", merged_df)
```

**DataFrame 1:**

|   A   |   B   |
|:-----:|:-----:|
|   1   |   4   |
|   2   |   5   |
|   3   |   6   |

**DataFrame 2:**

|   C   |   D   |
|:-----:|:-----:|
|   7   |  10   |
|   8   |  11   |
|   9   |  12   |

**After Merging:**

|   A   |   B   |   C   |   D   |
|:-----:|:-----:|:-----:|:-----:|
|   1   |   4   |   7   |  10   |
|   2   |   5   |   8   |  11   |
|   3   |   6   |   9   |  12   |

## Conclusion

Mastering Data Collection, Cleaning, and Wrangling is crucial in Data Science, paving the way for advanced analysis and machine learning tasks.

## Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Python for Data Analysis Book](https://bedford-computing.co.uk/learning/wp-content/uploads/2015/10/Python-for-Data-Analysis.pdf)
- [Kaggle's Data Cleaning Challenge](https://www.kaggle.com/learn/data-cleaning)
