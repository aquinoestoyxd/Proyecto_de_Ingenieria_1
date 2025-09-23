# Informe: Predicción de SO₂ en Alaska mediante Regresión Lineal  

## Introducción  
El dióxido de azufre (SO₂) es un contaminante atmosférico importante que afecta la calidad del aire y la salud pública.  
En este análisis se buscó realizar una predicción de las concentraciones de SO₂ en el estado de Alaska para el año 2024, utilizando como base los registros diarios de los años 2022 y 2023.  
El objetivo fue evaluar la utilidad de un modelo sencillo de regresión lineal para estimar valores futuros y comparar las predicciones con los datos reales de 2024.  

---

## Metodología  

1. **Datos utilizados**:  
   - Series diarias de concentraciones de **SO₂ (Daily Max 1-hour SO₂ Concentration)** de Alaska para los años 2022, 2023 y 2024.  
   - Se filtraron los registros únicamente del estado de Alaska.  

2. **Procesamiento**:  
   - Conversión de las fechas a formato de mes y año.  
   - Cálculo de la **mediana mensual** de las concentraciones de SO₂ para cada mes de 2022 y 2023.  

3. **Modelo aplicado**:  
   - Se utilizó una **regresión lineal simple** tomando como variables de entrada el año y el mes.  
   - Se entrenó con los datos de 2022 y 2023.  
   - Se realizaron predicciones para los 12 meses de 2024.  

4. **Evaluación del modelo**:  
   - Las predicciones se compararon con los valores reales de 2024.  
   - Se calcularon métricas de error:  
     - **MAE (Mean Absolute Error)**: mide el error promedio absoluto.  
     - **RMSE (Root Mean Squared Error)**: penaliza más los errores grandes.  

---

## Resultados  

- El modelo predijo los valores mensuales de SO₂ en 2024 con un **MAE ≈ 3.7 ppb** y un **RMSE ≈ 5.9 ppb**.  
- Los gráficos mostraron una tendencia relativamente cercana entre lo reales y lo predicho, aunque con diferencias notorias en los primeros meses. 
- La predicción funcionó mejor en meses con valores estables, pero presentó desviaciones cuando hubo variaciones abruptas en las mediciones reales.  

---

## Referencias  

- Datos de calidad del aire obtenidos de la **U.S. Environmental Protection Agency (EPA)**:  
  [https://www.epa.gov/outdoor-air-quality-data/download-daily-data](https://www.epa.gov/outdoor-air-quality-data/download-daily-data)  
