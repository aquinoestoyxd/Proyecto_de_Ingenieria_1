***Protocolo de Funcionamiento***

1. **Introducción:**

El presente documento establece el protocolo de acción para el sistema de alerta temprana “AirGuardian”, desarrollado para medir y reportar los niveles de CO2, ruido y confort térmico en los salones de clase. El propósito es brindar instrucciones claras y describir el comportamiento del dispositivo/sistema en cuanto a la detección de condiciones no favorables para los estudiantes en los ambientes de aprendizaje, la comunicación de estas mediante indicadores LED en el sistema físico y mensajes vía WhatsApp y las recomendaciones correctivas que pueden tomar los docentes de forma voluntaria, además de brindar una fuente de datos útil para el personal responsable (área administrativa y mantenimiento).

2. **Objetivo y alcance**

**2.1. Objetivo**

El objetivo principal de este Protocolo es definir las pautas de operación y respuesta para el sistema de alerta temprana "AirGuardian". En particular, busca:

- Establecer los límites críticos de Dióxido de Carbono (CO2), Confort Térmico (Humedad Relativa y Temperatura) y Ruido Ambiental, que afectan la salud, el bienestar y la capacidad de razonamiento de los universitarios.  
- Garantizar que las acciones correctivas sean trazables y estandarizadas, distinguiendo entre las responsabilidades de respuesta inmediata (que corresponden a los docentes) y las de solución de infraestructura (que pertenecen al personal administrativo o de mantenimiento).  
- Asegurar la continuidad de la educación mitigando de forma rápida las condiciones ambientales negativas y evitando que se repitan en horarios futuros a través del aviso proactivo.

**2.2. Alcance**

Este protocolo es aplicable a todas las áreas cerradas de la Universidad Peruana Cayetano Heredia (UPCH), incluyendo los laboratorios y las aulas, que tengan el equipo "AirGuardian" para supervisar el ambiente. El protocolo busca regular el comportamiento del personal docente durante las clases mediante recomendaciones y del personal administrativo (Mantenimiento e Infraestructura) en la administración y rectificación de las irregularidades que el sistema identifica.

3. **Umbrales operacionales**

El protocolo define tres niveles de funcionamiento para cada parámetro, los cuales están en consonancia con la concentración y el rendimiento cognitivo:

| Indicador LED | Rango Operacional (R) |
| ----- | ----- |
| **Verde \- 🟢** | **R1 (Óptimo):** Condiciones ideales, sin riesgo. |
| **Azul \- 🔵** | **R2 (Atención):** Condiciones fuera del óptimo, pero manejables. |
| **Rojo \-  🔴** | **R3 (Crítico):** Nivel de riesgo que exige acción inmediata. |

Se establece los rangos para cada parámetro:

| Parámetro | Rango (R1) Óptimo \- 🟢 | Rango (R2) Atención \- 🔵 | Rango (R3) Alerta/Crítico \- 🔴 |
| ----- | ----- | ----- | ----- |
| **Dióxido de Carbono (CO₂)** | **\< 800 ppm** (Ventilación adecuada) | **800 – 1000 ppm** (Ventilación insuficiente) | **\> 1000 ppm** (Requiere acción inmediata) |
| **Ruido Ambiental** | **\< 35 dB(A)** (Inteligibilidad óptima) | **35 – 50 dB(A)** (Distracción potencial) | **\> 50 dB(A)** (Molestia crítica/Excede ECA) |
| **Temperatura (°C)** | **22 – 24 °C** (Rango de confort) | **20 – 21.9 °C o 24.1 – 26 °C** (Fuera del óptimo) | **\< 20 °C o \> 26 °C** (Riesgo de estrés térmico) |
| **Humedad Relativa (HR)** | **40% – 60%** (Confort y control de aerosoles) | **30% – 39% o 61% – 70%** | **\< 30% o \> 70%**(Riesgo de disconfort) |

Especialmente para el R3, crítico, se establecen las siguiente matriz de consecuencias:

### 

