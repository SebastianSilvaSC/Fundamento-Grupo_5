<h1 align = "center">Iteración</h1>
<h2 align = "left">- Hardware</h2>
<img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/F_esquemático.png">
<img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_Partes.jpg">
<h2 align = "left">- Software</h2>

<h2 align = "left">a) Diagrama de flujo</h2>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_DF.jpg"></p>

<h2 align = "left">b) Modelo de clasificación(Edge Impulse)</h2>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_1.jpg"></p>

<p > Nota. La figura anterior muestra las configuraciones de entrenamiento de una red neuronal en la plataforma Edge Impulse, esenciales para la clasificación de microplásticos. Se configuran 20 ciclos de entrenamiento y una tasa de aprendizaje de 0.0005, parámetros que aseguran una adecuada adaptación del modelo a los datos. La opción de aumento de datos está habilitada, lo cual es crucial para mejorar la robustez del modelo al generar variaciones en las imágenes de entrenamiento, evitando el sobreajuste y permitiendo una mejor generalización. El tamaño del lote es de 32, equilibrando la eficiencia computacional y la estabilidad de las actualizaciones de los pesos. Además, el modelo está cuantizado a int8, reduciendo su tamaño y mejorando la velocidad de inferencia, ideal para su implementación en dispositivos con recursos limitados como el ESP32.</p>


<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_2.jpg"></p>

<p > Nota. La figura ilustra la arquitectura de una red neuronal convolucional basada en MobileNetV2, empleando transfer learning. El transfer learning aprovecha un modelo preentrenado en un gran conjunto de datos para extraer características generales y adaptar sus capas finales a la tarea específica de clasificación de microplásticos. El flujo comienza con el preprocesamiento de imágenes de 96x96 píxeles, seguido por varias capas convolucionales y de pooling que extraen características relevantes, como bordes y texturas. MobileNetV2, optimizada para eficiencia, permite un buen equilibrio entre precisión y uso de recursos. Las características extraídas se alimentan a una capa completamente conectada y finalmente a un clasificador Softmax, que asigna probabilidades a cada clase, determinando si una imagen contiene microplásticos. Esta arquitectura permite una clasificación precisa y eficiente, fundamental para detectar microplásticos en diferentes condiciones y escenarios.</p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_3.jpg"></p>

<h2 align = "left">c) Captura de datos(Arduino)</h2>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_4.jpg"></p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_5.jpg"></p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_6.jpg"></p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_7.jpg"></p>

<h2 align = "left">d) Ejemplo de clasificación</h2>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_8.jpg"></p>

<h2 align = "left">e) Avance de código</h2>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_9.jpg"></p>

<p > Nota.La figura muestra las librerías utilizadas en el desarrollo del proyecto de clasificación de microplásticos con ESP32. Incluye librerías como Arduino Uno WiFi Dev Ed Library para funcionalidades de red, ArduinoJson para manejar JSON de manera eficiente, ESP32Servo para controlar motores, DallasTemperature y OneWire para medir la temperatura, y esp32 para el soporte de las placas ESP32. </p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_10.jpg"></p>

<p > Nota.Como se muestra en la figura, se observa un fragmento de código que declara las credenciales necesarias para la conexión WiFi y el acceso a Google Apps Script, así como la obtención de datos del sensor de temperatura. La sección de credenciales incluye el SSID y contraseña de la red, así como la URL del script de Google. El código para el sensor de temperatura utiliza la librería DallasTemperature para solicitar y mostrar la temperatura en grados Celsius y Fahrenheit.</p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_11.jpg"></p>

<p > Nota.La figura presenta el código utilizado para leer y procesar los datos del sensor de turbidez. Se toma una media de 500 muestras para compensar el ruido, y se convierte la lectura analógica en unidades nefelométricas (NTU). </p>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_12.jpg"></p>

<p > Nota.Este fragmento de código ilustra cómo se envían los datos capturados del sensor de temperatura y turbidez a un servidor usando un script de Google Apps Script. Los datos se formatean y se envían mediante una solicitud HTTP POST. Este mecanismo de envío permite integrar los datos recogidos por los sensores con una base de datos centralizada, permitiendo el almacenamiento y posterior análisis en la nube, y a su vez facilita la automatización del proceso de recolección y reporte de datos, ya que logra que la información esté disponible para posterir análisis .</p>

<h2 align = "left">f) Ejemplo de circuito de prueba</h2>

<p align="center"><img src="https://github.com/SebastianSilvaSC/Fundamento-Grupo_5/blob/main/Proyecto/Imagenes/G_13.jpg"></p>

<h2 align = "left">- Integración Hardware - Impresión 3D</h2>
