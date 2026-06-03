# Thai Food Dataset Analysis & Preprocessing

## Short Description

This dataset contains Thai food dish records with dish names, ingredients, course type, province, and region information. It is intended for educational use, data cleaning practice, exploratory analysis, and beginner-friendly analytics projects.

## Data Sources / Origin

This dataset is used for educational and analytics practice. The files in this project do not clearly document an official source, so the dataset should not be described as official unless the publisher verifies the original source before release.

## Files

| File | Rows | Description |
| --- | ---: | --- |
| `data/raw/thailand_foods.csv` | 325 | Raw dataset containing English dish names, Thai dish names, ingredients, course type, province, and region. |
| `data/processed/thai_dish.csv` | 325 | Intermediate preprocessing file without the `th_name` column. |
| `data/processed/thai_dish_filled_complete.csv` | 324 | Cleaned dataset with filled ingredient, province, and region values where possible. |
| `data/processed/thai_dish_filled_complete_analysis_copy.csv` | 324 | Preserved analysis copy of the cleaned dataset. |

## Column Descriptions

### `thailand_foods.csv`

| Column | Description |
| --- | --- |
| `en_name` | English or romanized Thai dish name. |
| `th_name` | Thai-language dish name. |
| `ingredients` | Main listed ingredients for the dish, generally separated by `+`. |
| `course` | Dish category such as `main dish`, `dessert`, `snack`, `salad`, or `soup`. |
| `province` | Province or broad province group associated with the dish. Some raw values are `Unknown` or `Various`. |
| `region` | Thai region or broad regional label associated with the dish. Some raw values are `Unknown` or `Various`. |

### `thai_dish.csv`

| Column | Description |
| --- | --- |
| `en_name` | English or romanized Thai dish name. |
| `ingredients` | Main listed ingredients for the dish. |
| `course` | Dish category. |
| `province` | Province or broad province group. |
| `region` | Thai region or broad regional label. |

### `thai_dish_filled_complete.csv`

| Column | Description |
| --- | --- |
| `en_name` | English or romanized Thai dish name. |
| `th_name` | Thai-language dish name. |
| `ingredients` | Completed ingredient list for the dish. The cleaned file has no `Unknown` ingredient values. |
| `course` | Dish category. |
| `province` | Province or broad province group. The cleaned file has no `Unknown` province values, but some rows remain labeled `Various`. |
| `region` | Thai region or broad regional label. The cleaned file has no `Unknown` region values, but some rows remain labeled `Various`. |

## Possible Use Cases

- Thai cuisine exploration.
- Ingredient frequency analysis.
- Regional food comparison.
- Course/category distribution analysis.
- Beginner data cleaning and preprocessing practice.
- Dashboard/reporting practice with tools such as Power BI.
- Simple food lookup or recommendation experiments.

This dataset can be extended to nutrition analysis if reliable nutrition columns are added.

## Suggested Analysis Questions

- Which ingredients appear most often across Thai dishes?
- Which regions have the most dish records in the dataset?
- How are dishes distributed across main dishes, desserts, snacks, salads, and soup?
- Which provinces appear most frequently?
- Which dishes contain a specific ingredient such as sugar, coconut milk, garlic, or fish sauce?
- How could dishes be recommended based on shared ingredients, course type, or region?

## How to Use This Dataset

```python
import pandas as pd

df = pd.read_csv("thai_dish_filled_complete.csv")
df.head()
```

## License

This dataset is shared for educational and data analytics practice purposes only.

Before using or redistributing this dataset, please verify the original data source and make sure you have permission to publish it publicly. If the data was collected from public websites or other third-party sources, users should respect the original source’s terms of use.

Recommended license for this dataset: **CC BY-NC-SA 4.0**

This means others may use, share, and adapt the dataset for non-commercial purposes, but they should give proper credit and share any adapted version under the same license.
