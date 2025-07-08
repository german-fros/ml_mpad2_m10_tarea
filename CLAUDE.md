# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a data science project template following the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology. The project structure is designed to support the complete data science workflow from business understanding to deployment.

## Commands

- NO activar venv en comandos bash
- Generar código Python puro sin preocuparse por
  dependencias
- Enfocarse en lógica de análisis, no en configuración de entorno;
- Comentar adecuadamente las partes importantes del código
- Al crear funciones en una celda de notebook, no escribas debajo un codigo que la ejecute
- Siempre que precises ejecutar el codigo para obtener alguna información y pueda dar error con el venv, me avisas antes;
- Al graficar, evita colocar titulo en los ejes que sean reduntantes (año, nombre, temporada, etc). También, modifica solamente lo solicitado y sugiere posibles modificaciones en otras partes del codigo que se puedan ver afectadas, no toques ninguna otra celda del notebook.

## Architecture

### CRISP-DM Structure
The project follows a structured approach with distinct phases:

1. **Business Understanding** (`docs/1_business_understanding.md`) - Problem definition and objectives
2. **Data Understanding** (`docs/2_data_understanding.md`) - Data exploration and quality assessment
3. **Data Preparation** (`docs/3_data_preparation.md`) - Data cleaning and feature engineering
4. **Modeling** (`docs/4_modeling.md`) - Model selection and training
5. **Evaluation** (`docs/5_evaluation.md`) - Model assessment and validation
6. **Deployment** (`docs/6_deployment_plan.md`) - Implementation strategy

### Directory Structure
- `data/raw/` - Original, immutable data
- `data/processed/` - Cleaned and transformed datasets
- `src/` - Reusable Python modules and scripts
- `notebooks/` - Jupyter notebooks for exploration and analysis
- `models/` - Trained model artifacts (.pkl, .joblib files)
- `reports/figures/` - Generated visualizations and charts
- `docs/` - Project documentation and phase templates

### Key Files
- `src/main.py` - Main entry point for the project
- `docs/experiments_log.md` - Experiment tracking table
- `docs/structure_explained.md` - Detailed project structure documentation

### Estructura datasets
dataset:sb_matches_2022.xlsx
Index(['match_id', 'match_date', 'kick_off', 'competition', 'season',
       'home_team', 'away_team', 'home_score', 'away_score', 'attendance',
       'behind_closed_doors', 'neutral_ground', 'collection_status',
       'play_status', 'match_status', 'match_status_360', 'last_updated',
       'last_updated_360', 'match_week', 'competition_stage', 'stadium',
       'referee', 'home_managers', 'away_managers', 'data_version',
       'shot_fidelity_version', 'xy_fidelity_version'],
      dtype='object')
dataset:sb_matches_2023.xlsx
Index(['match_id', 'match_date', 'kick_off', 'competition', 'season',
       'home_team', 'away_team', 'home_score', 'away_score', 'attendance',
       'behind_closed_doors', 'neutral_ground', 'collection_status',
       'play_status', 'match_status', 'match_status_360', 'last_updated',
       'last_updated_360', 'match_week', 'competition_stage', 'stadium',
       'referee', 'home_managers', 'away_managers', 'data_version',
       'shot_fidelity_version', 'xy_fidelity_version'],
      dtype='object')
dataset:sb_matches_2024.xlsx
Index(['match_id', 'match_date', 'kick_off', 'competition', 'season',
       'home_team', 'away_team', 'home_score', 'away_score', 'attendance',
       'behind_closed_doors', 'neutral_ground', 'collection_status',
       'play_status', 'match_status', 'match_status_360', 'last_updated',
       'last_updated_360', 'match_week', 'competition_stage', 'stadium',
       'referee', 'home_managers', 'away_managers', 'data_version',
       'shot_fidelity_version', 'xy_fidelity_version'],
      dtype='object')
