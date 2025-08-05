# hr-cleaner

A simple but complete data cleaning pipeline for raw HR employee data.  
This project converts broken, inconsistent employee records into a clean dataset ready for analysis or dashboards.

# What’s Inside

This project:
- Handles corrupted encodings like `+AC0-` in date columns
- Parses weird date formats into clean ISO `YYYY-MM-DD` style
- Drops incomplete or garbage rows
- Converts categorical values and coerces numeric types
- Adds new field: `TenureYears` calculated from `StartDate`

All of this is done using pure Python with Pandas — fast, reproducible and robust.

---

# Files

| File | Purpose |
|------|---------|
| `employee_data.csv` | Raw HR dataset with encoding issues |
| `cleaned_hr_data_for_powerbi.csv` | Cleaned dataset – ready for BI or modeling |
| `hr_cleaning.ipynb` | Full cleaning pipeline code (load → fix → export) |
| `HR_Data_Cleaning_Project_Presentation.pptx` | Project summary slides |
| `README.md` | This file – project documentation |

---

# Tech Used

- Python (Pandas, Regex, Datetime)
- Jupyter Notebook for development
- `.pptx` auto-generated using `python-pptx`

---

# Final Words

The raw HR data was a mess.  
We’re talking:
- Garbled character encodings
- Mixed types
- Invalid dates
- Missing critical fields

Now it’s a clean, analysis-ready CSV that can be thrown straight into Power BI, Excel, or ML models.

The script is reusable — just replace the CSV and run the notebook.

---

