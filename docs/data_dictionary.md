# Data Dictionary

This reference lists the published CSV tables, row counts, and columns. It describes the data as shipped in this repository.

## `attempts_at_goal.csv`

Rows: 2571

| Column |
| --- |
| `appearance_id` |
| `body_part` |
| `delivery_type` |
| `event_id` |
| `match_id` |
| `match_team_id` |
| `minute` |
| `outcome` |
| `player_id` |
| `player_name` |
| `shirt_number` |
| `source_page` |
| `team` |
| `team_id` |

## `match_appearances.csv`

Rows: 5392

| Column |
| --- |
| `appearance_id` |
| `appeared` |
| `goal_minutes` |
| `is_starter` |
| `match_id` |
| `match_team_id` |
| `own_goal_minutes` |
| `player_id` |
| `player_name` |
| `position` |
| `red_card_minutes` |
| `shirt_number` |
| `status` |
| `subbed_off_minutes` |
| `subbed_on_minutes` |
| `team` |
| `team_id` |
| `team_role` |
| `yellow_card_minutes` |

## `match_teams.csv`

Rows: 208

| Column |
| --- |
| `home_away` |
| `match_id` |
| `match_team_id` |
| `score` |
| `team_id` |
| `team_name` |

## `matches.csv`

Rows: 104

| Column |
| --- |
| `away_score` |
| `away_team` |
| `away_team_id` |
| `date` |
| `group` |
| `home_score` |
| `home_team` |
| `home_team_id` |
| `kickoff` |
| `match_id` |
| `match_number` |
| `page_count` |
| `penalty_result` |
| `source_url` |
| `venue` |

## `passing_network_edges.csv`

Rows: 52072

| Column |
| --- |
| `edge_id` |
| `from_appearance_id` |
| `from_player` |
| `from_player_id` |
| `from_shirt_number` |
| `match_id` |
| `match_team_id` |
| `pass_count` |
| `source_page` |
| `team` |
| `team_id` |
| `to_appearance_id` |
| `to_player` |
| `to_player_id` |
| `to_shirt_number` |

## `player_crosses_open_play.csv`

Rows: 3288

| Column |
| --- |
| `appearance_id` |
| `cutback` |
| `driven` |
| `inswing` |
| `lofted` |
| `match_id` |
| `match_team_id` |
| `outswing` |
| `player_id` |
| `player_name` |
| `push_cross` |
| `shirt_number` |
| `team` |
| `team_id` |
| `topic` |
| `total_attempted` |

## `player_events.csv`

Rows: 2587

| Column |
| --- |
| `appearance_id` |
| `event_id` |
| `event_type` |
| `match_id` |
| `match_team_id` |
| `minute` |
| `minute_raw` |
| `player_id` |
| `player_name` |
| `shirt_number` |
| `source_page` |
| `team` |
| `team_id` |

## `player_in_possession_distributions.csv`

Rows: 3288

| Column |
| --- |
| `appearance_id` |
| `attempts_at_goal` |
| `ball_progressions` |
| `crosses_attempted` |
| `crosses_completed` |
| `goals` |
| `line_break_completion_pct` |
| `line_breaks_attempted` |
| `line_breaks_completed` |
| `match_id` |
| `match_team_id` |
| `pass_completion_pct` |
| `passes_attempted` |
| `passes_completed` |
| `player_id` |
| `player_name` |
| `shirt_number` |
| `source_page` |
| `step_ins` |
| `switches_of_play` |
| `take_ons` |
| `team` |
| `team_id` |

## `player_line_breaks.csv`

Rows: 3288

| Column |
| --- |
| `appearance_id` |
| `direction_around` |
| `direction_over` |
| `direction_through` |
| `distribution_ball_progression` |
| `distribution_cross` |
| `distribution_pass` |
| `four_units_attacking_line` |
| `four_units_attacking_midfield_line` |
| `four_units_defensive_line` |
| `four_units_midfield_line` |
| `line_break_completion_pct` |
| `line_breaks_attempted` |
| `line_breaks_completed` |
| `match_id` |
| `match_team_id` |
| `player_id` |
| `player_name` |
| `shirt_number` |
| `team` |
| `team_id` |
| `three_units_attacking_line` |
| `three_units_defensive_line` |
| `three_units_midfield_line` |
| `topic` |
| `two_units_defensive_line` |
| `two_units_midfield_line` |

