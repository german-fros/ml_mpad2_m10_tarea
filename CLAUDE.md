# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a data science project template following the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology. The project structure is designed to support the complete data science workflow from business understanding to deployment.

## Commands

### Environment Setup
```bash
# Activate virtual environment
venv\Scripts\activate     # Windows

# Run main script
python src/main.py
```

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