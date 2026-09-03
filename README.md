# 🤖 Propuestas de Proyectos Arduino

💡 Propuestas de innovación tecnológica para resolver problemas reales dentro del establecimiento educacional.

Este repositorio presenta 5 proyectos basados en Arduino, utilizando sensores, actuadores y programación para crear soluciones prácticas, económicas e innovadoras.

📑 Índice
💡 Propuesta 1 — AhorroLuz
🔊 Propuesta 2 — SilencioMeter
🌱 Propuesta 3 — EcoRiego
🗑️ Propuesta 4 — FullBin
🔐 Propuesta 5 — SafeLab
📊 Comparación general
🏆 Conclusión
💡 Propuesta N.º 1 — AhorroLuz
🔋 Sistema Inteligente de Ahorro de Energía en Salas
🎯 Problema o necesidad

Las luces y ventiladores pueden quedar encendidos en salas vacías, generando un gasto innecesario de energía eléctrica.

🏫 Aplicación

El sistema puede utilizarse en:

🏫 Salas de clases
🔬 Laboratorios
🚻 Baños
🏢 Otras dependencias del establecimiento
⚙️ Funcionamiento

Un sensor de movimiento detecta si hay personas dentro de la sala.

Si no se detecta movimiento durante 2 minutos (120 segundos), el sistema:

🔔 Hace sonar el buzzer para avisar antes de apagar.
💡 Apaga automáticamente las luces.
🌀 Apaga el ventilador mediante el relé.

Si alguien vuelve a entrar y el sensor detecta movimiento, el sistema vuelve a activar las luces y el ventilador.

🖥️ Arduino

Arduino UNO

📡 Sensores
Sensor de movimiento PIR HC-SR501
Sensor de luz LDR
⚡ Actuadores
Relé de 2 canales
Buzzer para avisar antes del apagado
🔧 Otros componentes
LEDs indicadores
Resistencias de 10 kΩ
Protoboard
Cables jumper
🛠️ Materiales
Caja plástica impresa o de madera
Tornillos
Cinta aislante
💻 Programación

El programa debe leer constantemente el sensor PIR.

SI se detecta movimiento:
    → Activar el relé.
    → Mantener las luces y ventilador encendidos.
    → Reiniciar el temporizador.

SI NO se detecta movimiento durante 120 segundos:
    → Comprobar el sensor LDR.
    → Si corresponde, hacer sonar el buzzer.
    → Cortar la corriente mediante el relé.

SI vuelve a detectarse movimiento:
    → Reactivar las luces y el ventilador.

✅ Viabilidad

🟢 Sí, muy viable. Los componentes son baratos y fáciles de conseguir.

🔊 Propuesta N.º 2 — SilencioMeter
🚦 Semáforo del Ruido
🎯 Problema o necesidad

Existe demasiado ruido dentro de las salas, lo que puede interrumpir las clases y dificultar la concentración de los estudiantes.

🏫 Aplicación

Puede utilizarse en:

🏫 Salas de clases
📚 Bibliotecas
🧑‍💼 Salas de UTP
🤫 Espacios donde se requiera mantener un nivel de ruido controlado
⚙️ Funcionamiento

El sistema mide el nivel de ruido del ambiente y lo representa mediante un semáforo luminoso.

Nivel de ruido	Indicador	Acción
🟢 Bajo	LED verde	Ambiente adecuado
🟡 Medio	LED amarillo	Nivel de precaución
🔴 Alto	LED rojo	Activa alarma

Cuando el nivel de ruido es demasiado alto, se enciende la luz roja y se activa el buzzer.

🖥️ Arduino

Arduino NANO

📡 Sensores
Sensor de sonido KY-038
Módulo micrófono MAX4466
💡 Actuadores
LED RGB o 3 LEDs:
🟢 Verde
🟡 Amarillo
🔴 Rojo
Buzzer activo
🔧 Otros componentes
Pantalla LCD 16x2 con I2C
Potenciómetro
Resistencias de 220 Ω
Botón pulsador para resetear
🛠️ Materiales
Base de MDF o cartón
Caja para construir el semáforo
💻 Programación

El programa debe:

1. Leer el valor entregado por el sensor de sonido.

2. Procesar el valor obtenido.

3. Convertir/calibrar el valor para obtener una estimación
   del nivel de ruido en decibeles.

4. Mostrar el nivel de ruido en la pantalla LCD.

5. Comparar el valor con los rangos establecidos.

6. Encender el LED correspondiente:
      → Verde = ruido bajo
      → Amarillo = ruido medio
      → Rojo = ruido alto

7. Si se supera el límite:
      → Activar el buzzer.

✅ Viabilidad

🟢 Sí, 100% viable y muy útil para los profesores.

🌱 Propuesta N.º 3 — EcoRiego
💧 Riego Automático del Huerto Escolar
🎯 Problema o necesidad