| Parámetro | Umbral Crítico (R3: 🔴) | Consecuencia Principal en la Concentración |
| :---- | :---- | :---- |
| **Dióxido de Carbono**  | **\> 1000 ppm** | Somnolencia, reducción de la toma de decisiones y atención. |
| **Ruido Ambiental** | **\> 50 dB(A)** | Estrés, interferencia con la comunicación y pérdida de foco. |
| **Temperatura** | **\< 20 °C o \> 26 °C** | Disconfort físico, estrés térmico, y desvío de recursos cognitivos. |
| **Humedad Relativa (HR)** | **\< 30% o \> 70%** | Sequedad o sensación de agobio, afectando el confort térmico general. |

4. **Flujo de protocolo de alerta y acción** 

Este flujo se activa cuando el Dashboard del software clasifica los datos registrados por los sensores en las categorías R2 (Atención) o R3 (Crítico), según los umbrales definidos para cada variable monitoreada. Cabe destacar que se establecen las recomendaciones  dirigidas a los docentes que decidan actuar de forma voluntaria ante situaciones de alerta ambiental, además de servir como herramienta de apoyo en la toma de decisiones para el área administrativa.

### **4.1. Detección y Generación de Alerta (Dashboard)**

1. **Detección (aparato físico):** Los sensores realizan lecturas continuas de ruido, temperatura, humedad y CO2 en el ambiente cerrado. Luego envía los datos recopilados a una base de datos cada dependiendo del parámetro.  
   * CO2: 1- 5 minutos   
   * Ruido: 2  minutos  
   * Temperatura y Humedad Relativa:30 \- 60 segundos  
2. **Clasificación (Dashboard):** El sistema analiza la información recopilada y clasifica los niveles registrados. Posteriormente se comparan con los umbrales operacionales establecidos.  
     
3. **Disparo de Alerta:**  
- **R2 (Atención):** El sistema activa el Indicador de Estado en amarillo. Genera un registro de advertencia en el dashboard.  
- **R3 (Alerta/Crítico):** El sistema activa el Indicador de Estado en rojo, dispara la señal visual de funcionamiento y envía un mensaje vía WhatsApp al Docente con recomendaciones y al área de Mantenimiento.

**4.2. Protocolo de recomendaciones correctivas**

El docente presente en el aula de clases recibirá un mensaje mediante Whatsapp, en el cual se encontrarán recomendaciones para que pueda tomar acción de forma voluntaria a su alcance y pueda contribuir en la mejora de la calidad en el rendimiento académico de sus estudiantes. Además, enviará también recomendaciones al área administrativa para que pueda tomar acción.

| Parámetro en R2 o R3 | Recomendación Correctiva Inmediata (Docente/Usuario) | Recomendación de acción Correctiva Mayor (Mantenimiento/Infraestructura) |
| :---- | :---- | :---- |
| **CO₂** | **1\. Ventilación:** Abrir las puertas y ventanas de forma inmediata.  **2\. Pausa:** Si es posible, haga una breve pausa o una actividad dinámica fuera del salón de clases hasta que el indicador regrese a R1 (dentro de lo posible). | **1\. Inspección:** Revisar filtros y conductos del sistema de ventilación mecánica. **2\. Ajuste:** Calibrar el sistema HVAC (Calefacción, Ventilación y Aire Acondicionado) para asegurar un caudal de aire fresco adecuado según la ocupación. |
| **Ruido**  | 1\. **Identificación:** Identificar la fuente de ruido (ej. tránsito, obra, actividad interna).  2\. **Mitigación:** Si es interno, solicitar silencio y reubicar la actividad. Si es externo, cerrar puertas y ventanas. | 1\. **Evaluación Formal:** Programar una medición oficial con un sonómetro certificado (Clase 1 o 2\) para el área.  2\. **Aislamiento:** Implementar medidas de aislamiento acústico (ej. sellos en ventanas y puertas, barreras acústicas). |
| **Temperatura**  | 1\. **Ajuste:** Encender o apagar el aire acondicionado/calefacción.  2\. **Sombra/Luz:**Ajustar cortinas o persianas para controlar la ganancia solar. | 1\. **Mantenimiento:** Verificar el correcto funcionamiento y calibración de termostatos y unidades de aire acondicionado.   |
| **Humedad Relativa** | 1\. **Ventilación:** Mejorar la ventilación para reducir la humedad excesiva (si es \> 70%).  2\. **Dispositivo:** Si hay un deshumidificador/humidificador portátil, activarlo. | 1\. **Verificación:** Revisar el sistema de control de humedad del edificio (si lo tuviera).  2\. **Sellado:** Identificar y reparar filtraciones o fuentes de humedad no deseadas. |

