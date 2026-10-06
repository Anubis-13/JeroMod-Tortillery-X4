# 🧪 Beta privada de JeroMod-Tortillery X4

Gracias por participar en las pruebas de **JeroMod-Tortillery X4**.

Este repositorio privado servirá para organizar las pruebas, comunicar incidencias y comprobar las correcciones que se publiquen durante la beta. El grupo es reducido para poder trabajar mejor y el contenido no debe compartirse fuera de él hasta que exista una imagen candidata para lanzamiento.

No es necesario saber programación, Klipper, Linux ni electrónica. Cada prueba tendrá instrucciones sencillas y se realizará utilizando la impresora y su pantalla de forma normal.

> ⏳ **El testeo todavía no ha comenzado.** No es necesario hacer nada hasta recibir la primera prueba.

## 📥 Descarga de la imagen inicial

La imagen principal se distribuirá mediante un enlace privado externo. Debido a su tamaño, **no estará alojada directamente en GitHub**.

**Enlace de descarga:**

```text
PENDIENTE DE AÑADIR
```

> 🔒 La imagen **BETA-01** debe descargarse únicamente desde el enlace publicado aquí.

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

## 📋 Versión inicial

Estas son las versiones de cada módulo al comenzar el testeo:

```text
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

El sistema de actualización mediante USB será una de las primeras funciones que utilizaremos, porque servirá para recibir las correcciones durante todo el testeo.

El paquete autorizado tendrá un nombre similar a:

```text
JM-T-X4_UPDATE_vX.X.XXX.mksp
```

Cada actualización deberá probarla **todo el grupo**, aunque esté destinada únicamente a la X4 Pro o a la X4 Plus. Esto permitirá comprobar tanto la instalación correcta como la protección entre modelos.

- En el modelo compatible, la actualización deberá instalarse y finalizar correctamente.
- En el modelo no compatible, el sistema deberá reconocer que el paquete pertenece a otro modelo y bloquear la instalación sin modificar nada.

Cada tester comunicará qué modelo ha utilizado y el resultado mostrado por la pantalla.

Si la pantalla indica que un archivo no es válido, pertenece a otro modelo o no puede instalarse, cancelad el proceso y comunicadlo.

> 🚫 Utilizad únicamente el paquete autorizado para esa prueba. No lo renombréis, no lo modifiquéis y no añadáis otros archivos o scripts al USB.

Después de actualizar no será necesario repetir todo el testeo. Se indicarán las pruebas afectadas y las comprobaciones relacionadas que deban repetirse.

Las pruebas de recuperación, rollback o interrupción deliberada de una actualización se prepararán aparte. **No deben realizarse por iniciativa propia.**

## 🧭 Cómo trabajaremos

Podéis utilizar la impresora y recorrer sus opciones con normalidad. No se trata de impedir que probéis o curioseéis por vuestra cuenta. Aun así, para que la beta avance y no volvamos continuamente sobre lo mismo, las comprobaciones oficiales seguirán un orden concreto.

El objetivo de esta fase es confirmar que las funciones actuales trabajan como fueron diseñadas. Las propuestas para cambiar el diseño o añadir funciones se pueden anotar, pero las revisaremos cuando la base esté terminada y estable. No significa que se vayan a ignorar; simplemente, si cambiamos y ampliamos cosas mientras validamos, el proceso puede hacerse eterno.

### Páginas y flujos

Habrá pruebas de dos tipos principales:

- **Pruebas de página:** comprobarán el proceso completo de una página concreta, sus botones, la información mostrada y el resultado de cada acción.
- **Pruebas de flujo:** comprobarán un proceso completo en el que intervienen varias páginas, acciones o estados, desde el inicio hasta el resultado final.

Las pruebas de página utilizarán identificadores como:

```text
BT-PAGE-001
```

Las pruebas de flujo utilizarán identificadores como:

```text
BT-FLOW-001
```

Una prueba rápida puede ser **Páginas de Herrmientas**: 

**En la pestaña movimiento:** realizar todos los homings indicados y comprobar que cada eje se mueve en la dirección correcta, llega a su posición y termina sin golpes ni errores.

**En la pestaña temperaturas:** enviar los perfiles de temperatura, parar. Poner temperaturas manual y ver límites.

**En la pestaña extruir:** realizar extrusiones y retracciones controlar temperaturas y errores.

Un proceso largo puede ser **Imprimir**. En él intervienen el inicio de una impresión desde la pantalla o desde Mainsail, la llegada al estado de impresión, la pausa, el comportamiento durante la pausa, la reanudación y otras variantes. Por su tamaño, este flujo se dejará para el final o se dividirá en varias fichas independientes. Aunque este puede ser una des las últimas pruebas por todo lo que conlleva. Ya que algún error puede venir de otra página con la que comparta programación.

También existirán identificadores específicos para pruebas especiales:

```text
BT-SAFE-xxx   Seguridad, temperatura o movimiento
BT-PLR-xxx    Recuperación tras un corte eléctrico
BT-UPD-xxx    Instalación o recuperación de actualizaciones
BT-RESET-xxx  Restauración de fábrica
```

No es necesario memorizar estos códigos. Cada ficha llegará con su identificador ya asignado.

### Fichas de prueba

Os pasaré una ficha por cada prueba. La ficha indicará:

- el identificador de la prueba;
- el modelo con el que debe realizarse;
- desde qué pantalla hay que empezar;
- qué botones hay que pulsar;
- los pasos que deben seguirse;
- qué debería ocurrir;
- si implica movimiento, calentamiento o algún riesgo;
- qué información hay que comunicar al terminar.

Seguid los pasos de la ficha en el orden indicado. Si alguna instrucción no está clara, preguntad antes de continuar.

Si todo funciona correctamente, cerraremos ese módulo y pasaremos al siguiente. Si aparece un problema, lo registraremos, se preparará la corrección y se entregará mediante una actualización. Después repetiremos las pruebas afectadas y, cuando todo quede validado, cerraremos el módulo.

El proceso de cada bloque será:

```text
Prueba
  ↓