dataset:sb_team_match_stats_2022.xlsx
Index(['match_id', 'team_name', 'team_id', 'account_id', 'team_match_minutes',
       'team_match_np_xg_per_shot', 'team_match_np_xg', 'team_match_np_shots',     
       'team_match_goals', 'team_match_xa', 'team_match_key_passes',
       'team_match_assists', 'team_match_through_balls',
       'team_match_passes_into_box', 'team_match_touches_inside_box',
       'team_match_tackles', 'team_match_interceptions',
       'team_match_possession', 'team_match_dribbles_faced',
       'team_match_dribbles', 'team_match_challenge_ratio', 'team_match_fouls',    
       'team_match_dispossessions', 'team_match_long_balls',
       'team_match_successful_long_balls', 'team_match_long_ball_ratio',
       'team_match_shots_blocked', 'team_match_clearances',
       'team_match_aerials', 'team_match_successful_aerials',
       'team_match_aerial_ratio', 'team_match_passes',
       'team_match_successful_passes', 'team_match_passing_ratio',
       'team_match_op_passes', 'team_match_forward_passes',
       'team_match_backward_passes', 'team_match_sideways_passes',
       'team_match_op_f3_passes', 'team_match_op_f3_forward_passes',
       'team_match_op_f3_backward_passes', 'team_match_op_f3_sideways_passes',     
       'team_match_np_shots_on_target', 'team_match_crosses',
       'team_match_successful_crosses', 'team_match_crossing_ratio',
       'team_match_penalties_won', 'team_match_passes_inside_box',
       'team_match_op_xa', 'team_match_op_assists',
       'team_match_pressured_long_balls', 'team_match_unpressured_long_balls',     
       'team_match_aggressive_actions', 'team_match_turnovers',
       'team_match_crosses_into_box', 'team_match_sp_xa',
       'team_match_op_shots', 'team_match_touches',
       'team_match_pressure_regains', 'team_match_box_cross_ratio',
       'team_match_deep_progressions', 'team_match_shot_touch_ratio',
       'team_match_fouls_won', 'team_match_xgchain', 'team_match_op_xgchain',      
       'team_match_xgbuildup', 'team_match_op_xgbuildup',
       'team_match_xgchain_per_possession',
       'team_match_op_xgchain_per_possession',
       'team_match_xgbuildup_per_possession',
       'team_match_op_xgbuildup_per_possession', 'team_match_pressures',
       'team_match_pressure_duration_total',
       'team_match_pressure_duration_avg', 'team_match_pressured_action_fails',    
       'team_match_counterpressures',
       'team_match_counterpressure_duration_total',
       'team_match_counterpressure_duration_avg',
       'team_match_counterpressured_action_fails', 'team_match_obv',
       'team_match_obv_pass', 'team_match_obv_shot',
       'team_match_obv_defensive_action', 'team_match_obv_dribble_carry',
       'team_match_obv_gk', 'team_match_deep_completions',
       'team_match_ball_recoveries', 'team_match_np_psxg',
       'team_match_penalties_faced', 'team_match_penalties_conceded',
       'team_match_fhalf_ball_recoveries'],
      dtype='object')
