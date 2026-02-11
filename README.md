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
Este proyecto tiene como objetivo diseñar y programar el funcionamiento de una lámpara inteligente con control remoto mediante una aplicación para el móvil, la cual debe tener funcionalidades que mejoren el entorno de teletrabajo de una persona. Para eso el proyecto ha sido dividido en varios apartados: el modelado 3D y sus funcionalidades, el circuito electrónico y su programación.


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

<p align="center">
  <img src="https://github.com/user-attachments/assets/c62ce349-2d69-43ab-9eb6-4903ad6cb75c" width="700"/>
</p>

Además del sistema de movimiento, la lámpara puede:
- Encender y apagarse mediante un pulsador o mediante la aplicación móvil. 
- Regular la intensidad de la luz con un "rodillito" o mediante la aplicación móvil.
- Cambiar la calidez de la luz mediante la aplicación móvil

IMAGEN MENU APP

Dejando a un lado lo llevado a cabo, tal y como se ha mencionado en la introducción, se han ideado otras funcionalidades que pueden complementar la lámpara convirtiéndola en una mejor herramienta para el teletrabajo, pero no han podido ser llevadas a cabo por falta de tiempo:

- Variación de la calidez de la luz dependiendo de la hora
- Sensor y display de temperatura, humedad y hora
- Sensor de exceso de ruido

## 3. Circuito electrónico
A continuación, se puede observar el circuito desarrollado junto con su respectivo esquema electrónico:

IMAGEN CIRCUITO

ESQUEMA ELECTRÓNICO

Dicho circuito contiene los siguientes elementos:
| Elemento                 | Identificador                     | Modelo                                              | Cantidad | Capacidad                     |
|--------------------------|------------------------------------|-----------------------------------------------------|----------|--------------------------------|
| Resistencia              | R10,R11,R7,R9,R12,R13,R14          | R_0402_1005Metric                                   | 7        | 10K                            |
|                          | R15,R3,R8                          | R_0402_1005Metric                                   | 3        | 1K                             |
|                          | R6                                 | R_0402_1005Metric                                   | 1        | 10kΩ                           |
|                          | R1                                 | R_0402_1005Metric                                   | 1        | TBD                            |
| Potenciómetro            | RV3                                | R_0402_1005Metric                                   | 1        | Varistor                       |
| Transistor               | Q2,Q3,Q1,Q4                        | SOT-23                                              | 4        | Q_NMOS_GSD                     |
| Conector                 | J5                                 | PinHeader_1x09_P2.54mm_Vertical                     | 1        | Conn_01x09                     |
|                          | J8                                 | PinHeader_1x03_P2.54mm_Vertical                     | 1        | Conn_01x03                     |
|                          | J7                                 | PinHeader_2x03_P2.54mm_Horizontal                   | 1        | Conn_02x03                     |
|                          | J1                                 | PinHeader_1x08_P2.54mm_Vertical                     | 1        | Conn_01x08                     |
|                          | J2                                 | USB_C_Receptacle_G-Switch_GT-USB-7010ASV            | 1        | USB_C_Receptacle_USB2.0        |
|                          | JP4,JP3,JP1,JP2                    | SolderJumper-2_P1.3mm_Open_RoundedPad1.0x1.5mm      | 4        | Jumper                         |
|                          | J4                                 | TestPoint_Pad_3.0x3.0mm                             | 1        | Conn_01x01                     |
| Inductor de potencia     | L2                                 | L_Abracon_ASPI-0425                                 | 1        | TBD                            |
| Diodo                    | D1                                 | D_SOD-128                                           | 1        | D_Small                        |
| Circuitos integrados     | U2                                 | SOT-23-5                                            | 1        | MIC5219-3.3YM5                 |
|                          | U5                                 | TSOT-23-6                                           | 1        | AP63205WU                      |
|                          | U1                                 | ESP32-C3-MINI-1                                     | 1        | ESP32-C3-MINI-1                |
|                          | U3                                 | SOIC-10_3.9x4.9mm_P1mm                              | 1        | ~                              |
| Condensador              | C13,C8,C1,C11                      | C_0402_1005Metric                                   | 4        | 1µF                            |
|                          | C15                                | C_0402_1005Metric                                   | 1        | 100nF                          |
|                          | C17,C16                            | C_0805_2012Metric                                   | 2        | 22µF                           |
|                          | C10                                | C_0805_2012Metric                                   | 1        | 10µF                           |
| Interruptor              | SW2                                | R-668048                                            | 1        | SW_MEC_5G                      |

El siguiente link muestra la posición exacta de cada elemento en el cirucito previamente mostrado:

LINK BOM

## 4. Código fuente de la aplicación web de control remoto
Tal y como se ha introducido previamente, la lámpara viene acompañada de una aplicación móvil con varias funciones integradas. La programación que ha permitido dicho funcionamiento se encuentra adjuntada en el repositorio con el nombre PROGRAMACIÓN.
