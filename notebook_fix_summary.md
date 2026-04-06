# Notebook Fix Summary

## Files returned
- `lecture_1_fixed.ipynb`
- `lecture_2_fixed.ipynb`
- `lecture_3_fixed.ipynb`
- `lecture_4_fixed.ipynb`
- `lecture_5_fixed.ipynb`

## What was fixed

### Lecture 1
- Added safer lookup for `chinook.db`.
- Validated that the notebook runs with the uploaded SQLite database.

### Lecture 2
- Added safer lookup for `chinook.db`.
- Validated that the JOIN examples run with the uploaded SQLite database.

### Lecture 3
- Fixed nullable `Int64` mean-fill example.
- Replaced broken references to missing columns like `price` in `retail_2016_2017.csv`.
- Replaced broken references to `dcoilwtico` with the actual uploaded oil column: `price`.
- Fixed invalid datetime conversion (`Datetime64` -> `pd.to_datetime(...)`).
- Replaced several broken end-of-notebook demo cells that referenced an undefined `df`.

### Lecture 4
- Added fallback synthetic Premier League data because `data/premier_league.xlsx` was missing.
- Fixed file loading for uploaded `retail_2016_2017.csv` and `transactions.csv`.
- Fixed broken query column names (`HomeTeam`/`AwayTeam` -> `Home`/`Away`).
- Fixed invalid matplotlib style strings (`solid`/`dashed` -> `-`/`--`).

### Lecture 5
- Replaced remote Titanic download with a local synthetic Titanic-like dataset so the notebook works offline.
- Added missing `plot_tree` import.
- Kept the same overall lesson flow: regression, classification, clustering, feature engineering, outlier handling.

## Notes
- I left comments marked `# FIX:` directly inside the repaired cells so you can see what changed.
- I did **not** rewrite the course pedagogy from scratch; I only repaired the parts that were broken or brittle.
- I did **not** change `pyproject.toml` yet. If you want, I can also make a cleaned `pyproject_fixed.toml` with more realistic package versions.
