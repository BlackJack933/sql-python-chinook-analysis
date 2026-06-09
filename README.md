# Chinook Database Analysis

SQL analysis of the [Chinook database](https://github.com/lerocha/chinook-database) — a sample SQLite database representing a small digital music store — using Python, SQLite, Pandas, and Matplotlib.

## Business Questions

| # | Question | Answer |
|---|----------|--------|
| 1 | Which are the 10 best-selling tracks? | All top tracks tied at 2 units sold |
| 2 | Which country generates the most revenue? | USA — $523.06 |
| 3 | Who is the top-performing sales employee? | Jane Peacock — $833.04 |

## Project Structure

```
chinook-analysis/
├── chinook_analysis.ipynb       # Main notebook
├── Chinook_Sqlite.sqlite        # Source database
└── README.md
```

## Workflow

1. **Setup** — Connect to the SQLite database via `sqlite3`
2. **Schema Exploration** — Identify tables and relationships using `sqlite_master` and `PRAGMA`
3. **Business Questions** — Write SQL queries and load results into Pandas DataFrames
4. **Visualization** — Bar chart of revenue by country (top 10) using Matplotlib

## Key SQL Concepts Used

- `JOIN` across multiple tables (`Track`, `InvoiceLine`, `Invoice`, `Customer`, `Employee`)
- `GROUP BY` with aggregate functions (`SUM`)
- `ORDER BY` on computed aliases
- Grouping by primary key (`TrackId`, `EmployeeId`) to avoid merging records with duplicate names

## Requirements

```
python >= 3.8
pandas
matplotlib
```

`sqlite3` is part of the Python standard library — no installation needed.

## How to Run

1. Download the Chinook database file from the [official repository](https://github.com/lerocha/chinook-database/blob/master/ChinookDatabase/DataSources/Chinook_Sqlite.sqlite) and place it in the project folder.
2. Install dependencies:
   ```bash
   pip install pandas matplotlib
   ```
3. Open `chinook_analysis.ipynb` in Jupyter and run all cells top to bottom.
