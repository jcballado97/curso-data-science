# Proyecto 8 - Visualización Estadística con Seaborn

## Descripción
Proyecto de análisis exploratorio y visualización estadística utilizando el dataset Gapminder World y Python.

## Objetivo
Analizar y visualizar diferentes variables del dataset Gapminder mediante histogramas, distribuciones y mapas de calor para identificar patrones y relaciones entre variables numéricas.

## Dataset
`gapminder_full.csv`

Contiene 1,704 registros del periodo 1952-2007 y las variables `country`, `year`, `population`, `continent`, `life_exp` y `gdp_cap`.

## Figuras
La carpeta `figuras/` contiene:
- `01_distribucion_esperanza_vida.png`
- `02_distribucion_por_continente.png`
- `03_distribucion_pib_per_capita.png`
- `04_heatmap_correlacion.png`
- `05_heatmap_america.png`

## Librerías
- Python
- Pandas
- Matplotlib
- Seaborn

## Estructura
```text
Proyecto_8_Visualizacion_Estadistica_Seaborn/
├── Proyecto_8_Visualizacion_Estadistica_Seaborn.ipynb
├── gapminder_full.csv
├── README.md
└── figuras/
    ├── 01_distribucion_esperanza_vida.png
    ├── 02_distribucion_por_continente.png
    ├── 03_distribucion_pib_per_capita.png
    ├── 04_heatmap_correlacion.png
    └── 05_heatmap_america.png
```

## Ejecución
Coloca el CSV en la misma carpeta que el notebook. El notebook puede abrirse en Google Colab o ejecutarse localmente con Python y las librerías indicadas.

## Conclusiones
Seaborn permite crear visualizaciones estadísticas a partir de DataFrames de Pandas. Los histogramas muestran la distribución de los datos y los mapas de calor facilitan la interpretación de las correlaciones entre variables.

## Respuesta breve para exposición
"En este proyecto utilizamos Seaborn para visualizar el dataset Gapminder. Analizamos distribuciones de esperanza de vida y PIB per cápita y usamos mapas de calor para observar correlaciones entre variables."
