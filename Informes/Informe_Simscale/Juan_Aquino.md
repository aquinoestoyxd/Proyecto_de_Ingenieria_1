# 📌  Informe SIMSCALE
El presente informe se elaboró a partir de un análisis estructural estática realizado en la plataforma SimScale. Este análisis se realizó con el propósito de poner a prueba la resistencia de un componente mecánica frente a cargas externas según el material empleado en su impresión.

---

# ⚙️ Metodología
A fin de hacer la prueba de una forma que pueda adecuarse a nuestra situación real, el material empleado para la prueba ha sido **PLA**. Para llevar la prueba a cabo, se realizó el siguiente procedimiento:
1.- Elaboración de un pequeño modelado 3D en OneShape (denominado Control Arm).
2.- Importar el modelado en SimScale.
3.- Se aplicó Fixed Support a las caras del Control Arm.
4.- Se aplicó Force 2 de 50 a una parte lateral del modelado.
5.- Se asignó como material PLA.
6.- Se realizó el mallado automático con refinamiento en las zonas más exigentes.
7.- Inició el proceso de prueba.

---

# 📊 Resultados
Como se evidencia en la imagen, la construcción es estable frente a la fuerza aplicada, sin embargo, hay una pequeña zona (notable mediante el color naranja/rojo) que podría verse seriamente afectada.

<p align= "center">
  <img src="https://github.com/aquinoestoyxd/Proyecto_de_Ingenieria_1/blob/main/Im%C3%A1genes/ControlArm.png" alt="300px" width="600px"/>
</p>
