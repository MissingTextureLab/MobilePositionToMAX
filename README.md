# MobilePositionToMAX

## Descripción
Esta aplicación explora el uso de sensores del smartphone como herramienta de producción musical.  
El prototipo, desarrollado en **Flutter**, utiliza el **sensor acelerómetro** del dispositivo para enviar datos en tiempo real a **Max/MSP** mediante el protocolo **OSC** (Open Sound Control).  
Max/MSP es un software de programación visual orientado a la creación de música y sonido mediante patches, lo que permite integrar los datos del móvil en un DAW.

---

## Recursos utilizados

### Lectura del sensor
- Se emplea el paquete [`sensors_plus`](https://pub.dev/packages/sensors_plus) para **Dart/Flutter**.  
- Permite leer fácilmente los valores del acelerómetro con las variables `event.x`, `event.y`, `event.z`.

### Comunicación OSC
- Se usa la librería [`osc`](https://pub.dev/packages/osc) para Dart.  
- Esta permite enviar mensajes OSC de manera sencilla.  
- En este caso, se transmiten tres valores (x, y, z) correspondientes al acelerómetro.  
- También se utiliza `dart:io` para gestionar la dirección IP del receptor.

### Imagen e iconos
- Se añade el **logo de Max/MSP** mediante el widget `Image` cargado desde un enlace online.  
- El mismo recurso se emplea como **icono de la aplicación**, usando el paquete [`flutter_launcher_icons`](https://pub.dev/packages/flutter_launcher_icons).  
- Este paquete permite generar y asignar iconos personalizados a partir de imágenes definidas en el archivo `pubspec.yaml`.

---

## Perspectivas
Aunque no se ha realizado todavía una implementación completa en un sintetizador de Max/MSP, este prototipo establece la conexión necesaria para expandir el proyecto en el futuro.  

La idea es:  
- Desarrollar un sistema más complejo que permita controlar **múltiples parámetros de sintetizadores sustractivos y aditivos**.  
- Ampliar el uso de sensores del móvil para transformarlo en un **instrumento musical interactivo**.  
- Integrar esta aproximación en contextos de **performance, educación musical e instalaciones interactivas**.

---

> Este repositorio no está pensado como recurso útil, sino como parte de mi porfolio académico y creativo.
