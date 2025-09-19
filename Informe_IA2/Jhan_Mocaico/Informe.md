# 🌍Regresión Lineal (PM10)

## 📌 Descripción
Este proyecto analiza datos de calidad del aire, específicamente la concentración de **material particulado PM10** (partículas menores a 10 micras), a partir de registros diarios en diferentes estaciones de monitoreo.  

El objetivo es **modelar y predecir los valores de PM10** usando **regresión lineal**, evaluando qué tan bien el modelo se ajusta a los datos observados.  

---

## ⚙️ Proceso del Proyecto
1. **Carga de datos:** Se utilizó el dataset de concentración de PM10 correspondientes a los años 2023, 2024 y 2025 en Alabama, Estados Unidos.  
2. **Preprocesamiento:**  
   - Limpieza de valores faltantes y datos atípicos.  
   - Selección de columnas relevantes (`Date`, `Daily Mean PM10 Concentration`, `Local Site Name`, etc.).  
3. **Construcción del modelo:**  
   - Algoritmo utilizado: **Regresión Lineal**.  
   - División en conjuntos de **entrenamiento y prueba**.  
4. **Evaluación del modelo:**  
   Se calcularon métricas de desempeño:  
   - **MAE (Error Absoluto Medio):** mide el error promedio en las predicciones.  
   - **RMSE (Raíz del Error Cuadrático Medio):** penaliza más los errores grandes.  

---

## 📈 Resultados
- El modelo logró predecir los valores de **PM10** con un nivel de error cuantificado en las métricas anteriores.  
- Las gráficas de líneas muestran la comparación entre **valores reales vs. predichos**.  
- Las barras de error absoluto permiten identificar los meses con mayor discrepancia.
  
### 🔹 Métricas Globales
- **MAE = 6 µg/m³**  
- **RMSE = 7.25 µg/m³**  

### 🔹 Interpretación
- El **MAE** indica que, en promedio, el modelo se equivoca en **6 µg/m³** respecto a los valores reales de PM10.  
- El **RMSE** es ligeramente mayor porque penaliza más los errores grandes. Su valor de **7.25 µg/m³** significa que, en promedio, la desviación entre lo real y lo predicho es de ese orden.

👉 En términos prácticos:  
- Si el límite recomendado de PM10 en 24h es **50 µg/m³**, un error de **7.25 µg/m³** representa alrededor del **14%** del límite.  
- Esto indica que la **regresión lineal funciona como un modelo base aceptable**, aunque puede mejorarse con algoritmos más avanzados (Random Forest, XGBoost, Redes Neuronales).  

> 📊 Los valores numéricos de MAE, RMSE y RMSD se encuentran calculados en el notebook y exportados en la carpeta `results/`.  

---
                 # Documentación del proyecto

