# Proyecto 7 — Visualización básica con Pandas Plot / Matplotlib

**Laboratorio Práctico 2.1 · Ciencia de Datos · Equipo B (Data Storytelling y Visualización)**

## Caso de uso

**Pregunta:** ¿cómo cambió la esperanza de vida en Latinoamérica entre 1952 y 2007, y qué relación tiene con la riqueza de cada país?

El proyecto original de Frank Andrade grafica la población de cinco países grandes (EE. UU., India, China, Indonesia y Brasil). Esta adaptación reutiliza el mismo código (`pivot()` + `DataFrame.plot(kind=...)`) con un dataset distinto, descargado de Kaggle, para analizar la esperanza de vida de México, Brasil, Argentina, Colombia y Chile.

## Dataset

| | |
|---|---|
| Nombre | Gapminder World |
| Autor | Tetiana Klimonova (datos originales de Gapminder.org) |
| Fuente | https://www.kaggle.com/datasets/tklimonova/gapminder-datacamp-2007 |
| Licencia | CC0: Public Domain |
| Archivo usado | `gapminder_full.csv` — 1,704 filas × 6 columnas, 142 países, 1952-2007 (cada 5 años), sin nulos |
| Columnas | `country`, `year`, `population`, `continent`, `life_exp`, `gdp_cap` |

## Qué se adaptó

| Sección | Original | Adaptado |
|---|---|---|
| Tabla pivote | `values='population'` | `values='life_exp'`, 5 países latinoamericanos |
| Lineplot | Población 1955-2020 | Esperanza de vida 1952-2007 |
| Barplot | Año 2020 | Año 2007 (último del dataset) |
| Piechart | Población por país | Población de los 5 países en 2007 (la esperanza de vida no es "parte de un todo") |
| Boxplot | EE. UU. y 5 países | México y 5 países |
| Histograma | Población de 2 países | Esperanza de vida de todos los países de África vs. Europa en 2007 |
| Scatter | Año vs. población | PIB per cápita vs. esperanza de vida, 142 países, escala logarítmica |
| Interactivo | `cufflinks` (`.iplot()`) | `plotly.express` (cufflinks no se actualiza desde 2020 y falla al importarse) |
| Extra | — | Sección "¿Qué pasa si...?": `kind='barh'`, `stacked=True`, `logx=False` |

## Resultados principales

- Los cinco países ganaron entre **13 (Argentina) y 25 años (México)** de esperanza de vida entre 1952 y 2007.
- En 2007 todos los países europeos superan los 71 años; la mediana africana es de unos 53.
- La esperanza de vida crece con el PIB per cápita: correlación de **0.68** en escala lineal y **0.81** con el logaritmo del PIB.

## Cómo ejecutarlo

```bash
pip install pandas matplotlib plotly openpyxl jupyter
jupyter notebook Proyecto7_Visualizacion_Adaptado.ipynb
```

El CSV debe estar en la misma carpeta que el notebook. Al ejecutarse genera:

- `tabla_pivote_esperanza_vida.xlsx`: tabla pivote exportada
- `grafica_esperanza_vida.png`: gráfica guardada con `plt.savefig`
- `grafica_interactiva_gapminder.html`: gráfica animada (abrir en el navegador; GitHub no muestra las gráficas Plotly dentro del notebook)

## Créditos

- Código base: Frank Andrade, repositorio [thepycoach/curso-data-science](https://github.com/thepycoach/curso-data-science), carpeta `07.Visualizacion de Datos`.
- Video: *Curso de Python para Data Science desde 0 (12 Horas)*, del minuto 4:59:32 al 6:15:31.
