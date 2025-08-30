# HR Data Cleaning & Analysis

## 📌 Project Overview

Messy HR data is one of the biggest challenges in workforce analytics. This project provides a **reproducible pipeline** for cleaning, validating, and preparing HR datasets for further analysis or machine learning.

The notebook demonstrates how to:

* Fix corrupted encodings (like `+AC0-` → `-`)
* Standardize inconsistent date formats
* Remove duplicate or invalid rows
* Convert categorical fields into consistent formats
* Compute employee tenure and other derived fields

---

## 🗂️ File Structure

```
├── employee_data.csv              # Raw messy HR dataset
├── cleaned_hr_data.csv            # Cleaned, analysis-ready dataset
├── HR_Data_Cleanup.ipynb          # Main Jupyter Notebook pipeline
├── HR_Data_Cleaning_Project_Presentation.pdf # Summary slides
└── README.md                      # Documentation (this file)
```

---

## 🚀 Features

✅ Handles corrupted encodings and messy text
✅ Cleans inconsistent HR fields (names, departments, salaries)
✅ Standardizes dates across formats
✅ Calculates derived HR metrics like employee tenure
✅ **Supports CSV, Excel, and JSON input**
✅ Extensible for new HR datasets

---

## 🔧 Usage

### 1. Install Requirements

```bash
pip install pandas openpyxl
```

### 2. Run the Notebook

Open `HR_Data_Cleanup.ipynb` in Jupyter or VSCode and execute step by step.

### 3. Using the Loader Function

```python
from hr_loader import load_hr_data

df = load_hr_data("employee_data.csv")   # CSV
df = load_hr_data("employee_data.xlsx")  # Excel
df = load_hr_data("employee_data.json")  # JSON
```

---

## 📊 Example Output

Before Cleaning:

| Name      | DOJ        | Dept         | Salary   |
| --------- | ---------- | ------------ | -------- |
| Jhn Doe   | 12/31/2022 | HR           | 50,000\$ |
| +AC0-Mary | 31-12-22   | human resrcs | 5O,OO0   |

After Cleaning:

| Name     | DOJ        | Dept | Salary |
| -------- | ---------- | ---- | ------ |
| John Doe | 2022-12-31 | HR   | 50000  |
| Mary     | 2022-12-31 | HR   | 50000  |

---

## 🏗️ Next Steps

* Add **unit tests** for validation (pytest)
* Integrate **GitHub Actions** for CI/CD
* Expand pipeline to support **SQL database ingestion**
* Build a **Streamlit dashboard** for visualization

---

## 📜 License

MIT License – free to use, modify, and distribute.
