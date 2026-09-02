<div align="center">

# ARCADE DISNEY ALADDIN 

<img src="assets/banner.png" alt="Banner Arcade Aladdin" width="100%" />

<p align="center">
  <a href="https://www.espressif.com/"><img src="https://img.shields.io/badge/MCU-ESP32--S3-E7352C?style=for-the-badge&logo=espressif&logoColor=white" alt="ESP32-S3"></a>
  <a href="https://github.com/moononournation/Arduino_GFX"><img src="https://img.shields.io/badge/Graphics-Arduino%20GFX-FF9900?style=for-the-badge" alt="Arduino GFX"></a>
  <a href="https://isocpp.org/"><img src="https://img.shields.io/badge/Language-C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Copyright-red?style=for-the-badge" alt="License"></a>
</p>

</div>

## ⚙️ Arquitectura del Sistema
Arquitectura distribuida de doble microcontrolador implementada para solventar la saturación de I/O (pines) de la unidad principal, delegando el procesamiento de entradas a un nodo secundario sin comprometer la velocidad del bus gráfico.

* **Unidad Principal (ESP32-S3 / JC4827W543):** Responsable de la ejecución del núcleo de la aplicación, el motor gráfico mediante `Arduino GFX` y el renderizado de la interfaz.
* **Subsistema Periférico (ESP32 Wroom 32):** Dedicado exclusivamente al control de botoneras, joystick, lector RFID y tira LED mediante IR.
* **Enlace de Comunicación:** Interconexión síncrona/asíncrona bidireccional mediante bus serie **UART** entre ambos microcontroladores.

---

## 🏆 Resultado y Organización
<div align="center">
<table border="0">
  <tr>
    <!-- COLUMNA IZQUIERDA: VISTA GENERAL -->
    <td width="50%" align="center" valign="top">
      <h3> Vista General</h3>
      <br>
      <img src="assets/maquina_arcade.jpg" alt="Máquina Arcade Aladdin Finalizada" width="100%" style="border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.2);" />
      <p><i>Máquina Arcade Finalizada y Funcionando</i></p>
    </td>
    <!-- COLUMNA DERECHA: ESTRUCTURA DEL REPOSITORIO -->
    <td width="50%" align="left" valign="top">
      <h3>Estructura del Repositorio</h3>
      <br>
      <!-- Usamos <pre> para forzar el formato de texto preformateado y evitar que se amontone -->
      <pre style="font-family: 'Courier New', Courier, monospace; font-size: 0.9em; background-color: #161b22; padding: 15px; border-radius: 8px; border: 1px solid #30363d;">
 Arcade-Disney-Aladdin
 ┣ 📂 assets/
 ┃ ┣ # Imágenes, banners y esquemas
 ┃ ┣ 📄 banner.png
 ┃ ┗ 📄 maquina_arcade.jpg
 ┃      
 ┣ 📂 docs/   
 ┣ # Documentación técnica y manuales
 ┃ ┣ 📂 datasheets/
 ┃ ┗ 📂 manuales/
 ┃      
 ┣ 📂 fabricación/   
 ┣ # Esquema eléctrico y planos 
 ┃ ┣ 📂 electronics/
 ┃ ┗ 📂 structure/
 ┃      
 ┣ 📂 src/
 ┃ ┣ 📂 esp32_s3_main/
 ┃ ┃ ┣ # Código principal 
 ┃ ┗ 📂 esp32_wroom_per/
 ┃   ┣ # Código secundario 
 ┃ 
 ┣ 📄 .gitignore
 ┣ 📄 LICENSE
 ┗ 📄 README.md
      </pre>
    </td>
  </tr>
</table>
</div>

---

## 🔄 Diagrama de flujo (Máquina de Estados)

<div align="center">
  <!-- Asegúrate de guardar tu imagen exportada de Draw.io con este nombre en la carpeta assets -->
  <img src="assets/diagrama_flujo_arcade.jpeg" alt="Máquina de Estados y Diagrama de Flujo" width="85%" />
</div>

---

## 📚 Documentación
Enlace a documentación del repositorio

*  [Esquema Electrónico y Cableado](fabricación/electronics/Arcade_Schematic.pdf)

---

## 📄 Licencia

Este proyecto está protegido bajo derechos de autor exclusivos. Consulta el archivo [LICENSE](LICENSE) para más información.
