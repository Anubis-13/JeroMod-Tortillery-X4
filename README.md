# 🧪 Beta privada de JeroMod-Tortillery X4

Gracias por participar en las pruebas de **JeroMod-Tortillery X4**.

Este repositorio privado servirá para organizar las pruebas, comunicar incidencias y comprobar las correcciones que se publiquen durante la beta. El grupo es reducido para una mejor trabajo y el contenido no debe compartirse fuera de él has el momento de tener una imagen candidata para lanzamiento.

No es necesario saber programación, Klipper, Linux ni electrónica. Cada prueba tendrá instrucciones sencillas y se realizará utilizando la impresora y su pantalla de forma normal.

> ⏳ **La campaña todavía no ha comenzado.** No es necesario hacer nada hasta recibir la primera prueba.

## 📥 Descarga de la imagen inicial

La imagen principal se distribuirá mediante un enlace privado externo. Debido a su tamaño, **no estará alojada directamente en GitHub**.

**Enlace de descarga:**

```text
PENDIENTE DE AÑADIR
```
> 🔒 La imagen beta 01... se descarga del enlace publicado aquí. 
Archivo que debéis recibir:

```text
JeroMod_Tortillery_X4_BETA-01-1.0.5-0.0.23-0.164-8GB.img
```


Comprobación del archivo:

```text
Tamaño: 7.818.182.656 bytes
Tamaño aproximado: 7,281 GiB
SHA-256: 46CD224D14F29F1B7F8D8BFCF6D7E5703B4784E7237ED7DD1A64DB7002FAE479
```
> 🔒 Antes de grabarla en la eMMC, comprobad que el nombre, el tamaño y el SHA-256 coincidan.


## 📋 Versión inicial:

```text
Estas son las versiones de cada módulo de inicio 

Imagen: JeroMod-Tortillery X4 BETA-01
Firmware base: Tortillery v1.0.5
Sistema: JeroMod SYS v0.0.23
Pantalla: JeroMod TFT v0.164
```


Modelos incluidos:

- **Artillery X4 Pro:** modelo principal de la beta y físicamente validado.
- **Artillery X4 Plus:** perfil instalable, pero pendiente de validación física completa.

> ⚠️ El perfil X4 Plus solo debe probarse en una X4 Plus real. No lo instaléis ni lo seleccionéis en una X4 Pro.

## Actualizaciones de la beta

El sistema de actualización mediante USB será una de las primeras funciones que utilizaremos, porque servirá para recibir las correcciones durante toda la campaña.

Cada actualización aparecerá identificada con un nombre como:

```text
UPD-BETA-02
```

Cada actualización deberá probarla **todo el grupo**, aunque esté destinada únicamente a la X4 Pro o a la X4 Plus. Esto permitirá comprobar tanto la instalación correcta como la protección entre modelos.

- En el modelo compatible, la actualización deberá instalarse y finalizar correctamente.
- En el modelo no compatible, el sistema deberá reconocer que el paquete pertenece a otro modelo y bloquear la instalación sin modificar nada.

Cada tester comunicará qué modelo ha utilizado y el resultado mostrado por la pantalla.

Si la pantalla indica que un archivo no es válido, pertenece a otro modelo o no puede instalarse, cancelad el proceso y comunicadlo.

> 🚫 Utilizad únicamente el paquete autorizado para esa prueba. No lo renombréis, no lo modifiquéis y no añadáis otros archivos o scripts al USB.

Después de actualizar no será necesario repetir toda la campaña. Se indicarán las pruebas afectadas y las comprobaciones de regresión necesarias.

Las pruebas de recuperación, rollback o interrupción deliberada de una actualización se prepararán aparte. **No deben realizarse por iniciativa propia.**

## Cómo trabajaremos

Las pruebas se publicarán poco a poco. Algunas serán rápidas, como comprobar un botón, hacer Home o mover un eje. Otras se dividirán en varias partes, como imprimir, pausar, cambiar filamento o recuperar una impresión.

Cada prueba indicará:

- qué modelo puede realizarla;
- desde qué pantalla hay que empezar;
- qué pasos hay que seguir;
- qué debería ocurrir;
- si implica movimiento, calentamiento o algún riesgo;
- qué información necesito recibir al terminar.

