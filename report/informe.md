 Informe del Proyecto: Predicción del Rendimiento Académico de Estudiantes

1. Introducción

Este proyecto tiene como objetivo desarrollar un modelo de regresión lineal múltiple para predecir el rendimiento final (nota G3) de estudiantes de secundaria, utilizando variables demográficas, sociales, académicas y familiares. Se utilizó el dataset "Student Performance" del UCI Machine Learning Repository.

2. Descripción del Dataset

Fuente: UCI Machine Learning Repository

Nombre: Student Performance

Filas: 649

Columnas: 33

Target: G3 (nota final de los estudiantes, de 0 a 20)

Formato: CSV con separador ;

3. Análisis Exploratorio de Datos (EDA)

Se revisaron valores nulos y tipos de datos. No se encontraron datos faltantes.

Se realizó un histograma de la variable G3:

La mayoría de estudiantes tiene calificaciones entre 10 y 15.

Correlaciones:

G1 y G2 (notas anteriores) tienen alta correlación con G3.

El consumo de alcohol (Dalc, Walc) y el tiempo de estudio también mostraron correlaciones moderadas.

4. Preprocesamiento de Datos

Se codificaron las variables categóricas usando one-hot encoding.

Se separaron variables predictoras (X) y la variable objetivo (y = G3).

Se dividió el dataset en conjuntos de entrenamiento (80%) y prueba (20%).

Se aplicó escalado estándar a las variables predictoras.

5. Modelo de Regresión Lineal

Se utilizó la clase LinearRegression de Scikit-learn.

El modelo fue entrenado con los datos normalizados.

Evaluación del modelo:

Métrica

Valor

R²

~0.84

MAE

~1.85

RMSE

~2.36

6. Visualización de Resultados

Se generó un scatter plot de valores reales (G3) vs predichos:

Se observa una alineación general con algunos errores comunes en valores extremos.

Se generaron gráficos de:

Histograma de G3

Mapa de calor de correlación con G3

7. Importancia de las Variables Predictoras

Las notas previas G1 y G2 fueron las más relevantes.

Factores como tiempo de estudio, apoyo familiar (schoolsup), y consumo de alcohol también influyeron moderadamente.

8. Conclusiones

Es posible predecir con buena precisión el rendimiento final de los estudiantes utilizando un modelo de regresión lineal.

Las calificaciones anteriores son fuertes indicadores del rendimiento futuro.

Las variables sociales y de estilo de vida también aportan información valiosa.

9. Recomendaciones

Probar modelos más complejos como Random Forest o XGBoost.

Considerar ingeniería de características para mejorar la calidad del modelo.

Evaluar modelos separados por género, escuela u otros segmentos.

10. Archivos Entregables

src/: Código fuente

data/student-por.csv: Dataset original

output/*.png: Visualizaciones generadas

report/informe.md: Este informe

README.md: Instrucciones del repositorio

11. Referencias

UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/320/student+performance

Autores: 
- Martínez Chávez Cristofer Benjamín
- Quispe Yauri Rosario Lizeth
- Rodríguez Galindo Rogelio Armando
Fecha de entrega: 22 de julio de 2025
