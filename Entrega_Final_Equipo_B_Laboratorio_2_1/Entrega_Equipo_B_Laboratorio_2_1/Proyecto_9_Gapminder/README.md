# Proyecto 9 - Preprocesamiento para Machine Learning

**Laboratorio Práctico 2.1 - Ciencia de Datos - Equipo B**

## Caso de uso

**Pregunta:** ¿cómo preparar datos históricos de desarrollo mundial que contienen variables numéricas y categóricas para utilizarlos correctamente en Machine Learning?

El código original de Frank Andrade utiliza el dataset Boston House Prices y selecciona variables numéricas para entrenar una regresión lineal. Esta adaptación conserva la lógica de separar predictores y variable objetivo, pero utiliza el mismo dataset Gapminder del Proyecto 7 e incorpora el preprocesamiento solicitado en el PDF: escalado de datos y One Hot Encoding.

Como ejercicio se clasifica cada observación país-año según tenga una esperanza de vida baja o alta respecto a la mediana histórica.

## Dataset

| | |
|---|---|
| Nombre | Gapminder World |
| Fuente | https://www.kaggle.com/datasets/tklimonova/gapminder-datacamp-2007 |
| Licencia | CC0: Public Domain |
| Archivo usado | `gapminder_full.csv` |
| Dimensiones | 1,704 filas x 6 columnas; 142 países; 1952-2007 |
| Columnas | `country`, `year`, `population`, `continent`, `life_exp`, `gdp_cap` |

## Qué se adaptó

| Elemento | Código original | Caso adaptado |
|---|---|---|
| Dataset | Boston House Prices | Gapminder World completo |
| Predictores numéricos | `Rooms`, `Distance` | `year`, `population`, `gdp_cap` |
| Variable categórica | No utiliza | `continent` |
| Escalado | No aplica | `StandardScaler` |
| Codificación | No aplica | `OneHotEncoder` |
| Organización | Selección directa de columnas | `Pipeline` y `ColumnTransformer` |
| División | Ajuste sobre el conjunto disponible | Entrenamiento 80% y prueba 20% |
| Comprobación | Regresión lineal | Regresión logística auxiliar |

## Resultados principales

- El dataset no contiene valores nulos ni filas duplicadas.
- La mediana histórica de esperanza de vida es **60.71 años**.
- La variable objetivo quedó equilibrada: **852 observaciones bajas y 852 altas**.
- El entrenamiento contiene 1,363 filas y la prueba 341.
- El preprocesamiento produce **8 columnas numéricas**: tres escaladas y cinco columnas de continente.
- La regresión logística auxiliar obtuvo **84.5% de accuracy**. Se utiliza únicamente para confirmar que los datos procesados funcionan en un modelo.
- `life_exp` se excluyó de los predictores para evitar fuga de información, porque se utilizó para construir el objetivo.

## Cómo ejecutarlo

```bash
pip install pandas matplotlib scikit-learn jupyter
jupyter notebook Proyecto_9_Preprocesamiento_ML_Gapminder.ipynb
```

El archivo `gapminder_full.csv` debe permanecer en la misma carpeta que el notebook. Al ejecutar todas las celdas se generan las evidencias de la carpeta `figuras`.

## Archivos generados

- `figuras/01_distribucion_objetivo.png`
- `figuras/02_antes_y_despues_escalado.png`
- `figuras/03_matriz_confusion.png`

## Créditos

- Código base: Frank Andrade, repositorio [thepycoach/curso-data-science](https://github.com/thepycoach/curso-data-science), carpeta `11.Machine Learning`.
- Adaptación: José Carlos Hernández Ballado, Equipo B.