dataset:sb_team_match_stats_2023.xlsx
Index(['match_id', 'team_name', 'team_id', 'account_id', 'team_match_minutes',
       'team_match_np_xg_per_shot', 'team_match_np_xg', 'team_match_np_shots',     
       'team_match_goals', 'team_match_xa', 'team_match_key_passes',
       'team_match_assists', 'team_match_through_balls',
       'team_match_passes_into_box', 'team_match_touches_inside_box',
       'team_match_tackles', 'team_match_interceptions',
       'team_match_possession', 'team_match_dribbles_faced',
       'team_match_dribbles', 'team_match_challenge_ratio', 'team_match_fouls',    
       'team_match_dispossessions', 'team_match_long_balls',
       'team_match_successful_long_balls', 'team_match_long_ball_ratio',
       'team_match_shots_blocked', 'team_match_clearances',
       'team_match_aerials', 'team_match_successful_aerials',
       'team_match_aerial_ratio', 'team_match_passes',
       'team_match_successful_passes', 'team_match_passing_ratio',
       'team_match_op_passes', 'team_match_forward_passes',
       'team_match_backward_passes', 'team_match_sideways_passes',
       'team_match_op_f3_passes', 'team_match_op_f3_forward_passes',
       'team_match_op_f3_backward_passes', 'team_match_op_f3_sideways_passes',     
       'team_match_np_shots_on_target', 'team_match_crosses',
       'team_match_successful_crosses', 'team_match_crossing_ratio',
       'team_match_penalties_won', 'team_match_passes_inside_box',
       'team_match_op_xa', 'team_match_op_assists',
       'team_match_pressured_long_balls', 'team_match_unpressured_long_balls',     
       'team_match_aggressive_actions', 'team_match_turnovers',
       'team_match_crosses_into_box', 'team_match_sp_xa',
       'team_match_op_shots', 'team_match_touches',
       'team_match_pressure_regains', 'team_match_box_cross_ratio',
       'team_match_deep_progressions', 'team_match_shot_touch_ratio',
       'team_match_fouls_won', 'team_match_xgchain', 'team_match_op_xgchain',      
       'team_match_xgbuildup', 'team_match_op_xgbuildup',
       'team_match_xgchain_per_possession',
       'team_match_op_xgchain_per_possession',
       'team_match_xgbuildup_per_possession',
       'team_match_op_xgbuildup_per_possession', 'team_match_pressures',
       'team_match_pressure_duration_total',
       'team_match_pressure_duration_avg', 'team_match_pressured_action_fails',    
       'team_match_counterpressures',
       'team_match_counterpressure_duration_total',
       'team_match_counterpressure_duration_avg',
       'team_match_counterpressured_action_fails', 'team_match_obv',
       'team_match_obv_pass', 'team_match_obv_shot',
       'team_match_obv_defensive_action', 'team_match_obv_dribble_carry',
       'team_match_obv_gk', 'team_match_deep_completions',
       'team_match_ball_recoveries', 'team_match_np_psxg',
       'team_match_penalties_faced', 'team_match_penalties_conceded',
       'team_match_fhalf_ball_recoveries'],
      dtype='object')
dataset:sb_team_match_stats_2024.xlsx
Index(['match_id', 'team_name', 'team_id', 'account_id', 'team_match_minutes',
       'team_match_np_xg_per_shot', 'team_match_np_xg', 'team_match_np_shots',     
       'team_match_goals', 'team_match_xa', 'team_match_key_passes',
       'team_match_assists', 'team_match_through_balls',
       'team_match_passes_into_box', 'team_match_touches_inside_box',
       'team_match_tackles', 'team_match_interceptions',
       'team_match_possession', 'team_match_dribbles_faced',
       'team_match_dribbles', 'team_match_challenge_ratio', 'team_match_fouls',    
       'team_match_dispossessions', 'team_match_long_balls',
       'team_match_successful_long_balls', 'team_match_long_ball_ratio',
       'team_match_shots_blocked', 'team_match_clearances',
       'team_match_aerials', 'team_match_successful_aerials',
       'team_match_aerial_ratio', 'team_match_passes',
       'team_match_successful_passes', 'team_match_passing_ratio',
       'team_match_op_passes', 'team_match_forward_passes',
       'team_match_backward_passes', 'team_match_sideways_passes',
       'team_match_op_f3_passes', 'team_match_op_f3_forward_passes',
       'team_match_op_f3_backward_passes', 'team_match_op_f3_sideways_passes',     
       'team_match_np_shots_on_target', 'team_match_crosses',
       'team_match_successful_crosses', 'team_match_crossing_ratio',
       'team_match_penalties_won', 'team_match_passes_inside_box',
       'team_match_op_xa', 'team_match_op_assists',
       'team_match_pressured_long_balls', 'team_match_unpressured_long_balls',     
       'team_match_aggressive_actions', 'team_match_turnovers',
       'team_match_crosses_into_box', 'team_match_sp_xa',
       'team_match_op_shots', 'team_match_touches',
       'team_match_pressure_regains', 'team_match_box_cross_ratio',
       'team_match_deep_progressions', 'team_match_shot_touch_ratio',
       'team_match_fouls_won', 'team_match_xgchain', 'team_match_op_xgchain',      
       'team_match_xgbuildup', 'team_match_op_xgbuildup',
       'team_match_xgchain_per_possession',
       'team_match_op_xgchain_per_possession',
       'team_match_xgbuildup_per_possession',
       'team_match_op_xgbuildup_per_possession', 'team_match_pressures',
       'team_match_pressure_duration_total',
       'team_match_pressure_duration_avg', 'team_match_pressured_action_fails',    
       'team_match_counterpressures',
       'team_match_counterpressure_duration_total',
       'team_match_counterpressure_duration_avg',
       'team_match_counterpressured_action_fails', 'team_match_obv',
       'team_match_obv_pass', 'team_match_obv_shot',
       'team_match_obv_defensive_action', 'team_match_obv_dribble_carry',
       'team_match_obv_gk', 'team_match_deep_completions',
       'team_match_ball_recoveries', 'team_match_np_psxg',
       'team_match_penalties_faced', 'team_match_penalties_conceded',
       'team_match_fhalf_ball_recoveries'],
      dtype='object')