#### **4.3. Plantilla de Mensajes Detallada (WhatsApp)**

Estos mensajes se envían inmediatamente después de que el sistema "AirGuardian" detecta que un parámetro ha permanecido en nivel R3 (Crítico) por un período sostenido (ej. 10 minutos), indicando que la acción del docente en el horario anterior fue insuficiente o que el problema es de infraestructura.

#### A. DIÓXIDO DE CARBONO (Alerta Crítica)

- Mensaje al Personal Administrativo/Mantenimiento:

"ALARMA *AIRGUARDIAN*: SOLICITUD DE ANÁLISIS Y ADECUACIÓN INMEDIATA. **Aula/Lab \[...\]** registró niveles críticos de Dióxido de Carbono \> 1000 ppm entre **\[Hora Inicio\]** y **\[Hora Fin\].** La data ha sido enviada automáticamente al Dashboard para su análisis. 

ACCIÓN REQUERIDA URGENTE: Analizar el registro para determinar la causa probable (Ej: falla en el caudal de aire o filtros). Ejecutar la adecuación necesaria (Ej: verificar la ventilación mecánica) antes de la clase de las **\[Hora de inicio de la siguiente clase\]** para garantizar un ambiente óptimo. 

Posibles consecuencias de no tomar acción: Reducción en la atención y somnolencia."

- Mensaje al Docente Próximo (Horario N+1 \- Aviso de Intervención):

" AVISO IMPORTANTE *AIRGUARDIAN*: ADECUACIÓN POR DIÓXIDO DE CARBONO ALTO. Prof. **\[Nombre del Docente Próximo\]**, se le informa que el **Aula/Lab \[X\]** presentó Dióxido de Carbono alto en el horario anterior. 

ACCIÓN TOMADA: Solicitamos la intervención inmediata de Mantenimiento para Mejorar la Ventilación. 

SU ACCIÓN (Monitoreo): Al iniciar su clase, si el indicador sigue en Rojo (Crítico) y no nota cambios en la ventilación, **NOTIFIQUE AL PERSONAL ADMINISTRATIVO** (Anexo **\[Número\]**) para una segunda intervención."

#### B. RUIDO AMBIENTAL (Alerta Crítica)

- Mensaje al Personal Administrativo/Mantenimiento:

"ALARMA *AIRGUARDIAN*: SOLICITUD DE ANÁLISIS Y ADECUACIÓN INMEDIATA. **Aula/Lab \[X\]** registró niveles críticos de Ruido Ambiental \>50 dB(A) entre **\[Hora Inicio\]** y **\[Hora Fin\]**. La data ha sido enviada automáticamente al Dashboard para su análisis. 

ACCIÓN REQUERIDA URGENTE: Analizar el registro para identificar la fuente persistente del ruido (Ej: obra, equipos ruidosos cercanos). Ejecutar la adecuación necesaria (Ej: verificar el sellado de ventanas o aislar la fuente) antes de la clase de las **\[Hora de inicio de la siguiente clase\]**. 

Impacto:Estrés e interferencia con el aprendizaje."

- Mensaje al Docente Próximo (Horario N+1 \- Aviso de Intervención):

"AVISO IMPORTANTE *AIR GUARDIAN*: ADECUACIÓN POR RUIDO AMBIENTAL ALTO. Prof. **\[Nombre del Docente Próximo\]**, se le informa que el **Aula/Lab \[X\]** presentó Ruido Ambiental alto en el horario anterior. 

ACCIÓN TOMADA: Solicitamos la intervención inmediata de Mantenimiento para Revisar el Aislamiento Acústico. 

SU ACCIÓN (Monitoreo): Al iniciar su clase, si el indicador sigue en Rojo (Crítico) debido a una fuente de ruido, **NOTIFIQUE AL PERSONAL ADMINISTRATIVO** (Anexo **\[Número\]**) para una segunda intervención."

