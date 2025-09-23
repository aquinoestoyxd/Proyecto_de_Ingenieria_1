# Informe de Análisis: Predicción de PM2.5 Mensual en Adrian, Michigan (2022-2024) 🌬️

<div align="center">
  <img src="./images/comparacion_pm25.png" alt="Gráfico de Comparación PM2.5 Real vs. Predicho" width="600">
  <h1>Predicción del PM2.5 Mensual mediante Regresión Lineal</h1>
  <p><strong>Autor:</strong> Sendy Rodríguez | <strong>Estación:</strong> Adrian, Michigan | <strong>Fecha:</strong> 22 de septiembre de 2025</p>
</div>

## 📋 Resumen Ejecutivo

Este informe presenta un análisis de los niveles mensuales de **materia particulada fina (PM2.5)** en Adrian, Michigan, para los años 2022-2024, utilizando un modelo de **regresión lineal simple**. El objetivo fue predecir los valores de PM2.5 para 2024 basándose en datos históricos de 2022-2023, empleando variables dummy para años y meses. Los datos provienen de la base de datos [EPA AirData](https://aqs.epa.gov/aqsweb/airdata/download_files.html). 

**Hallazgos clave**:
- El modelo muestra un rendimiento deficiente, con un **R² negativo (-4.0383)**, indicando que no captura la variabilidad de los datos.
- Los errores promedio (MAE: 2.8519, RMSE: 3.7198) son significativos en la escala de PM2.5 (~3-8 μg/m³).
- La relación entre PM2.5 y las variables temporales (año/mes) no es adecuada para un modelo lineal simple.

**Recomendaciones**: Explorar modelos de series temporales (ARIMA, SARIMA) e incorporar variables externas como datos meteorológicos.

---

## 🎯 Objetivos del Análisis

1. **Predecir PM2.5 Mensual**: Estimar los niveles promedio mensuales de PM2.5 para 2024 en Adrian, Michigan.
2. **Evaluar el Modelo**: Analizar el desempeño de la regresión lineal mediante métricas (MAE, RMSE, R²).
3. **Identificar Limitaciones**: Proponer mejoras basadas en los resultados.

---

## 🛠️ Metodología

### 1. **Carga y Preprocesamiento de Datos**
- **Datos**: Archivos CSV de PM2.5 diarios (2022-2024) de la estación de Adrian, Michigan.
- **Preprocesamiento**:
  - Combinación de CSVs de 2022-2023 (entrenamiento) y 2024 (prueba).
  - Eliminación de valores faltantes (NaN).
  - Creación de variables dummy para años (2022, 2023) y meses (1-12).
- **Tamaño del Conjunto**: 
  - Entrenamiento: 24 muestras (12 meses x 2 años).
  - Features: 14 (2 años + 12 meses).

### 2. **Construcción del Modelo**
- **Modelo**: Regresión lineal simple (Scikit-learn).
- **Variables**:
  - Independientes (X): Dummies de año y mes.
  - Dependiente (Y): Promedio mensual de PM2.5 (μg/m³).
- **Entrenamiento**: Usando datos de 2022-2023.

### 3. **Evaluación y Visualización**
- Predicciones generadas para los 12 meses de 2024.
- Métricas calculadas: MAE, RMSE, R².
- Visualización: Gráfico de barras comparando PM2.5 real vs. predicho con barras de error.

---

## 📊 Resultados

### Comparación Real vs. Predicho (2024)
La siguiente tabla muestra los valores reales y predichos de PM2.5 para cada mes de 2024:

| Mes | PM2.5 Real (μg/m³) | PM2.5 Predicho (μg/m³) | Diferencia |
|-----|--------------------|------------------------|------------|
| 1   | 3.8                | 5.40                   | -1.60      |
| 2   | 4.3                | 7.85                   | -3.55      |
| 3   | 4.2                | 5.60                   | -1.40      |
| 4   | 2.9                | 4.60                   | -1.70      |
| 5   | 3.6                | 2.80                   | 0.80       |
| 6   | 3.1                | 8.05                   | -4.95      |
| 7   | 6.5                | 4.95                   | 1.55       |
| 8   | 4.3                | 5.45                   | -1.15      |
| 9   | 6.5                | 3.65                   | 2.85       |
| 10  | 4.9                | 4.80                   | 0.10       |
| 11  | 2.4                | 3.90                   | -1.50      |
| 12  | 8.1                | 5.60                   | 2.50       |

### Métricas de Desempeño
| Métrica                          | Valor   | Interpretación                              |
|----------------------------------|---------|---------------------------------------------|
| **MAE (Error Absoluto Medio)**   | 2.8519  | Error promedio de ~2.85 μg/m³ por mes.      |
| **RMSE (Raíz del Error Cuadrático Medio)** | 3.7198 | Indica dispersión significativa en errores.  |
| **R² (Coeficiente de Determinación)** | -4.0383 | Negativo: modelo peor que la media simple. |

### Visualización
![Gráfico de Comparación PM2.5 Real vs. Predicho](./images/comparacion_pm25.png)  
*Figura 1: Barras de PM2.5 real (azul) vs. predicho (naranja) para 2024, con barras de error mostrando discrepancias significativas.*

---

## 🔍 Análisis e Insights

- **Bajo Rendimiento del Modelo**: El R² negativo (-4.0383) indica que la regresión lineal no captura la variabilidad de PM2.5. Esto sugiere que la relación entre año/mes y PM2.5 no es lineal o que faltan factores clave.
- **Errores Significativos**: El MAE (~2.85 μg/m³) y RMSE (~3.72 μg/m³) son altos en comparación con la escala de PM2.5 (2.4-8.1 μg/m³), representando errores del 30-50% en algunos meses.
- **Limitaciones**:
  - Pocos datos de entrenamiento (24 muestras para 14 features), lo que puede causar underfitting.
  - No se consideraron variables externas (e.g., temperatura, humedad, incendios forestales).
  - Falta de análisis de estacionalidad (e.g., PM2.5 podría ser más alto en invierno por calefacción).
- **Fortalezas**: La simplicidad del modelo permite una rápida implementación, pero no es adecuada para este caso.

---

## 🚀 Próximos Pasos

1. **Modelos Alternativos**:
   - Implementar modelos de series temporales como **ARIMA** o **SARIMA** para capturar patrones estacionales.
   - Probar modelos no lineales como **Random Forest** o **Gradient Boosting**.
2. **Incluir Variables Externas**:
   - Integrar datos meteorológicos (NOAA) como temperatura, humedad y viento.
   - Considerar eventos externos (e.g., incendios forestales, tráfico).
3. **Análisis Exploratorio**:
   - Realizar un EDA completo: histogramas, boxplots por mes, análisis de correlación.
   - Identificar patrones estacionales (e.g., `sns.boxplot(x='Month', y='PM25', data=df)`).
4. **Validación Robusta**:
   - Usar validación cruzada temporal (`TimeSeriesSplit` en Scikit-learn).
   - Validar con más datos de 2024 si están disponibles.
5. **Mejorar Visualizaciones**:
   - Exportar gráficos en alta resolución a `./images/`.
   - Agregar gráficos de series temporales para mostrar tendencias.

---

## 📚 Código y Reproducibilidad

El análisis completo está en el notebook: [Sendy.ipynb](../Sendy.ipynb). Para reproducir:

1. **Clona el Repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/Informe_IA2.git
   cd Informe_IA2/Sendy\ Rodriguez
   ```

2. **Instala Dependencias**:
   ```bash
   pip install -r ../../requirements.txt
   ```
   Contenido de `requirements.txt`:
   ```
   pandas
   numpy
   scikit-learn
   matplotlib
   ```

3. **Descarga Datos**:
   - Obtén CSVs de PM2.5 (2022-2024) desde [EPA AirData](https://aqs.epa.gov/aqsweb/airdata/download_files.html).
   - Colócalos en `Informe_IA2/data/`.

4. **Ejecuta el Notebook**:
   ```bash
   jupyter notebook Sendy.ipynb
   ```

---

## 📌 Conclusiones

El modelo de regresión lineal simple no es adecuado para predecir PM2.5 mensual en Adrian, Michigan, debido a su incapacidad para modelar relaciones no lineales y patrones temporales. El R² negativo y los errores altos destacan la necesidad de enfoques más avanzados. Los próximos pasos deben centrarse en modelos de series temporales y la inclusión de variables meteorológicas para mejorar la precisión.

**Contribuciones**: ¡Abre un issue o PR en el repositorio para sugerencias!  
**Contacto**: [Tu correo o enlace a GitHub]  
**Fecha**: 22 de septiembre de 2025
