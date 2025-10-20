# Task 1: Data Cleaning and Preprocessing for Netflix Dataset

## Objective
[cite_start]The goal of this task was to clean and prepare a raw dataset of Netflix movies and TV shows to make it suitable for analysis[cite: 5]. [cite_start]The process involved identifying and fixing common data quality issues like inconsistent data types and non-standard column names[cite: 20].

## Dataset
- [cite_start] Source: Netflix Movies and TV Shows [cite: 17]
- Format: The initial data was provided in an `.xlsx` file.

## Tools Used
- Language: Python
- [cite_start] Library: Pandas [cite: 5]

## Process

### 1. Initial Data Analysis & Examination
The first step was to load the dataset and perform an initial exploratory analysis.
- The dataset was loaded using the Pandas library.
- [cite_start]`.info()` was used to get a summary of the data, including column data types and null value counts[cite: 8].
- [cite_start]`.duplicated().sum()` was used to check for any duplicate rows[cite: 9].

**Findings from this step:**
- The dataset contained "no duplicate rows".
- Initially, there appeared to be no "missing values".
- [cite_start]The `date_added` column was incorrectly typed as `object` (text) instead of a date format[cite: 12].

### 2. Data Cleaning and Formatting
Based on the analysis, the following cleaning actions were performed:
- Corrected Data Types: The `date_added` column was converted to a proper `datetime` format. [cite_start]During this conversion, some entries with unrecognized date formats were automatically converted to `NaT` (Not a Time), which are pandas' standard null value for datetime objects[cite: 10, 12].
- [cite_start] Standardized Column Headers: All column names were converted to lowercase, and spaces were replaced with underscores for consistency and easier access in code (e.g., `release year` became `release_year`)[cite: 11].

## Final Outcome
[cite_start]The result is a clean and structured dataset (`netflix_cleaned.csv`) that is ready for further analysis, visualization, or modeling[cite: 24]. All relevant data types are corrected, and the column headers are standardized.

## Files in this Repository
1.  `output_adjusted.xlsx`: The original, raw dataset.
2.  [cite_start]`netflix_cleaned.csv`: The final, cleaned dataset ready for analysis[cite: 6].
3.  `step1_analysis.py`: Python script used for the initial data examination.
4.  `step2_cleaning.py`: Python script used to perform the cleaning and formatting tasks.
5.  [cite_start]`README.md`: This summary file explaining the project[cite: 46].