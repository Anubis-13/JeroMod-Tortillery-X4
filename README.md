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

## 🔄 Actualizaciones de la beta

El sistema de actualización mediante USB será una de las primeras funciones que probaremos, ya que se utilizará para recibir las correcciones durante toda la campaña.

Cada actualización tendrá un identificador, por ejemplo:

```text
UPD-BETA-02
```

La publicación de cada actualización indicará:

- los modelos compatibles;
- la versión necesaria antes de instalarla;
- qué problema corrige;
- cómo preparar el USB;
- qué debe aparecer en pantalla;
- qué pruebas hay que repetir después.

Las primeras comprobaciones incluirán:

1. Detectar una actualización autorizada desde la pantalla principal.
2. Revisar la información mostrada antes de instalar.
3. Probar la opción **Cancelar** sin modificar el sistema.
4. Instalar una actualización beta autorizada.
5. Comprobar el reinicio posterior.
6. Confirmar que la impresora vuelve a funcionar normalmente.
7. Revisar la versión mostrada en **Información**.
8. Repetir las pruebas relacionadas con la corrección.

> 🚫 No instaléis archivos sueltos, scripts, paquetes enviados por otras personas ni actualizaciones destinadas a otro modelo. No renombréis ni modifiquéis el paquete.

Si la pantalla indica que un archivo no es válido, pertenece a otro modelo o no puede instalarse, cancelad el proceso y comunicadlo.

Las pruebas de recuperación, rollback o interrupción deliberada de una actualización se prepararán aparte. **No deben realizarse por iniciativa propia.**

## 🗂️ Cómo se organizarán las pruebas

No probaremos todo a la vez. El trabajo se dividirá por páginas y por flujos para localizar mejor cualquier fallo.

### Páginas directas

Son comprobaciones rápidas de una pantalla concreta. Se entra en la página, se prueban sus botones y se confirma que responde como fue diseñada.


- abrir **Información** y revisar las versiones;
- entrar en **Movimiento** y comprobar sus controles;
- abrir **Temperatura** y revisar los valores mostrados;
- cambiar de idioma y comprobar los textos visibles.

Estas pruebas utilizarán identificadores como:

```text
BT-PAGE-001
```

### Flujos rápidos

Son funciones que recorren uno o varios pasos, pero pueden comprobarse en poco tiempo.

Un ejemplo es **Premove**: ejecutar los homings indicados y comprobar que cada eje se mueve en la dirección correcta, llega a su posición y termina sin golpes ni errores.

Estas pruebas utilizarán identificadores como:

```text
BT-FLOW-001
```

### Flujos largos

Son procesos con muchas pantallas, estados o variantes. Se dividirán en varias pruebas pequeñas para que resulte más fácil realizarlas y localizar los fallos.

El ejemplo principal es **PrintPause**, que puede incluir:

1. iniciar un G-code desde la pantalla;
2. iniciar un G-code desde Mainsail;
3. llegar al estado de impresión;
4. pausar desde la pantalla;
5. comprobar posición, temperatura y mensajes;
6. reanudar la impresión;
7. repetir desde Mainsail;
8. comprobar cancelación, cambio de filamento y otras variantes.

PrintPause será uno de los últimos procesos de la campaña o se publicará dividido en bloques independientes.

### Pruebas especiales

Algunas funciones tendrán su propia categoría:

```text
BT-SAFE-xxx   Seguridad, temperatura o movimiento
BT-PLR-xxx    Recuperación tras un corte eléctrico
BT-UPD-xxx    Instalación o recuperación de actualizaciones
BT-RESET-xxx  Restauración de fábrica
```

No es necesario memorizar estos códigos. Cada prueba llegará con su identificador ya asignado.

## 📝 Cómo realizar una prueba

Cada prueba indicará:

- el modelo compatible;
- desde qué pantalla hay que empezar;
- qué botón hay que pulsar;
- los pasos exactos;
- qué debería ocurrir;
- si implica movimiento o calentamiento;
- cuándo hay que detenerse;
- qué resultado se debe comunicar.

Seguid solamente los pasos indicados. Si una instrucción no está clara, preguntad antes de continuar.

Al describir lo ocurrido, utilizad el **título visible en la pantalla**. Indicad siempre desde qué pantalla llegasteis y qué botón pulsasteis.

## ✅ Cómo informar del resultado

Si todo funciona, será suficiente con responder:

```text
ID de prueba: BT-PAGE-001
Resultado: OK
Modelo: X4 Pro o X4 Plus
Observaciones: opcional
```

Estados que utilizaremos:

