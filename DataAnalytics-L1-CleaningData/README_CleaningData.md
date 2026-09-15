# Data Cleaning — Student Performance Dataset

**Track:** Data Analytics (Oasis Infobyte SIP)
**Level:** Level 1 — Task 3 (Cleaning Data)
**Author:** Minhaj Uddin Farhad

## Objective

Take a deliberately messy dataset and systematically transform it into a clean, analysis-ready dataset, documenting every cleaning decision.

## Dataset

`bi.csv` — 77 rows, 11 columns. Student records including name, age, gender, country, residence type, previous education, entry exam score, study hours, and Python/DB scores.

## Tools Used

- Python
- pandas
- numpy
- Jupyter Notebook (Google Colab)

## Cleaning Steps Performed

1. **Data Quality Report** — nulls, duplicates, dtypes, and inconsistent-value counts before any cleaning
2. **Missing Data Handling** — 2 missing `Python` scores imputed with the column median
3. **Duplicate Removal** — checked and confirmed 0 duplicate rows
4. **Standardization**:
   - `gender`: 6 inconsistent variants → 2 (`Male`, `Female`)
   - `country`: 16 variants → 13 (case fixes + merging synonyms like `Rsa` → `South Africa`)
   - `residence`: 6 variants → 3 (merged differently-punctuated "BI Residence" labels)
   - `prevEducation`: 10 variants → 5 (case fixes + typo corrections)
5. **Outlier Detection** — IQR method applied to Age, entryEXAM, studyHOURS, Python, DB; all flagged values were retained as legitimate data (not data-entry errors)
6. **Data Type Correction** — confirmed all columns have correct dtypes
7. **Before/After Summary Table** — side-by-side comparison of data quality metrics
8. **Saved cleaned dataset** as `bi_cleaned.csv`

## Files in This Folder

- `Cleaning_Data.ipynb` — full cleaning notebook
- `bi.csv` — original raw dataset
- `bi_cleaned.csv` — cleaned output dataset
- `screenshots/` — output screenshots
- `README.md` — this file

## How to Run

1. Open `Cleaning_Data.ipynb` in Jupyter Notebook or Google Colab.
2. Upload `bi.csv` when prompted (or place it in the same directory).
3. Run all cells in order. The cleaned file `bi_cleaned.csv` will be generated automatically.
