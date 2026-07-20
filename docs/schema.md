# Schema

This page describes the join keys and table relationships for the published CSV data.

## Main Identifiers

| Field | Meaning |
| --- | --- |
| `match_id` | Stable match identifier, for example `2026-M001-MEX-RSA`. |
| `match_number` | Tournament match number, `1` through `104`. |
| `team_id` | Short team code, for example `MEX`, `ARG`, or `USA`. |
| `match_team_id` | One team in one match: `{match_id}_{team_id}`. |
| `player_id` | Team-scoped player identifier. |
| `appearance_id` | One player appearance in one match: `{match_id}_{team_id}_{shirt_number}`. |

## Core Tables

| Table | Grain |
| --- | --- |
| `matches.csv` | One row per match. |
| `teams.csv` | One row per team. |
| `players.csv` | One row per team-scoped player. |
| `match_teams.csv` | One row per team per match. |
| `match_appearances.csv` | One row per player listed for a match. |

## Player-Level Tables

These tables join to `match_appearances.csv` through `appearance_id`:

- `attempts_at_goal.csv`
- `player_events.csv`
- `player_crosses_open_play.csv`
- `player_in_possession_distributions.csv`
- `player_line_breaks.csv`
- `player_offers_receptions.csv`
- `player_out_of_possession.csv`
- `player_physical_data.csv`

`passing_network_edges.csv` uses `from_appearance_id` and `to_appearance_id` for player-to-player connections.

## Team-Level Tables

These tables join to `match_teams.csv` through `match_team_id`:

- `team_aerial_control.csv`
- `team_defensive_pressure.csv`
- `team_goal_prevention.csv`
- `team_goalkeeping_distribution.csv`
- `team_key_stats.csv`
- `team_phases.csv`
- `team_set_plays.csv`

## Common Joins

Join match facts:

```sql
SELECT *
FROM match_teams mt
JOIN matches m ON mt.match_id = m.match_id;
```

Join player facts:

```sql
SELECT *
FROM player_physical_data p
JOIN match_appearances a ON p.appearance_id = a.appearance_id
JOIN matches m ON p.match_id = m.match_id;
```

Join passing networks:

```sql
SELECT *
FROM passing_network_edges e
JOIN match_appearances passer ON e.from_appearance_id = passer.appearance_id
JOIN match_appearances receiver ON e.to_appearance_id = receiver.appearance_id;
```
