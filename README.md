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
Nombre: JeroMod_Tortillery_X4_Beta_001_FB1.0.5_LCD0.0.23_TFT0.164_8GB.img
Tamaño: 7.818.182.656 bytes
Tamaño aproximado: 7,281 GiB
SHA-256: BB2461F967E7597D967AF47A7C05E349E31DE65DCB70F21944C996A7404617BF
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

Las pruebas se publicarán poco a poco y estarán organizadas por **bloques**. Cada bloque recorrerá una página completa, un menú o un proceso formado por varias pantallas.

Cada guía indicará:

- dónde empezar y qué botones pulsar;
- qué debe ocurrir;
- si también hay que comprobar algo en Mainsail;
- si existe movimiento, calentamiento o algún riesgo.

Seguid el orden indicado y preguntad si algún paso no está claro. Si todo funciona, cerraremos el bloque. Si aparece un fallo, se corregirá, recibiréis una actualización y repetiremos solamente las partes afectadas.

Podéis utilizar y explorar la impresora con normalidad. Si encontráis algo fuera del bloque actual, anotad qué hicisteis y qué ocurrió; lo revisaremos cuando lleguemos a esa función. Las propuestas para cambiar el diseño o añadir funciones se estudiarán cuando la base actual esté terminada y estable, es decir cuando ya sea una versión pública. Aunque realmente solo me interesa añadir canBus de Makerbase o Bigtreetech y quizás algo para colores(Esto último lo mismo ya tengo otra impresora o ya se acabó las ganas de seguir con el proyecto). Por eso me interesa cerrar lo que hay y no salir de ahí. Dejar un sitema con más posibilidades que el oficial, pero cerrarlo siendo estable.

## ✅ Cómo informar del resultado

Si todo funciona, bastará con responder:

```text
Bloque o prueba:
Resultado: OK
Modelo: X4 Pro / X4 Plus
Observaciones: opcional
```

Si encontráis un problema, comunicad cada fallo por separado e indicad:

```text
Bloque o prueba:
Modelo:
Pantalla inicial:
Botón pulsado:
Pasos realizados:
Qué esperabais:
Qué ocurrió:
¿Ocurre siempre?:
¿Hubo movimiento, calentamiento o riesgo?:
Foto o vídeo, si ayuda:
```

Describid lo que hicisteis y utilizad los nombres visibles en la pantalla. No es necesario buscar la causa ni interpretar el código.

## ⚠️ Seguridad y normas básicas

- Permaneced junto a la impresora durante pruebas con movimiento o calentamiento.
- Detened la prueba ante movimientos incorrectos, golpes, calentamiento inesperado, humo, olor a quemado o cualquier riesgo.
- No repitáis una situación peligrosa para conseguir una foto o un vídeo.
- No cortéis la alimentación, forcéis una recuperación ni confirméis una restauración de fábrica salvo que la guía lo indique.
- No modifiquéis archivos internos ni instaléis paquetes no autorizados.
- No mostréis contraseñas WiFi, claves SSH, tokens ni información privada.
- No compartáis fuera del grupo las imágenes, enlaces, actualizaciones o documentos de esta beta.

## 🤝 Objetivo

```text
Probar un bloque
        ↓
Corregir los fallos encontrados
        ↓
Actualizar y repetir lo necesario
        ↓
Cerrar el bloque y pasar al siguiente
        ↓
Cerrar todos los bloques
        ↓
Imagen candidata de lanzamiento público
```

El objetivo es comprobar **JeroMod-Tortillery X4** de forma ordenada, segura y fácil de seguir. Gracias por dedicar vuestro tiempo y vuestra impresora a estas pruebas.