#### C. TEMPERATURA (Alerta Crítica)

- Mensaje al Personal Administrativo/Mantenimiento:

"ALARMA *AIR GUARDIAN*: SOLICITUD DE ANÁLISIS Y ADECUACIÓN INMEDIATA. **Aula/Lab \[X\]** registró niveles críticos de Temperatura \<20 °C ó \>26 °C entre **\[Hora Inicio\]** y **\[Hora Fin\]**. La data ha sido enviada automáticamente al Dashboard para su análisis. ACCIÓN REQUERIDA URGENTE: Analizar el registro para determinar la causa (Ej: falla en el termostato, conductos del Aire Acondicionado, o alta ganancia solar). Ejecutar la adecuación necesaria (Ej: verificar el funcionamiento del Aire Acondicionado/calefacción) antes de la clase de las **\[Hora de inicio de la siguiente clase\]**. 

Impacto: Disconfort físico y desvío de la concentración."

- Mensaje al Docente Próximo (Horario N+1 \- Aviso de Intervención):

"AVISO IMPORTANTE *AIRGUARDIAN*: ADECUACIÓN POR TEMPERATURA EXTREMA. Prof. **\[Nombre del Docente Próximo\]**, se le informa que el **Aula/Lab \[X\]** presentó Temperatura fuera de rango en el horario anterior. 

ACCIÓN TOMADA: Solicitamos la intervención inmediata de Mantenimiento para Revisar el equipo de Aire Acondicionado/Calefacción. 

SU ACCIÓN (Monitoreo): Al iniciar su clase, si el indicador sigue en Rojo (Crítico) y la temperatura no es confortable, **NOTIFIQUE AL PERSONAL ADMINISTRATIVO** (Anexo **\[Número\]**) para una segunda intervención."

#### D. HUMEDAD RELATIVA (Alerta Crítica)

- Mensaje al Personal Administrativo/Mantenimiento:

"ALARMA *AIRGUARDIAN*: SOLICITUD DE ANÁLISIS Y ADECUACIÓN INMEDIATA. **Aula/Lab \[X\]** registró niveles críticos de Humedad Relativa \<30% ó \>70% entre **\[Hora Inicio\]** y **\[Hora Fin\]**. La data ha sido enviada automáticamente al Dashboard para su análisis. 

ACCIÓN REQUERIDA URGENTE: Analizar el registro para identificar la causa (Ej: filtraciones o ventilación insuficiente). Ejecutar la adecuación necesaria (Ej: verificar el sistema de control de humedad del edificio o sellar filtraciones) antes de la clase de las **\[Hora de inicio de la siguiente clase\]**. 

Impacto: Agravamiento del disconfort térmico general."

- Mensaje al Docente Próximo (Horario N+1 \- Aviso de Intervención):

"AVISO IMPORTANTE *AIR GUARDIAN*: ADECUACIÓN POR HUMEDAD RELATIVA FUERA DE RANGO. Prof. **\[Nombre del Docente Próximo\]**, se le informa que el **Aula/Lab \[X\]** presentó Humedad Relativa extrema en el horario anterior. 

ACCIÓN TOMADA: Solicitamos la intervención inmediata de mantenimiento para revisar el control de humedad. 

SU ACCIÓN (Monitoreo): Al iniciar su clase, si el indicador sigue en Rojo (Crítico), **NOTIFIQUE AL PERSONAL ADMINISTRATIVO** (Anexo **\[Número\]**) para una segunda intervención."

Leyenda:

* **\[...\]**: Representa el identificador del Aula/Lab (ej. número o nombre específico).  
* **\[Hora Inicio\]**: Hora de inicio del período crítico.  
* **\[Hora Fin\]**: Hora de fin del período crítico.  
* **\[Hora de inicio de la siguiente clase\]**: Hora de la próxima clase.  
* **\[Nombre del Docente Próximo\]**: Nombre del docente del siguiente horario.  
* **\[Número\]**: Número de anexo o contacto administrativo.  
* **\[X\]**: Parte del Aula/Lab, posiblemente un código o número (ej. Aula/Lab **\[X\]**).

