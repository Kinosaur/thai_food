# Thai Food Dataset Analysis & Preprocessing

## Project Overview

This project explores a Thai food dataset through data cleaning, preprocessing, and exploratory analysis. It is designed as a data analytics / data science portfolio project that demonstrates how raw food records can be transformed into a cleaner dataset for ingredient analysis, cuisine exploration, recommendation ideas, and dashboard/reporting practice.

The project includes raw CSV data, cleaned dataset versions, Jupyter notebooks for preprocessing and analysis, and a workflow that can be extended into Power BI reporting.

## Dataset

The dataset contains Thai dishes with English names, Thai names, ingredients, course type, province, and region information. The final cleaned dataset contains 324 dish records.

| File | Description |
| --- | --- |
| `data/raw/thailand_foods.csv` | Raw dataset with 325 rows and 6 columns: `en_name`, `th_name`, `ingredients`, `course`, `province`, and `region`. Some values are listed as `Unknown`. |
| `data/processed/thai_dish.csv` | Intermediate preprocessing file with 325 rows. It removes the Thai-name column and keeps `en_name`, `ingredients`, `course`, `province`, and `region`. |
| `data/processed/thai_dish_filled_complete.csv` | Cleaned dataset with 324 rows and 6 columns. Unknown ingredient, province, and region values were filled where possible, and a duplicate created during preprocessing was removed. |
| `data/processed/thai_dish_filled_complete_analysis_copy.csv` | Preserved analysis copy of the completed cleaned dataset. This copy was kept so no files were overwritten during project reorganization. |

## Cleaning and Preprocessing

The preprocessing notebook reviews the raw data shape, sample rows, missing-like values, course counts, and duplicate rows. The cleaning workflow includes:

- Loading the raw CSV with Pandas.
- Creating an intermediate dish dataset.
- Checking course distribution across main dishes, desserts, snacks, salads, and soup.
- Identifying duplicate rows after preprocessing.
- Filling `Unknown` ingredient values with dish-specific ingredient text.
- Filling `Unknown` province and region values where possible.
- Saving the completed cleaned dataset as `thai_dish_filled_complete.csv`.

The completed dataset has no blank values or `Unknown` values in the checked columns. Some province and region values remain labeled as `Various`, which means the geographic origin is broad or not specific to one province.

## Analysis Goals

The analysis notebook focuses on practical exploratory analysis questions:

- Look up a Thai dish by name and return its region and ingredients.
- Identify the most common ingredients across dishes.
- Count dishes by region and province.
- Compare dish counts by course type.
- Create basic charts with Matplotlib and Seaborn.

## Tools Used

- Python
- Pandas
- Jupyter Notebook
- Matplotlib and Seaborn
- Power BI for dashboard and reporting practice

## Project Structure

```text
thai_food/
├── data/
│   ├── raw/
│   │   └── thailand_foods.csv
│   └── processed/
│       ├── thai_dish.csv
│       ├── thai_dish_filled_complete.csv
│       └── thai_dish_filled_complete_analysis_copy.csv
├── notebooks/
│   ├── dataCleaning.ipynb
│   └── fullAnalysis.ipynb
├── dashboard/
├── README.md
└── KAGGLE_DATASET_DESCRIPTION.md
```

Checkpoint folders, virtual document folders, Anaconda metadata, and temporary files are not part of the main project workflow. No Power BI `.pbix` file was present in the scanned project tree; the `dashboard/` folder is ready for one if added later.

## How to Run the Notebooks

1. Clone or download this repository.
2. Install the main Python packages:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Open Jupyter Notebook or JupyterLab:

```bash
jupyter notebook
```

4. Run the notebooks in this order:

- `notebooks/dataCleaning.ipynb`
- `notebooks/fullAnalysis.ipynb`

The cleaned dataset is stored at `data/processed/thai_dish_filled_complete.csv`. If rerunning notebook cells after this folder reorganization, use the updated CSV paths under `data/raw/` and `data/processed/`.

## Key Features

- End-to-end data preprocessing workflow from raw CSV to cleaned dataset.
- Ingredient-level exploration using string splitting and frequency counts.
- Regional and province-level dish distribution analysis.
- Course type analysis for main dishes, desserts, snacks, salads, and soup.
- Simple food lookup function for retrieving dish details by name.
- Dataset structure that can support future dashboarding or recommendation-system experiments.

## Possible Use Cases

- Thai food recommendation based on ingredients, course, or region.
- Cuisine analysis by region or province.
- Ingredient frequency and ingredient-pattern analysis.
- Food category exploration using the `course` column.
- Dashboard and reporting practice in Power BI.
- This project can be extended to nutrition analysis if nutrition fields are added later.

## Portfolio Skills Demonstrated

This project demonstrates practical data analyst and data science internship skills, including:

- Reading and inspecting raw CSV datasets.
- Cleaning categorical and text-based data with Pandas.
- Handling unknown values carefully.
- Creating reproducible notebook workflows.
- Performing exploratory data analysis.
- Building simple visualizations for categorical data.
- Preparing cleaned datasets for reporting, dashboards, and future modeling.

## What I Learned

- How to inspect a raw dataset and identify columns that need cleaning.
- How duplicate rows can appear after dropping or changing columns.
- How to replace unknown ingredient and location values in a controlled way.
- How ingredient strings can be transformed into analyzable lists.
- How regional and course-level summaries can help explain a cuisine dataset.

## Future Improvements

- Add clear source documentation for each dish and ingredient update.
- Standardize region labels such as `North` / `Northern` and `South` / `Southern`.
- Replace broad `Various` province and region values with more specific labels where reliable sources are available.
- Normalize ingredients into a separate ingredient table for deeper analysis.
- Add nutrition fields such as calories, protein, fat, carbohydrates, or allergens if reliable data is available.
- Build a Power BI dashboard for course distribution, ingredient frequency, and regional cuisine exploration.
- Develop a simple recommendation system using ingredients, region, and course type.
