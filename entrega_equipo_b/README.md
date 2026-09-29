# Laboratorio práctico 2.1 de Ciencia de Datos

Equipo B, proyectos 7, 8 y 9. Se usa Gapminder World para enlazar visualización, análisis estadístico y preprocesamiento. Dataset: 1,704 observaciones, 142 países, registros entre 1952 y 2007.

## Qué contiene la entrega

| Carpeta o archivo | Contenido |
| --- | --- |
| Proyecto7_Visualizacion/ | Notebook ejecutado, dataset, figuras, XLSX y gráfico interactivo HTML |
| Proyecto_8_Visualizacion_Estadistica_Seaborn/ | Notebook ejecutado, dataset y cinco figuras |
| Proyecto_9_Gapminder/ | Notebook ejecutado, dataset y tres figuras |
| evidencia_otros_nueve/ | Notebook ejecutado con ejercicios propios basados en los temas 1 a 6 y 10 a 12 de la consigna |
| Reporte_Proyectos_7_8_9_Equipo_B.pdf | Resultados de los proyectos asignados |
| Reporte_Otros_9_Temas_Equipo_B.pdf | Evidencia resumida de los temas complementarios |
| Presentacion_Equipo_B_Gapminder.pdf | Presentación para exponer |
| Presentacion_Equipo_B_Gapminder.pptx | Versión editable de la presentación |

Los dos reportes también incluyen versiones editables DOCX. Cada proyecto tiene un README individual.

## Cómo reproducir las prácticas

Abre cada notebook en Google Colab. Carga el archivo gapminder_full.csv de la misma carpeta en el panel Archivos de Colab y selecciona Entorno de ejecución > Ejecutar todo. Colab borra los archivos temporales cuando se desconecta, por lo que quizá debas volver a cargar el CSV.

El notebook evidencia_otros_nueve/Evidencia_otros_9_temas.ipynb busca gapminder_full.csv en la carpeta raíz del proyecto o en /content/. Para ejecutarlo en Colab, sube el CSV que está en la raíz.

Dependencias principales: pandas, numpy, matplotlib, seaborn, plotly, scikit-learn, openpyxl y, para extraer tablas HTML locales, lxml.

## Resultados principales

- Proyecto 7: evolución de esperanza de vida de cinco países latinoamericanos y relación con el PIB en 2007.
- Proyecto 8: distribuciones y correlación entre esperanza de vida y PIB por habitante de alrededor de 0.58 en todo el dataset.
- Proyecto 9: 852 registros de cada clase, ocho entradas transformadas y exactitud de 84.5 % en una regresión logística auxiliar.
- Ejercicios complementarios: diez celdas de código ejecutadas sin errores. El árbol de decisión afinado obtuvo aproximadamente 0.880 de exactitud sobre 341 registros de prueba.

## Alcance de la evidencia adicional

Los nueve ejercicios complementarios siguen los temas que enumera el PDF del profesor, pero son implementaciones propias para este laboratorio. El ejercicio de extracción usa una página HTML creada localmente; no demuestra descarga de una página web en vivo. Este material no acredita por sí solo que el equipo haya replicado y ejecutado los nueve notebooks originales del curso.

## Fuentes

- Código base del curso: https://github.com/thepycoach/curso-data-science
- Dataset Gapminder: https://www.kaggle.com/datasets/tklimonova/gapminder-datacamp-2007
- Consigna: CD 2.1 Laboratorio Práctico, Fernando Mayorga Guittins.