- **OK:** funcionó como se esperaba.
- **FALLO:** ocurrió algo diferente.
- **NO PROBADO:** todavía no se ha realizado.
- **NO APLICA:** no corresponde a ese modelo o configuración.
- **BLOQUEADO POR SEGURIDAD:** fue necesario detener la prueba.
- **PENDIENTE DE ACTUALIZACIÓN:** existe una corrección pendiente de instalar.
- **CORREGIDO, PENDIENTE DE REPETIR:** la corrección está instalada, pero falta comprobarla.
- **VALIDADO DESPUÉS DE ACTUALIZAR:** la prueba se repitió correctamente.

## 🐞 Si encontráis un problema

Cada problema debe comunicarse por separado. No intentéis interpretar el código ni averiguar la causa técnica: necesito saber **qué hicisteis y qué ocurrió**.

Podéis utilizar esta plantilla:

```text
ID de prueba:
Fecha y hora:
Modelo: X4 Pro / X4 Plus
Tamaño de eMMC:
Expansión seleccionada:
Idioma:
Página desde la que empezasteis:
Página en la que terminó:
Botón que pulsasteis:
Pasos realizados:
Resultado esperado:
Resultado real:
¿Ocurre siempre o solo algunas veces?:
¿Hubo movimiento?: Sí / No
¿Hubo calentamiento?: Sí / No
¿Existió algún riesgo?: Sí / No
Foto o vídeo, si está disponible:
Observaciones:
```

Ejemplo:

```text
ID de prueba: BT-FLOW-003
Página inicial: Movimiento
Botón: Home Y
Esperaba que se moviese el eje Y, pero se movió el eje X.
Apagué la impresora y no repetí la prueba por seguridad.
Resultado: BLOQUEADO POR SEGURIDAD
```
La coordinación de la beta añadirá después el identificador de incidencia, las versiones completas y los logs disponibles. Una incidencia corresponderá siempre a un único problema.

## 🔗 Seguimiento de una corrección

Cuando un fallo reciba una actualización, se conservará toda la relación:

```text
Prueba → Incidencia → Actualización → Repetición
```

Ejemplo:

```text
BT-FLOW-WIFI-002
→ BUG-2026-10-06-001
→ UPD-BETA-02
→ RETEST-UPD-BETA-02
→ OK
```

La lista de repetición incluirá:

- la prueba que fallaba;
- la comprobación de instalación;
- el reinicio posterior;
- las páginas o flujos relacionados;
- el resultado después de actualizar.

No será necesario repetir toda la campaña después de cada actualización. Se indicarán únicamente las pruebas afectadas y las comprobaciones relacionadas.

## ⚠️ Seguridad

Durante cualquier prueba con movimiento o calentamiento, permaneced junto a la impresora y mantened despejada la zona de trabajo.

Detened la prueba si observáis:

- un eje moviéndose en una dirección incorrecta;
- golpes o ruidos mecánicos anormales;
- la boquilla acercándose de forma peligrosa a la cama o a una pieza;
- calentamiento no solicitado;
- una temperatura que aumenta de forma inesperada;
- humo, olor a quemado o cableado caliente;
- cualquier comportamiento que pueda dañar la impresora o resultar peligroso.

> 🛑 No repitáis una situación peligrosa para conseguir una foto o un vídeo. Indicad **BLOQUEADO POR SEGURIDAD** y explicad brevemente lo ocurrido.

No cortéis la alimentación, forcéis una recuperación ni iniciéis una restauración de fábrica salvo que la prueba lo indique expresamente.

## 📷 Fotos, vídeos e información privada

Las fotos y vídeos solo serán necesarios cuando ayuden a entender el problema. Antes de publicarlos, comprobad que no muestren:

- contraseñas Wi-Fi;
- claves SSH;
- tokens o códigos privados;
- direcciones o datos personales;
- información que no esté relacionada con la prueba.

No compartáis fuera del grupo las imágenes, actualizaciones, enlaces ni documentos de esta beta.

## 📌 Reglas generales

- Realizad únicamente las pruebas asignadas.
- Describid lo que hicisteis y lo que ocurrió.
- Utilizad los nombres visibles en la pantalla.
- Comunicad cada problema por separado.
- Preguntad si alguna instrucción no está clara.
- No modifiquéis archivos internos de la impresora.
- No instaléis archivos sueltos ni paquetes no autorizados.
- No probéis el perfil Plus en una X4 Pro.
- No repitáis movimientos o calentamientos peligrosos.
- No compartáis el material de la beta fuera del grupo.

## 🤝 Objetivo

El proceso será sencillo:

```text
Beta-testing detecta y documenta
        ↓
Diagnóstico y corrección en desarrollo
        ↓
Se publica una actualización USB autorizada
        ↓
Beta-testing repite las pruebas afectadas
        ↓
Resultados estables
        ↓
Publicación de la versión final
```

El objetivo es comprobar **JeroMod-Tortillery X4** de forma ordenada, segura y fácil de seguir. Gracias por dedicar vuestro tiempo y vuestra impresora a estas pruebas.
