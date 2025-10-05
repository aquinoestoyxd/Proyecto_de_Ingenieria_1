# Regresión lineal para hallar cantidad promedio de NO2 mensual en Florida

## Introducción

El presente proyecto se realizó con el propósito de demostrar la posibilidad de predecir los valores del promedio de concentración de NO2 mensual en Florida (USA).

Para cumplir con dicha finalidad, se estará empleando el método de Regresión Lineal e intentaremos definir si resulta efectivo o no.

---

## Metodología

Como se mencionó anteriormente, se estará empleando el método de Regresión Lineal para predecir los nuevos valores, y para saber si nuestro modelo de Machine Learning resulta efectivo, estaremos comparando los datos predichos con los datos reales del año 2025.

El procedimiento realizado ha sido el siguiente:

1.- Lectura de los datasets de los años 2023 y 2024.

2.- Cración de un nuevo archivo csv, conteniendo el promedio mensual de los datasets. Contrario a los archivos originales que poseen múltiples columnas con características variadas, para este nuevo csv se tendrán un total de 16: La primera indica el promedio de concentración de NO2 mensual, la segunda, tercera y cuarta son dedicadas para cada año (2023, 2024 y 2025), y el resto se destina a cada mes. Tanto las tablas de mes, como las de año, reciben valores de 0 y 1, donde 1 simboliza que el valor pertenece a dicho mes/año, y 0 que no es así.

3.-Se realiza el entrenamiento basándonos en los promedios mensuales obtenidos de cada mes de los años 2023 y 2024, teniendo como target la columna NO2 concentration. También se realiza el proceso de predicción.

4.- A fin de poder realizar una comparativa entre los valores predichos y valores reales, se crea un archivo csv que almacene los datos predichos por el sistema para los primeros 8 meses del año 2025, y se realiza una comparativa con los datos reales, los cuales se observan en el siguiente gráfico:

<p align="center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/NO2%20gr%C3%A1fico.PNG"/>
</p>

5.- Para tener una mayor facilidad de obtener los valores predichos para cada mes del año 2025, se crea la función consultar_mes, la cual permite al usuario ingresar un número del 1 al 12 (correspondiente a cada mes del año) y a partir del valor ingresado se presentan el valor predicho y el valor real. En caso de no existir un dato real para algún mes (del mes 9 en adelante), se imprimirá el valor predicha con la mención de que no hay dato real para su comparación.

<p align="center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/Consultar_mes.PNG"/>
</p>

6.- Finalmente, se realizan cálculos de MAE, MSE, RMSE y R2 para evaluar el desempeño de nuestro modelo.

<p align="center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/M%C3%A9tricas.PNG"/>
</p>

---

## Resultados

La evaluación del desempeño de nuestro modelos nos dio a conocer lo siguiente:

- MAE: 1.86. Esto demuestra que el error promedio entre los valores predichos y reales no es tanto.
- MSE: 4.9. Similar a la métrica anterior, el resultado indica que el promedio de errores al cuadrado cometidos no es tan excesivo y se encuentra en un rango adecuado.
- RMSE: 2.21. Muestra el error cometido por la máquina, pero esta vez, en la unidad de la variable de estudio. Nuevamente, es una cifra pequeña que indican un buen desempeño.
- R2: 0.73. Esta métrica mide el porcentaje de la variabilidad de los datos reales que interpreta el modelo. Un dato inferior o cercano a 0 indica un mal resultado, no obstante, el nuestro se encuentra más cercano a 1, lo que es un resultado positivo.

En conjunto a ello, en los datos ilustrados en el gráfico de comparación, se observa que, exceptuando los meses 3 y 7, los datos predichos se encuentran muy cerca de los valores reales. Esto demuestra que el modelo de regresión lineal ha resultado bastante útil y efectivo para la predicción de nuevos datos, sin embargo, se pueden obtener resultados aún mejores, por ejemplo, mediante el uso de un promedio semanal en lugar de uno mensual, ya que así el entrenamiento es mayor.

---

## Referencias
Datasets obtenidos de:
U.S. Environmental Protection Agency, “Download Daily Data” Outdoor Air Quality Data, EPA. [Online]. https://www.epa.gov/outdoor-air-quality-data/download-daily-data

