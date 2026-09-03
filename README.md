# Propuestas de proyectos (5)

*PROPUESTA N°1*
*Nombre del proyecto:* AhorroLuz - Sistema Inteligente de Ahorro de Energía en Salas

*Problema o necesidad:* Las luces y ventiladores quedan prendidos en salas vacías, generando gasto de luz.

*Aplicación:* En cada sala de clases, laboratorio o baño.

*Funcionamiento:* Un sensor detecta si hay personas. Si no hay nadie por 2 minutos, apaga automáticamente luces y ventilador. Si alguien entra, los vuelve a prender.

*Arduino:* Arduino UNO

*Sensores:* Sensor de movimiento PIR HC-SR501, Sensor de luz LDR

*Actuadores:* Relé de 2 canales, Buzzer (avisa antes de apagar)

*Otros componentes:* LEDs indicadores, Resistencias 10k, Protoboard, Cables jumper

*Materiales:* Caja plástica impresa o de madera, tornillos, cinta aislante

*Programación:* El programa debe leer el PIR. Si detecta movimiento, activa el relé. Si no detecta por 120 segundos y el LDR indica que hay luz natural, suena el buzzer y corta la corriente.

*Viabilidad:* Sí, muy viable. Componentes baratos y fáciles de conseguir.

*PROPUESTA N°2*
*Nombre del proyecto:* SilencioMeter - Semáforo del Ruido

*Problema o necesidad:* Mucho ruido en la sala que interrumpe las clases.

*Aplicación:* Dentro de la sala de clases, biblioteca o sala de UTP.

*Funcionamiento:* Mide el nivel de ruido. Si es bajo, prende luz verde. Si es medio, amarilla. Si es muy alto, roja y suena una alarma.

*Arduino:* Arduino NANO

*Sensores:* Sensor de sonido KY-038 / Módulo micrófono MAX4466

*Actuadores:* LED RGB o 3 LEDs (verde, amarillo, rojo), Buzzer activo

*Otros componentes:* Pantalla LCD 16x2 con I2C, Potenciómetro, Resistencias 220 ohm, Botón pulsador para resetear

*Materiales:* Base de MDF o cartón, caja para el semáforo

*Programación:* Leer el valor del sensor de sonido. Convertirlo a decibeles. Mostrar el nivel en la LCD. Según rangos, prender el LED correspondiente y activar el buzzer si supera el límite.

*Viabilidad:* Sí, 100% viable y muy útil para los profes.

*PROPUESTA N°3*
*Nombre del proyecto:* EcoRiego - Riego Automático del Huerto Escolar

*Problema o necesidad:* El huerto del liceo se seca porque se olvidan de regarlo o se riega de más.

*Aplicación:* Huerto escolar, invernadero o jardines del patio.

*Sensores:* Sensor de humedad de suelo FC-28, Sensor de temperatura y humedad DHT11

*Actuadores:* Mini bomba de agua 5V o electroválvula, Servo motor SG90 (abre compuerta)

*Otros componentes:* Pantalla OLED 0.96", Relé 1 canal, LEDs, Resistencias

*Materiales:* Macetero, manguera, botella de 5 litros como estanque, tierra

*Funcionamiento:* Si la tierra está seca, activa la bomba y riega por 5 segundos. Muestra en la pantalla la humedad y temperatura.

*Arduino:* Arduino UNO

*Programación:* Si humedad de suelo < 40%, activar relé de la bomba. Mostrar datos en OLED. Esperar 1 hora antes de volver a medir.

*Viabilidad:* Sí, viable. Ideal si tienen huerto.

*PROPUESTA N°4*
*Nombre del proyecto:* FullBin - Basurero Inteligente con Alerta de Llenado

*Problema o necesidad:* Los basureros del patio se rebalsan y nadie avisa hasta que ya está sucio.

*Aplicación:* Patio, casino o pasillos.

*Funcionamiento:* Detecta qué tan lleno está el basurero. Cuando está al 90%, prende una luz roja y envía alerta sonora.

*Arduino:* Arduino UNO

*Sensores:* Sensor ultrasónico HC-SR04, Sensor de movimiento PIR (para abrir tapa)

*Actuadores:* Servo motor MG995 (para abrir la tapa), Buzzer, Tira LED roja

*Otros componentes:* Botón, Resistencias, Cables

*Materiales:* Basurero plástico grande, estructura de madera para soporte del sensor

*Programación:* El HC-SR04 mide la distancia al fondo. Si la distancia es pequeña = lleno. Si está lleno, prende LED rojo y buzzer. Si el PIR detecta mano, el servo abre la tapa.

*Viabilidad:* Sí, viable y muy innovador.

*PROPUESTA N°5*
*Nombre del proyecto:* SafeLab - Control de Acceso al Laboratorio

*Problema o necesidad:* Entran estudiantes sin permiso al laboratorio de ciencias o a bodega y se pueden perder materiales.

*Aplicación:* Puerta del laboratorio, sala de computación o bodega.

*Funcionamiento:* Solo permite el acceso si se ingresa una clave correcta en un teclado o se detecta la tarjeta.

*Arduino:* Arduino MEGA (tiene más pines)

*Sensores:* Teclado matricial 4x4, Lector RFID RC522

*Actuadores:* Cerradura solenoide o Servo motor para el pestillo, LED verde y rojo, Buzzer

*Otros componentes:* Pantalla LCD 16x2 I2C, Resistencias, Protoboard

*Materiales:* Caja para el circuito, puerta de maqueta para la prueba

*Programación:* El programa pide clave. Si la clave es correcta o la tarjeta RFID está autorizada, activa el servo para abrir por 5 segundos y prende LED verde. Si es incorrecta, LED rojo y buzzer 3 veces.

*Viabilidad:* Sí, requiere comprar el kit RFID que es barato.
