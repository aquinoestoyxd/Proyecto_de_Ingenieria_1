# 📊 Informe: Regresión Lineal aplicada al *Healthcare Dataset*

## 1. Objetivo
El propósito de este trabajo fue **adaptar un dataset con variables cualitativas y cuantitativas** para que pueda ser utilizado en un **modelo de regresión lineal**.  
La **variable objetivo (`y`)** seleccionada fue **`Test Results`**, que originalmente es categórica (`Normal`, `Abnormal`, `Inconclusive`).

---

## 2. Preparación de los datos

1. **Carga del dataset**  
   Se utilizó el archivo disponible en GitHub:  


2. **Eliminación de columnas irrelevantes**  
Se descartaron `Name`, `Doctor` y `Hospital` por ser identificadores sin valor predictivo.

3. **Procesamiento de fechas**  
- Se convirtieron `Date of Admission` y `Discharge Date` a formato `datetime`.  
- Se calculó la variable `Stay_Duration` = diferencia en días entre ingreso y alta.  
- Luego se eliminaron las columnas originales de fecha.

4. **Codificación de la variable objetivo**  
Con `LabelEncoder` se transformó `Test Results` en valores numéricos:  

<p align= "center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/code.png?raw=true"/>
</p>
  
5. **Transformación de variables categóricas**  
Se aplicó **One-Hot Encoding** (`pd.get_dummies`) para convertir columnas categóricas en variables binarias (0/1), evitando multicolinealidad con `drop_first=True`.

---

## 3. Graficas de los resultados

<p align= "center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/density.png?raw=true"/>
</p>

<p align= "center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/tabla.png?raw=true"/>
</p>
