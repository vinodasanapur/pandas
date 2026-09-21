# Notebook Summary
* **Library Loaded:** Pandas (`import pandas as pd`)[cite: 3]
* **Dataset Loaded:** `matches.csv` stored into a DataFrame `df`[cite: 3]
* **Dataset Size:** 
  * **Initial:** 1,095 rows and 20 columns[cite: 3]
  * **After Data Cleaning:** 1,028 rows and 19 columns[cite: 3]

---

### Data Cleaning & Analysis Steps Performed
1. **Inspecting Data:**
   * Used `.head()` to view the top 5 rows[cite: 3]
   * Used `.tail()` to view the bottom rows (up to 10 rows)[cite: 3]
   * Used `.columns`, `.shape`, `len()`, and `.info()` to check structure and data types[cite: 3]
2. **Duplicates & Null Values:**
   * Checked for duplicates using `.duplicated().sum()` (found `0` duplicates)[cite: 3]
   * Checked null values using `.isnull().sum()`[cite: 3]. The `method` column had 1,074 missing values, while `city` had 51 missing values[cite: 3]
   * Dropped the heavily missing `method` column using `df.drop(columns="method", inplace=True)`[cite: 3]
   * Dropped remaining rows containing null values using `df.dropna(inplace=True)`[cite: 3]
3. **Column Selection & Summary Statistics:**
   * Selected single and multiple columns (e.g., `df[['toss_decision', 'winner', 'city']]`)[cite: 3]
   * Generated summary statistics for numerical columns (`result_margin`, `target_runs`, `target_overs`) using `.describe()`[cite: 3]
