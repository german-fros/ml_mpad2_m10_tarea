# Comprensión de los Datos

## Proyecto 1

### Fuentes de Datos

Los datos provienen de 9 archivos Excel que contienen información completa de los equipos del campeonato uruguayo de las temporadas 2022, 2023 y 2024. Los archivos están organizados en 3 categorías principales:


#### 1. Información General de Partidos (sb_matches_YYYY.xlsx)

**Estructura:**
- **2022**: 298 registros × 27 columnas
- **2023**: 300 registros × 27 columnas  
- **2024**: 297 registros × 27 columnas

**Análisis Exploratorio Inicial:**
- Contiene información básica de todos los partidos (fecha, equipos, marcador, estadio, árbitro, etc.)
- Variables clave: match_id, match_date, home_team, away_team, home_score, away_score, match_week
- Identificadores únicos por partido permiten cruzar información con otros datasets
- Datos de asistencia completamente faltantes en las 3 temporadas (attendance = 0 registros)

**Problemas Detectados:**
- 2022: 3 partidos sin marcador final (home_score, away_score faltantes)
- 2023: Datos más completos, solo 10 árbitros faltantes
- 2024: 1 árbitro faltante, datos más consistentes
- Columnas last_updated_360 completamente vacías en todas las temporadas


#### 2. Estadísticas de Equipos por Partido (sb_team_match_stats_YYYY.xlsx)

**Estructura:**
- **2022**: 588 registros × 91 columnas
- **2023**: 600 registros × 91 columnas
- **2024**: 586 registros × 91 columnas

**Análisis Exploratorio Inicial:**
- Estadísticas detalladas de cada equipo por partido
- 16 equipos únicos en todas las temporadas
- Métricas de rendimiento: xG, tiros, pases, posesión, etc.
- Datos muy completos (solo 1 valor faltante por temporada)

**Problemas Detectados:**
- Calidad de datos excelente, mínimos valores faltantes
- Solo 1 columna con valores faltantes por temporada
- Datos consistentes entre temporadas


#### 3. Estadísticas Agregadas por Equipo (sb_team_season_stats_YYYY.xlsx)

**Estructura:**
- **2022**: 16 registros × 181 columnas
- **2023**: 16 registros × 181 columnas
- **2024**: 16 registros × 181 columnas

**Análisis Exploratorio Inicial:**
- Estadísticas agregadas por temporada completa para cada equipo
- 16 equipos únicos por temporada (estructura de liga consistente)
- Métricas comprehensivas de rendimiento por temporada
- Datos muy completos para análisis de predicción

**Problemas Detectados:**
- Solo 16 valores faltantes por temporada (1 por equipo)
- 1 columna con valores faltantes por temporada
- Datos de alta calidad para modelado


## Proyecto 2

### Fuentes de Datos

Los datos provienen de 6 archivos Excel que contienen información completa de los jugadores del campeonato uruguayo de las temporadas 2022, 2023 y 2024. Los archivos están organizados en 2 categorías principales:

#### 1. Estadísticas de Jugadores por Partido (sb_player_match_stats_YYYY.xlsx)

**Estructura:**
- **2022**: 9,057 registros × 167 columnas
- **2023**: 9,316 registros × 167 columnas
- **2024**: 9,180 registros × 167 columnas

**Análisis Exploratorio Inicial:**
- Estadísticas detalladas de cada jugador por partido jugado
- 521-551 jugadores únicos por temporada
- 16 equipos consistentes en todas las temporadas
- Métricas avanzadas: xG, pases, defensas, goles, asistencias, etc.

**Problemas Detectados:**
- 93 columnas con valores faltantes de 167 totales, principalmente en métricas específicas de porteros

#### 2. Estadísticas Agregadas por Jugador (sb_player_season_stats_YYYY.xlsx)

**Estructura:**
- **2022**: 540 registros × 224 columnas
- **2023**: 580 registros × 224 columnas
- **2024**: 571 registros × 224 columnas

**Análisis Exploratorio Inicial:**
- Estadísticas agregadas por temporada completa para cada jugador
- 523-554 jugadores únicos por temporada
- Mayor cantidad de métricas que los datos por partido (224 vs 167 columnas)
- Incluye métricas calculadas y promedios por temporada

**Problemas Detectados:**
- 122-124 columnas con valores faltantes de 224 totales, principalmente en métricas específicas de porteros
- Inconsistencias en jugadores que cambiaron de equipo durante la temporada


## Problemas Detectados Globales

1. **Inconsistencia en Tipos de Datos**: Scores como float en 2022, int en 2023-2024
2. **Datos de Asistencia**: Completamente faltantes en todos los archivos de partidos
3. **Columnas Redundantes**: Varias columnas completamente vacías
4. **Transferencias**: Jugadores que cambiaron de equipo pueden tener registros duplicados
