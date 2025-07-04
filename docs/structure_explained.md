# Estructura del Proyecto CRISP-DM

Esta estructura está diseñada para proyectos de ciencia de datos siguiendo la metodología CRISP-DM.

## Carpetas

- `data/raw/`: Datos crudos, sin modificar.
- `data/processed/`: Datos limpios y transformados.
- `notebooks/`: Notebooks de análisis exploratorio y pruebas.
- `src/`: Scripts fuente reutilizables. Incluye `main.py` como punto de entrada.
- `models/`: Modelos entrenados guardados (.pkl, .joblib, etc.).
- `reports/`: Figuras y reportes exportados para presentaciones.
- `docs/`: Documentación estructurada por fases CRISP-DM.
  - `img/`: Visuales incluidas en los documentos.
  - `reports/`: Informes generados (PDFs, presentaciones).
  - `references/`: Material de referencia usado.
  - `.md`: Plantillas por etapa del proceso.

## Archivos Clave

- `README.md`: Explicación general del proyecto, dependencias y cómo ejecutar.
- `docs/*.md`: Plantillas por fase del proceso CRISP-DM para registrar decisiones, hallazgos y resultados.

Esta plantilla puede ser reutilizada como base para nuevos proyectos, asegurando trazabilidad y orden.
