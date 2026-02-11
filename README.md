# PROYECTO LÁMPARA
     
## Índice

1. **Propósito**
2. **Modelado 3D y funcionalidades** 
3. **Circuito electrónico**
   - Conexión de sensores, LEDs, Arduino, etc.
   - Realizados en KiCad
   - Entregar la vista esquemática del circuito
4. **Código fuente de la aplicación web de control remoto**
   - Código de control de la lámpara

## 1. Propósito

## 2. Modelado 3D y funcionalidades
Esta lampara inteligente y sensorizada para el teletrabajo tiene varias funciones que la diferencian de otras propuestas del mercado. Teniendo de referencia en todo momento el modelo 3D realizado, se desarrollarán las funcionalidades implementadas e ideadas. Estas últimas, aunque han sido definidas en su totalidad, no han podido ser implementadas por las limitaciones del proyecto en lo referente al tiempo.

<p align="center">
  <img src="https://github.com/user-attachments/assets/fe32f820-4d9b-4236-9429-7e004b319264" alt="Imagen1" />
  <img src="https://github.com/user-attachments/assets/90809cb9-c4c7-46f4-9829-ef1d2f7366e1" alt="Imagen2" />
</p>

Empezando por la base de la lámpara, contiene varias funcionalidades gracias al diseño llevado a cabo. El primero trata del almacenamiento de material de oficina como lápices, bolígrafos u otros elementos como tijeras o reglas. Tanto el cubículo izquierdo como los agujeros individuales de la parte derecha están dirigidos a dicha función. Además, la inclinación y muesca de esta última sección mencionada también permiten la utilización de la base como soporte para teléfonos móviles.

<p align="center">
  <img src="https://github.com/user-attachments/assets/cd8b9b78-8c51-4529-97da-37f58a786d6a" alt="Imagen3" />
</p>

Por otra parte, gracias al sistema de posicionamiento mediante servomotor, el brazo de la lámpara puede ajustarse a diferentes posiciones dada su movilidad angular. Esto puede ser utilizado para un mejor almacenamiento del producto cuando no es utilizado.

<p align="center">
  <img src="https://github.com/user-attachments/assets/1e22d15f-4ce9-4e55-8047-e19c7c826bd6" alt="Imagen4" />
  <img src="https://github.com/user-attachments/assets/1f628f4f-b97f-4c78-a526-d66ddaad3690" alt="Imagen5" />
</p>

Tanto el sistema de movimiento, como el encendido y apagado de la lámpara se basan en un controlador WLED, la cual se conecta a una aplicación móvil que permite otras funcionalidades ideadas y que se van a detallar a continuación.

Dejando a un lado lo llevado a cabo, tal y como se ha mencionado en la introducción, se han ideado otras funcionalidades que pueden complementar la lámpara convirtiéndola en una mejor herramienta para el teletrabajo, pero no han podido ser llevadas a cabo por falta de tiempo:

- Variación de la calidez de la luz dependiendo de la hora
- Regulador de la intensidad de la luz
- Sensor y display de temperatura, humedad y hora
- Sensor de exceso de ruido

