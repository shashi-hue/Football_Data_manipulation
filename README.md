# ⚽ Football Rolling Stats Generator

This project computes rolling statistics for football teams over the last 5, 15, and 38 matches.

## 📋 Features

- Calculates stats like:
  - Goals Scored/Conceded
  - Shots, Fouls, Corners
  - Cards (Yellow/Red)
  - Match Results (W/D/L)
- Separate tracking for home and away teams
- Avoids data leakage by only using **past matches**

## 🛠 How It Works

1. Loads and sorts raw match data by date.
2. Tracks each team's match history.
3. For every match, looks up the last N games for both home and away teams.
4. Calculates the rolling stats and appends them as new columns.

## 🧠 Rolling Windows

- Last 5 matches
- Last 15 matches
- Last 38 matches

## 📂 Files

- `data/Raw_Football_Data.csv` – Input data
- `data/Manipulated_Football_Data_v2.csv` – Output with rolling stats
- `script/rolling_stats_generator.py` – Main script

## 📌 Example Output

| Date       | HomeTeam | AwayTeam | FTHG | FTAG | ... | FTHG_L5 | FTAG_L5 | ... |
|------------|----------|----------|------|------|-----|---------|---------|-----|
| 2022-01-01 | Arsenal  | Chelsea  | 2    | 1    | ... | 7       | 4       | ... |

## 🧪 Run It Yourself

```bash
Task1.ipynb
