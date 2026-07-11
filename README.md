# Superstore Sales Analysis 2015–2018

Análisis del comportamiento de ventas en retail para la optimización de decisiones comerciales mediante visualización de datos.

**Pregunta analítica:** ¿Qué patrones estacionales y diferencias regionales en el desempeño de las categorías influyen en las ventas, y cómo pueden utilizarse para apoyar la toma de decisiones del negocio?

## Dataset

- **Fuente:** [Superstore Sales Dataset](https://www.kaggle.com/datasets/rohitsahoo/sales-forecasting) (Sahoo, 2020) — Kaggle
- **Tamaño:** 9,800 filas, transacciones 2015–2018

## Pipeline

1. Limpieza (tipado de fechas, texto categórico, nulos en Postal Code, duplicados)
2. Feature engineering (Nivel_Ventas, Region_Category, Shipping_Time, variables temporales)
3. EDA y perfilado sobre `train_clean_enriched.csv`
4. Agregación a nivel Región-Categoría-Trimestre (5 tablas derivadas, 192 combinaciones)
5. PCA sobre las métricas agregadas (2 componentes, 84.6% varianza explicada) → `region_category_quarter_pca.csv`
6. Dashboard en Tableau, conectando fuentes agregadas + PCA por relaciones (no joins físicos)

## Resultados clave

| Métrica | Valor |
|---|---|
| Ventas totales | $2,261,536.78 |
| Órdenes totales | 9,800 |
| Región líder | West (31.4%) |
| Categoría líder | Technology ($827,456) |

## Entregables

- [Dashboard final (Tableau Public)](https://public.tableau.com/app/profile/sofia.cardenas7499/viz/DashboardFinal_17837372829700/DashboardAlpha)
- Documento técnico completo (informe + resumen ejecutivo)
- Notebooks del pipeline (limpieza → EDA → agregación → PCA)
- Presentación de defensa
- [Video de exposición (entrega 4)](https://youtu.be/-NQcbajeSsk)

## Equipo

- Miranda Cardenas, Sofia Gabriel — u20191c439
- Olivera Alvarez, Lizbeth Teresita — u201616851
- Gomez Rubina, Luis David — U20221C621

**Curso:** Data Visualization — UPC, 2026
**Docente:** Carlos Adrian Alarcon Delgado