El huerto del liceo puede secarse porque se olvida regarlo, o puede recibir demasiada agua debido a un riego excesivo.

🏫 Aplicación

Puede utilizarse en:

🌱 Huertos escolares
🌿 Invernaderos
🌳 Jardines del patio
🪴 Maceteros
⚙️ Funcionamiento

El sistema mide la humedad de la tierra.

Cuando la tierra está demasiado seca, el sistema activa automáticamente una bomba de agua y realiza un riego durante 5 segundos.

Además, muestra información sobre la humedad y temperatura en una pantalla OLED.

🖥️ Arduino

Arduino UNO

📡 Sensores
Sensor de humedad de suelo FC-28
Sensor de temperatura y humedad DHT11
💧 Actuadores
Mini bomba de agua 5V o electroválvula
Servo motor SG90 para abrir una compuerta
🔧 Otros componentes
Pantalla OLED 0.96"
Relé de 1 canal
LEDs
Resistencias
🛠️ Materiales
Macetero
Manguera
Botella de 5 litros como estanque
Tierra
💻 Programación

La lógica principal será:

1. Leer la humedad del suelo.

2. Mostrar en la pantalla OLED:
      → Humedad del suelo
      → Temperatura
      → Humedad ambiental

3. Si la humedad del suelo < 40%:
      → Activar el relé.
      → Encender la bomba.
      → Regar durante 5 segundos.
      → Apagar la bomba.

4. Esperar 1 hora.

5. Volver a medir la humedad.

✅ Viabilidad

🟢 Sí, viable. Es un proyecto ideal si el establecimiento cuenta con un huerto.

🗑️ Propuesta N.º 4 — FullBin
🚨 Basurero Inteligente con Alerta de Llenado
🎯 Problema o necesidad

Los basureros del patio pueden rebalsarse sin que nadie avise, provocando suciedad y malos olores.

🏫 Aplicación

Puede utilizarse en:

🏫 Patios
🍽️ Casinos
🚶 Pasillos
🗑️ Espacios comunes del establecimiento
⚙️ Funcionamiento

El sistema detecta qué tan lleno está el basurero utilizando un sensor ultrasónico.

Cuando el basurero alcanza aproximadamente el 90% de su capacidad:

🔴 Enciende una luz roja.
🔊 Activa una alerta sonora.

Además, el sensor PIR permite detectar cuando una persona acerca la mano al basurero.

Cuando detecta movimiento, el servo motor abre automáticamente la tapa.

🖥️ Arduino

Arduino UNO

📡 Sensores
Sensor ultrasónico HC-SR04
Sensor de movimiento PIR para detectar la mano
⚙️ Actuadores
Servo motor MG995 para abrir la tapa
Buzzer
Tira LED roja
🔧 Otros componentes
Botón
Resistencias
Cables
🛠️ Materiales
Basurero plástico grande
Estructura de madera para soportar el sensor
💻 Programación

El HC-SR04 mide la distancia entre el sensor y la basura.

1. Medir la distancia dentro del basurero.

2. Calcular el porcentaje aproximado de llenado.

3. Si el basurero alcanza el 90%:
      → Encender LED rojo.
      → Activar el buzzer.

4. Si el sensor PIR detecta una mano:
      → Activar el servo.
      → Abrir la tapa.

5. Después de unos segundos:
      → Cerrar nuevamente la tapa.

✅ Viabilidad

🟢 Sí, viable y muy innovadora.

🔐 Propuesta N.º 5 — SafeLab
🛡️ Control de Acceso al Laboratorio
🎯 Problema o necesidad

El ingreso de estudiantes o personas sin autorización al laboratorio de ciencias o a una bodega puede provocar pérdida o daño de materiales.

🏫 Aplicación

Puede utilizarse en:

🔬 Laboratorio de ciencias
💻 Sala de computación
📦 Bodegas
🚪 Espacios con acceso restringido
⚙️ Funcionamiento

El sistema permite el acceso únicamente si:

🔢 Se ingresa una clave correcta mediante un teclado, o
💳 Se detecta una tarjeta RFID autorizada.

Si la clave o tarjeta es correcta, se activa el mecanismo de apertura durante 5 segundos.

Si los datos son incorrectos, se activa una alerta.

🖥️ Arduino

Arduino MEGA

El Arduino MEGA se utiliza debido a que dispone de una mayor cantidad de pines, lo que facilita conectar todos los componentes del proyecto.

📡 Sensores / Entradas
Teclado matricial 4x4
Lector RFID RC522
🔒 Actuadores
Cerradura solenoide o servo motor para el pestillo
LED verde
LED rojo
Buzzer
🔧 Otros componentes
Pantalla LCD 16x2 con I2C
Resistencias
Protoboard
🛠️ Materiales
Caja para el circuito
Puerta de maqueta para realizar las pruebas
💻 Programación

El sistema solicitará una clave o leerá una tarjeta RFID.

1. Solicitar clave o leer tarjeta RFID.