dataset:sb_team_season_stats_2022.xlsx
Index(['account_id', 'team_name', 'team_id', 'competition_id',
       'competition_name', 'season_id', 'season_name', 'team_female',
       'team_season_matches', 'team_season_minutes',
       ...
       'team_season_obv_shot_conceded_pg',
       'team_season_obv_defensive_action_conceded_pg',
       'team_season_obv_dribble_carry_conceded_pg',
       'team_season_obv_gk_conceded_pg', 'team_season_passes_pg',
       'team_season_successful_passes_pg', 'team_season_passes_conceded_pg',       
       'team_season_successful_passes_conceded_pg', 'team_season_op_passes_pg',    
       'team_season_op_passes_conceded_pg'],
      dtype='object', length=181)
dataset:sb_team_season_stats_2023.xlsx
Index(['account_id', 'team_name', 'team_id', 'competition_id',
       'competition_name', 'season_id', 'season_name', 'team_female',
       'team_season_matches', 'team_season_minutes',
       ...
       'team_season_obv_shot_conceded_pg',
       'team_season_obv_defensive_action_conceded_pg',
       'team_season_obv_dribble_carry_conceded_pg',
       'team_season_obv_gk_conceded_pg', 'team_season_passes_pg',
       'team_season_successful_passes_pg', 'team_season_passes_conceded_pg',       
       'team_season_successful_passes_conceded_pg', 'team_season_op_passes_pg',    
       'team_season_op_passes_conceded_pg'],
      dtype='object', length=181)
dataset:sb_team_season_stats_2024.xlsx
Index(['account_id', 'team_name', 'team_id', 'competition_id',
       'competition_name', 'season_id', 'season_name', 'team_female',
       'team_season_matches', 'team_season_minutes',
       ...
       'team_season_obv_shot_conceded_pg',
       'team_season_obv_defensive_action_conceded_pg',
       'team_season_obv_dribble_carry_conceded_pg',
       'team_season_obv_gk_conceded_pg', 'team_season_passes_pg',
       'team_season_successful_passes_pg', 'team_season_passes_conceded_pg',       
       'team_season_successful_passes_conceded_pg', 'team_season_op_passes_pg',    
       'team_season_op_passes_conceded_pg'],
      dtype='object', length=181)

## Development Notes

- The project uses a Python virtual environment (venv) for dependency management
- All model artifacts should be saved to the `models/` directory
- Experiment results should be logged in `docs/experiments_log.md`
- Follow the CRISP-DM methodology by completing each phase documentation before proceeding

## Claude Code Configuration

### Estilo de Código
- **Naming:** camelCase
- **Manejo de errores:** try/catch obligatorio

### Commits Git
Después de validar modificaciones, generar commits siguiendo esta estructura:

| Prefix | Uso |
|--------|-----|
| `feat:` | Nueva funcionalidad |
| `fix:` | Corregir error o bug |
| `chore:` | Tareas de mantenimiento, refactor, setup sin impacto en funcionalidades |
| `refactor:` | Reescrituras internas que no cambian el comportamiento |
| `docs:` | Actualizar documentación |
| `style:` | Cambios visuales o de formato sin afectar lógica |
| `test:` | Agregar o modificar pruebas automatizadas |

### Workflow
1. Desarrollar y validar cambios en notebook
2. Confirmar que modificaciones son correctas
3. Generar commits categorizados por tipo de cambio
4. Un commit por cada tipo de modificación realizada