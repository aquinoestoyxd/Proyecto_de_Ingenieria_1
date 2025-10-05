### 📌  Informe SIMSCALE
Este proyecto corresponde a un análisis estructural estático realizado en SimScale
El objetivo fue evaluar la distribución de tensiones en un componente mecánico sometido a cargas externas, verificando la resistencia del material y posibles zonas críticas de esfuerzo.
El análisis se llevó a cabo utilizando el criterio de Von Mises Stress, con el fin de determinar si el diseño cumple con los requisitos de seguridad estructural.

### ⚙️ Metodología
-Tipo de análisis:
Análisis estructural estático lineal.

-Condiciones de contorno:
Se aplicó una fuerzas externa de 100N en la zona frontal del componente.
El cuerpo principal fue restringido para evitar movimientos rígidos.

-Mallado:
Mallado automático con refinamiento local en áreas críticas.


Materiales:
Se utilizó el material PLA

### 📊 Resultados
El diseño soporta las cargas aplicadas sin superar los límites elásticos esperados del material.
Se identificaron zonas críticas donde se concentran esfuerzos, lo que puede servir como base para refinamiento de diseño (redondeo de aristas, incremento de sección, o cambio de material). Las zonas con mayor concentración de esfuerzos se encuentran en las regiones de contacto y transición geométrica.

<p align= "center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/simscale_jhan.jpeg?raw=true" alt="800px" width="800px"/>
</p>