2. Comprobar si la clave/tarjeta está autorizada.

SI es correcta:
      → Encender LED verde.
      → Activar el servo/cerradura.
      → Abrir durante 5 segundos.
      → Cerrar nuevamente.

SI es incorrecta:
      → Encender LED rojo.
      → Activar el buzzer 3 veces.
      → Mantener la puerta cerrada.

✅ Viabilidad

🟢 Sí, viable. Requiere comprar un kit RFID, pero es económico y fácil de integrar al proyecto.

📊 Comparación general

A continuación se comparan las cinco propuestas considerando su área de aplicación, placa Arduino, dificultad, utilidad y principales componentes.

#	Proyecto	Área	Arduino	Dificultad	Utilidad
1	💡 AhorroLuz	⚡ Ahorro energético	UNO	🟢 Fácil	⭐⭐⭐⭐⭐
2	🔊 SilencioMeter	🤫 Control de ruido	NANO	🟢 Fácil	⭐⭐⭐⭐⭐
3	🌱 EcoRiego	🌎 Medioambiente	UNO	🟡 Media	⭐⭐⭐⭐⭐
4	🗑️ FullBin	♻️ Limpieza	UNO	🟡 Media	⭐⭐⭐⭐
5	🔐 SafeLab	🛡️ Seguridad	MEGA	🟠 Media/Alta	⭐⭐⭐⭐⭐
🧩 Comparación de componentes
Proyecto	Sensor principal	Actuador principal	Pantalla
💡 AhorroLuz	PIR HC-SR501 + LDR	Relé 2 canales	❌
🔊 SilencioMeter	KY-038 / MAX4466	LEDs + Buzzer	LCD 16x2
🌱 EcoRiego	FC-28 + DHT11	Bomba / electroválvula	OLED 0.96"
🗑️ FullBin	HC-SR04 + PIR	Servo MG995	❌
🔐 SafeLab	RFID RC522 + teclado 4x4	Servo / solenoide	LCD 16x2
🎯 Problema que resuelve cada propuesta
Proyecto	Problema	Solución
💡 AhorroLuz	Luces y ventiladores encendidos innecesariamente	Apagado automático mediante sensores
🔊 SilencioMeter	Exceso de ruido en las salas	Semáforo visual y alarma sonora
🌱 EcoRiego	Falta o exceso de riego	Riego automático según humedad
🗑️ FullBin	Basureros rebalsados	Alerta automática de llenado
🔐 SafeLab	Acceso no autorizado	Control mediante clave y RFID
💰 Viabilidad general
Proyecto	Costo estimado	Disponibilidad de componentes	Viabilidad
💡 AhorroLuz	💲 Bajo	🟢 Fácil	⭐⭐⭐⭐⭐
🔊 SilencioMeter	💲 Bajo	🟢 Fácil	⭐⭐⭐⭐⭐
🌱 EcoRiego	💲 Bajo/Medio	🟢 Fácil	⭐⭐⭐⭐⭐
🗑️ FullBin	💲 Medio	🟢 Fácil	⭐⭐⭐⭐
🔐 SafeLab	💲 Medio	🟡 Requiere kit RFID	⭐⭐⭐⭐⭐

💡 Los costos pueden variar dependiendo de dónde se compren los componentes y de si algunos materiales ya están disponibles.

🏆 Conclusión

Las cinco propuestas buscan aplicar Arduino, sensores, actuadores y programación para solucionar problemas reales dentro del establecimiento educacional.

💡 AhorroLuz

Busca reducir el consumo innecesario de energía, apagando luces y ventiladores cuando no hay personas.

🔊 SilencioMeter

Busca mejorar el ambiente de aprendizaje mediante un semáforo que indica visualmente el nivel de ruido.

🌱 EcoRiego

Permite automatizar el riego de un huerto escolar, evitando que las plantas se sequen o reciban demasiada agua.

🗑️ FullBin

Busca mejorar la limpieza mediante un basurero capaz de detectar su nivel de llenado y abrirse automáticamente.

🔐 SafeLab

Aumenta la seguridad mediante un sistema de control de acceso utilizando contraseña y tecnología RFID.

🚀 Objetivo final

Convertir problemas cotidianos del establecimiento en soluciones tecnológicas mediante programación, electrónica y automatización.

🛠️ Tecnologías




Arduino · C++ · Electrónica · Sensores · Actuadores · Automatización · Prototipado

📌 Estado del proyecto
Estado	Descripción
📝 Propuestas	Completadas
🔧 Selección del proyecto	⏳ Pendiente
🧩 Diseño del prototipo	⏳ Pendiente
💻 Programación	⏳ Pendiente
🔌 Montaje electrónico	⏳ Pendiente
🧪 Pruebas	⏳ Pendiente
🚀 Presentación final	⏳ Pendiente

⭐ Proyecto de innovación tecnológica escolar

🤖 Crear. Programar. Automatizar. Solucionar.
