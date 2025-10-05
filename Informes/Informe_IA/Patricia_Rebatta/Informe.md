# 📊 Informe – Predicción de niveles de CO en Puerto Rico

## 📌 Introducción  

El presente informe tiene como finalidad analizar la concentración de **monóxido de carbono (CO)** en el aire de **Puerto Rico**, empleando datos históricos de los años **2022 y 2023** para generar un modelo predictivo que se contrasta con las mediciones reales de **2024**.  

El estudio busca evaluar la capacidad de un **modelo de regresión lineal** para anticipar las variaciones **mensuales y semanales** de este contaminante atmosférico, con el propósito de comprender su utilidad en el **monitoreo y la planificación ambiental**.  

---

## ⚙️ Metodología  

### 1. Recopilación de datos  
- Se utilizan datasets de los años **2022, 2023 y 2024**, filtrando exclusivamente los registros correspondientes a **Puerto Rico**.  

### 2. Procesamiento de la información  
- Conversión de fechas a variables temporales (**mes y semana**).  
- Cálculo de la **moda** de la concentración máxima diaria de CO (promedio en intervalos de 8 horas).  

### 3. Construcción del modelo  
- Generación de **variables dummy** para representar meses, semanas y años.  
- Entrenamiento de un modelo de **regresión lineal** con datos de 2022 y 2023.  
- Predicciones realizadas para cada mes y semana del año **2024**.  

### 4. Evaluación del modelo  
- Comparación entre valores **reales y predichos**.  
- Cálculo de métricas de desempeño:  
  - **MAE** (Error Absoluto Medio)  
  - **RMSE** (Raíz del Error Cuadrático Medio)  
  - **R²** (Coeficiente de Determinación)  
- Visualización gráfica de resultados, incluyendo **márgenes de error**.  

---

## 📈 Resultados  

- El modelo logra reflejar **cierta tendencia general** de los niveles de CO en 2024, aunque con **diferencias notables** en determinados meses y semanas.  
- Las métricas de error indican que el modelo tiene un **nivel moderado de precisión**, siendo útil como **aproximación inicial**, pero insuficiente para predicciones altamente confiables.  
- Los gráficos muestran con claridad la **discrepancia entre valores reales y predichos**, permitiendo identificar los periodos con mayor margen de error.  
- Se concluye que el modelo lineal es un **primer paso válido**, pero que sería recomendable explorar **modelos más avanzados** o incorporar **variables adicionales** (clima, tráfico, factores estacionales) para mejorar la calidad de las predicciones.  

---
✍️ *Informe elaborado a partir del análisis de datos en Jupyter Notebook.*  