## `player_offers_receptions.csv`

Rows: 3288

| Column |
| --- |
| `appearance_id` |
| `in_behind` |
| `in_between` |
| `in_front` |
| `in_to_out` |
| `match_id` |
| `match_team_id` |
| `no_movement` |
| `offers_received` |
| `out_to_in` |
| `player_id` |
| `player_name` |
| `shirt_number` |
| `source_page` |
| `team` |
| `team_id` |
| `total_offers` |

## `player_out_of_possession.csv`

Rows: 3288

| Column |
| --- |
| `appearance_id` |
| `blocks` |
| `clearances` |
| `duels_won_aerial` |
| `duels_won_physical` |
| `interceptions` |
| `loose_ball_receptions` |
| `match_id` |
| `match_team_id` |
| `player_id` |
| `player_name` |
| `possession_contests_won` |
| `possession_interrupted` |
| `possession_regains` |
| `pressing_direct` |
| `pressing_indirect` |
| `pushing_on` |
| `pushing_on_into_pressing` |
| `shirt_number` |
| `tackles_made_won` |
| `team` |
| `team_id` |
| `topic` |

## `player_physical_data.csv`

Rows: 3288

| Column |
| --- |
| `appearance_id` |
| `high_speed_runs_zone3` |
| `match_id` |
| `match_team_id` |
| `player_id` |
| `player_name` |
| `shirt_number` |
| `source_page` |
| `sprints_zone4_5` |
| `team` |
| `team_id` |
| `top_speed_kmh` |
| `total_distance_m` |
| `zone1_0_7_kmh_m` |
| `zone2_7_15_kmh_m` |
| `zone3_15_20_kmh_m` |
| `zone4_20_25_kmh_m` |
| `zone5_25_plus_kmh_m` |

## `players.csv`

Rows: 1277

| Column |
| --- |
| `appearances_count` |
| `display_name` |
| `player_id` |
| `shirt_numbers` |
| `team_id` |

## `team_aerial_control.csv`

Rows: 208

| Column |
| --- |
| `delivery_cutback` |
| `delivery_driven` |
| `delivery_inswing` |
| `delivery_lofted` |
| `delivery_outswing` |
| `delivery_push` |
| `delivery_total` |
| `match_id` |
| `match_team_id` |
| `source_page` |
| `team` |
| `team_id` |

## `team_defensive_pressure.csv`

Rows: 208

| Column |
| --- |
| `avg_pressure_duration_s` |
| `ball_recovery_time_s` |
| `direct_pressures` |
| `forced_turnovers` |
| `match_id` |
| `match_team_id` |
| `pressing_direction_inside` |
| `pressing_direction_outside` |
| `pushing_on` |
| `pushing_on_into_pressing` |
| `source_page` |
| `team` |
| `team_id` |
| `total_pressures` |

## `team_goal_prevention.csv`

Rows: 208

| Column |
| --- |
| `deflect_retain` |
| `match_id` |
| `match_team_id` |
| `no_save_attempt` |
| `save_attempt` |
| `save_deflect` |
| `save_pct` |
| `save_retain` |
| `source_page` |
| `team` |
| `team_id` |
| `total_attempts_faced` |
| `total_interventions` |

## `team_goalkeeping_distribution.csv`

Rows: 832

| Column |
| --- |
| `match_id` |
| `match_team_id` |
| `metric` |
| `source_page` |
| `team` |
| `team_id` |
| `value` |

## `team_key_stats.csv`

Rows: 3432

| Column |
| --- |
| `match_id` |
| `match_team_id` |
| `metric` |
| `raw` |
| `team` |
| `team_id` |
| `unit` |
| `value` |

## `team_phases.csv`

Rows: 3536

| Column |
| --- |
| `match_id` |
| `match_team_id` |
| `phase` |
| `phase_group` |
| `raw` |
| `team` |
| `team_id` |
| `unit` |
| `value` |

## `team_set_plays.csv`

Rows: 3328

| Column |
| --- |
| `category` |
| `from_left_side` |
| `from_right_side` |
| `match_id` |
| `match_team_id` |
| `metric` |
| `source_page` |
| `team` |
| `team_id` |
| `value` |

## `teams.csv`

Rows: 48

| Column |
| --- |
| `team_id` |
| `team_name` |
