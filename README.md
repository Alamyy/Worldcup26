# World Cup 2026 Open Match Data

Open CSV dataset for exploring FIFA World Cup 2026 match, team, and player-level performance data.

The tables in this repository are based on publicly available post-match reports from the FIFA Training Centre. This repository publishes data tables only. It does not include report PDFs, player images, scraped media, or dashboard assets.

## What's Included

- 104 matches
- 48 teams
- 1,277 player records
- 21 published CSV tables
- Match metadata, scores, venues, groups, and source links
- Lineups, starters, substitutes, cards, goals, and appearance records
- Attempts at goal and event timelines
- Passing-network edges
- Player in-possession, out-of-possession, line-break, reception, crossing, and physical data
- Team key stats, phases, set plays, pressure, aerial control, goal prevention, and goalkeeping distribution

## Repository Layout

```text
data/csv/                 Published CSV tables
docs/data_dictionary.md   Table-by-table columns and row counts
docs/schema.md            Join keys and table relationships
docs/sources.md           Source and attribution notes
docs/table_inventory.md   Compact table inventory
metadata/schema.json      Machine-readable table columns
metadata/dataset_summary.json
metadata/table_manifest.csv
```

## Start Here

The core tables are:

- `data/csv/matches.csv`
- `data/csv/teams.csv`
- `data/csv/players.csv`
- `data/csv/match_teams.csv`
- `data/csv/match_appearances.csv`

Most player-level fact tables join through `appearance_id`. Most team-level fact tables join through `match_team_id`.

Example DuckDB query:

```sql
SELECT
  m.match_number,
  m.home_team,
  m.away_team,
  a.team,
  a.player_name,
  a.minute,
  a.outcome,
  a.body_part
FROM read_csv_auto('data/csv/attempts_at_goal.csv') a
JOIN read_csv_auto('data/csv/matches.csv') m
  ON a.match_id = m.match_id
ORDER BY m.match_number, a.minute;
```

## Related Project

Explore the companion analytics experience at [World Cup 26 Analytics Lab](https://worldcup26-analyticslab.vercel.app/).

The Analytics Lab is an interactive dashboard for browsing the tournament dataset visually: match summaries, team analytics, player profiles, comparisons, passing networks, tactical matchups, and scouting-style views built from these published data tables.

## Notes

- Data is provided as CSV for easy use in spreadsheets, BI tools, DuckDB, R, SQL engines, and notebooks.
- Source report links are available in `matches.csv` under `source_url`.
- This project is not affiliated with FIFA.
- Please cite the source reports and this repository when using the data.