Cuando recibáis una prueba, seguid solamente los pasos indicados. Si alguna instrucción no está clara, preguntad antes de continuar.

## Cómo informar del resultado

Si todo funciona, bastará con responder:

```text
OK
Modelo: X4 Pro o X4 Plus
Observaciones: opcional
```

Los estados que utilizaremos son:

- **OK:** funcionó como se esperaba.
- **FALLO:** ocurrió algo diferente.
- **NO PROBADO:** todavía no se ha realizado.
- **NO APLICA:** no corresponde a ese modelo o configuración.
- **BLOQUEADO POR SEGURIDAD:** fue necesario detener la prueba.
- **PENDIENTE DE ACTUALIZACIÓN:** existe una corrección pendiente de instalar.
- **CORREGIDO, PENDIENTE DE REPETIR:** la corrección está instalada, pero falta comprobarla.
- **VALIDADO DESPUÉS DE ACTUALIZAR:** la prueba se repitió correctamente.

## Si encontráis un problema

Cada problema debe comunicarse por separado. No es necesario intentar averiguar la causa técnica; necesito saber qué hicisteis y qué ocurrió.

Indicad:

```text
Prueba que estabais realizando:
Modelo de impresora:
Pantalla desde la que empezasteis:
Botón que pulsasteis:
Resultado esperado:
Resultado real:
¿Ocurre siempre o solo algunas veces?:
¿Hubo movimiento?: Sí / No
¿Hubo calentamiento?: Sí / No
¿Existió algún riesgo?: Sí / No
Foto o vídeo, si está disponible:
```

Ejemplo:

```text
Estaba en la pantalla Movimiento.
Pulsé Home Y.
Esperaba que se moviese el eje Y, pero se movió el eje X.
Apagué la impresora y no repetí la prueba por seguridad.
```

## Seguridad

Durante cualquier prueba con movimiento o calentamiento, permaneced junto a la impresora y mantened despejada la zona de trabajo.

Detened la prueba si observáis:

- un eje moviéndose en una dirección incorrecta;
- golpes o ruidos mecánicos anormales;
- la boquilla acercándose de forma peligrosa a la cama o a una pieza;
- calentamiento no solicitado;
- una temperatura que aumenta de forma inesperada;
- humo, olor a quemado o cableado caliente;
- cualquier comportamiento que pueda dañar la impresora o resultar peligroso.

No repitáis una situación peligrosa para conseguir una foto o un vídeo. Si es necesario detener la prueba, indicad `BLOQUEADO POR SEGURIDAD` y explicad brevemente lo ocurrido.

## Fotos, vídeos e información privada

Las fotos y vídeos solo serán necesarios cuando ayuden a entender el problema. Antes de publicarlos, comprobad que no muestren:

- contraseñas Wi-Fi;
- claves SSH;
- tokens o códigos privados;
- direcciones o datos personales;
- otra información que no esté relacionada con la prueba.

No compartáis fuera del grupo las imágenes, actualizaciones, enlaces o documentos de esta beta.

## Pruebas especiales

Las siguientes pruebas se dejarán para campañas específicas:

- impresión completa y todas sus variantes;
- pausa, reanudación y cambio de filamento;
- recuperación tras un corte eléctrico;
- recuperación o rollback forzado de una actualización;
- restauración de fábrica;
- validación física completa de la X4 Plus.

No realicéis estas pruebas por iniciativa propia. Se proporcionarán instrucciones concretas cuando llegue el momento.

## Reglas generales

- Seguid únicamente los pasos de la prueba asignada.
- Preguntad si alguna instrucción no está clara.
- No modifiquéis archivos internos de la impresora.
- No instaléis archivos sueltos ni paquetes no autorizados.
- No probéis el perfil Plus en una X4 Pro.
- No cortéis la alimentación sin una prueba preparada.
- No utilicéis una restauración de fábrica para intentar resolver una incidencia.
- No compartáis el material de la beta fuera del grupo.

El objetivo es comprobar el funcionamiento de JeroMod-Tortillery X4 de forma ordenada y segura. Gracias por dedicar vuestro tiempo y vuestra impresora a estas pruebas.