Resultado correcto → módulo cerrado
  ↓
Siguiente módulo
```

Si aparece un fallo:

```text
Prueba
  ↓
Incidencia
  ↓
Corrección y actualización
  ↓
Repetición de las pruebas afectadas
  ↓
Validación y cierre del módulo
```

Este proyecto lleva cerca de un año de trabajo y durante mucho tiempo se dieron demasiadas vueltas a distintos apartados. Trabajar por fichas y cerrar cada módulo antes de pasar al siguiente es la forma más clara de avanzar y terminarlo.

### Uso libre fuera de la prueba

Si mientras utilizáis la impresora encontráis algo fuera de la prueba que estamos realizando, anotad qué hicisteis y qué ocurrió. Lo revisaremos cuando lleguemos a esa página o flujo.

No hace falta abrir en ese momento una nueva línea de trabajo ni repetir el fallo varias veces. Si existe riesgo térmico o mecánico, detened la prueba y comunicadlo inmediatamente.

### ✅ Cómo informar del resultado

Si todo funciona, bastará con responder:

```text
ID de prueba: BT-PAGE-001
Resultado: OK
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

### 🐞 Si encontráis un problema

Cada problema debe comunicarse por separado. No es necesario intentar averiguar la causa técnica ni interpretar el código. Necesito saber qué hicisteis, desde dónde llegasteis y qué ocurrió.

Utilizad el título que aparece visible en la pantalla e indicad siempre qué botón pulsasteis.

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

La coordinación de la beta añadirá después el identificador de incidencia, las versiones completas y los logs disponibles. Cada fallo generará una ficha independiente y cada ficha corresponderá a un único problema.

### Repetición después de una actualización

Cuando una actualización corrija un fallo, se conservará la relación completa:

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

La ficha de repetición incluirá:

- la prueba que fallaba;
- la comprobación de instalación;
- el reinicio posterior;
- las páginas o flujos relacionados;
- el resultado después de actualizar.

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

> 🛑 No repitáis una situación peligrosa para conseguir una foto o un vídeo. Si es necesario detener la prueba, indicad **BLOQUEADO POR SEGURIDAD** y explicad brevemente lo ocurrido.

No cortéis la alimentación, forcéis una recuperación ni iniciéis una restauración de fábrica salvo que la ficha lo indique expresamente.

## 📷 Fotos, vídeos e información privada

Las fotos y vídeos solo serán necesarios cuando ayuden a entender el problema. Antes de publicarlos, comprobad que no muestren:

- contraseñas Wi-Fi;
- claves SSH;
- tokens o códigos privados;
- direcciones o datos personales;
- otra información que no esté relacionada con la prueba.

No compartáis fuera del grupo las imágenes, actualizaciones, enlaces ni documentos de esta beta.

## 🧰 Pruebas especiales

Las siguientes pruebas se dejarán para fichas o fases específicas del testeo:

- impresión completa y todas sus variantes;
- pausa, reanudación y cambio de filamento;
- recuperación tras un corte eléctrico;
- recuperación o rollback forzado de una actualización;
- restauración de fábrica;
- validación física completa de la X4 Plus.

No realicéis estas pruebas por iniciativa propia. Se proporcionarán instrucciones concretas cuando llegue el momento.

## 📌 Reglas generales

- Podéis utilizar la impresora con normalidad, pero las pruebas oficiales deben seguir su ficha.
- Describid lo que hicisteis y lo que ocurrió, sin intentar interpretar el código.
- Utilizad los nombres visibles en la pantalla.
- Indicad desde qué pantalla llegasteis y qué botón pulsasteis.
- Comunicad cada problema por separado.
- Preguntad si alguna instrucción no está clara.
- No modifiquéis archivos internos de la impresora.
- No instaléis archivos sueltos ni paquetes no autorizados.
- No probéis el perfil Plus en una X4 Pro.
- No repitáis movimientos o calentamientos peligrosos.
- No cortéis la alimentación sin una prueba preparada.
- No utilicéis una restauración de fábrica para intentar resolver una incidencia.
- No compartáis el material de la beta fuera del grupo.

## 🤝 Objetivo

El proceso general será:

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
Imagen candidata → publicación final
```

El objetivo es comprobar **JeroMod-Tortillery X4** de forma ordenada, segura y fácil de seguir. Gracias por dedicar vuestro tiempo y vuestra impresora a estas pruebas.
