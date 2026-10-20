# 🧪 Beta pública de JeroMod-Tortillery X4

**JeroMod-Tortillery X4** es una modificación comunitaria para las impresoras **Artillery X4 Pro** y **Artillery X4 Plus**. Esta versión es una beta pública: puede contener errores y debe utilizarse con precaución.

Este repositorio contiene únicamente la documentación, las guías de uso y el registro de incidencias. La imagen, las actualizaciones y el código interno no se alojan aquí.

> ⚠️ Este proyecto no es un firmware oficial de Artillery. Instalar la imagen sustituye el sistema existente de la eMMC. Antes de comenzar, conservad una copia funcional del sistema que utilizabais.

## 🇪🇸 Idioma y soporte

La documentación, las consultas y la gestión de incidencias se realizarán **únicamente en español**. Podéis utilizar un traductor, pero el contenido publicado en GitHub deberá estar en español.

## 🐞 Antes de abrir una incidencia

Solo se revisarán incidencias enviadas mediante el formulario oficial y con el título obligatorio:

```text
[BLOQUE][MODELO] Descripción breve del problema
```

Ejemplos correctos:

```text
[B03][X4 PRO] Home Y mueve el eje en dirección incorrecta
[B05][X4 PLUS] Pre-Impresión no muestra la miniatura
[B10][X4 PRO] La actualización válida no aparece en pantalla
```

Los Issues incompletos, duplicados, escritos en otro idioma, con un título genérico o que mezclen varios problemas se cerrarán sin diagnóstico. Deberán enviarse de nuevo siguiendo el formulario.

Antes de informar:

1. Consultad la [wiki de funciones](wiki/README.md).
2. Buscad si ya existe un Issue con el mismo problema.
3. Si existe, añadid allí vuestro modelo, versiones y resultado.
4. Si no existe, abrid **un Issue por cada problema**.

No se utilizarán Issues para confirmar que algo funciona, pedir nuevas funciones o solicitar modificaciones personales. Durante la beta se priorizarán los fallos reproducibles del sistema actual.

## 📥 Descarga de la imagen

La imagen se distribuirá mediante un enlace externo porque ocupa más de 7 GB y no se alojará directamente en GitHub.

**Enlace de descarga:**

[Descarga "Imagen Beta"]([https://drive.google.com/uc?export=download&id=1acVj2qs3dZN3fFy-GJ40GVE3lyYIc95-](https://drive.google.com/file/d/1acVj2qs3dZN3fFy-GJ40GVE3lyYIc95-/view?usp=sharing))

Datos del archivo publicado:

```text
Nombre: JeroMod_Tortillery_X4_Beta_001_FB1.0.5_LCD0.0.23_TFT0.164_8GB.img
Tamaño total en disco: 7.818.182.656 bytes
Tamaño equivalente: 7,28 GiB
SHA-256: BB2461F967E7597D967AF47A7C05E349E31DE65DCB70F21944C996A7404617BF
```

> 🔒 Antes de grabar la imagen, comprobad que el nombre, el tamaño y el SHA-256 coinciden exactamente con los publicados.

## 📋 Versiones de la imagen inicial

```text
Imagen: JeroMod-Tortillery X4 BETA-01
Firmware base: Tortillery v1.0.5
Sistema: JeroMod SYS v0.0.23
Pantalla: JeroMod TFT v0.164
```

Modelos incluidos:

- **Artillery X4 Pro:** modelo principal y físicamente validado.
- **Artillery X4 Plus:** perfil instalable, pendiente de validación física completa por usuarios con una X4 Plus real.

> 🛑 Seleccionad siempre el modelo físico correcto. No instaléis ni seleccionéis el perfil X4 Plus en una X4 Pro, ni el perfil X4 Pro en una X4 Plus.

## 📚 Wiki de funciones

La [wiki](wiki/README.md) explica el sistema por bloques:

- instalación y primer arranque;
- ajustes, WiFi, NeoPixel y energía;
- movimiento, temperatura y filamento;
- nivelación y calibraciones;
- archivos e impresión;
- controles durante una impresión;
- pausa, reanudación y cambio de filamento;
- sensor de filamento;
- recuperación tras un corte eléctrico;
- actualizaciones USB;
- restauración de fábrica;
- mensajes de error y recuperación.

Las páginas no son exámenes ni listas de pruebas. Explican cómo funciona cada apartado, qué precauciones requiere y qué información debe incluirse si aparece un fallo.

## 🔄 Actualizaciones USB

Las correcciones de la beta se distribuirán mediante paquetes autorizados con un nombre similar a:

```text
JM-T-X4_UPDATE_vX.X.XXX.mksp
```

Consultad siempre la [guía de actualizaciones USB](wiki/10-actualizaciones-usb.md) antes de instalar un paquete.

Si la pantalla indica que un archivo no es válido, pertenece a otro modelo o no puede instalarse, cancelad el proceso y comunicad exactamente el mensaje mostrado.

> 🚫 No renombréis ni modifiquéis el paquete. No instaléis archivos sueltos, scripts ni actualizaciones obtenidas fuera de los enlaces autorizados.

Las pruebas de recuperación, rollback o interrupción deliberada de una actualización se anunciarán expresamente. **No deben realizarse por iniciativa propia.**

## ⚠️ Seguridad

- Permaneced junto a la impresora durante movimientos, calentamientos y calibraciones.
- Detened el proceso ante movimientos incorrectos, golpes, calentamiento inesperado, humo, olor a quemado o cualquier riesgo.
- No repitáis una situación peligrosa para conseguir una fotografía o un vídeo.
- No cortéis la alimentación salvo que una guía indique expresamente que se está comprobando la recuperación tras un corte.
- No modifiquéis archivos internos para intentar corregir un fallo antes de comunicarlo.
- No publiquéis contraseñas WiFi, claves SSH, tokens, direcciones personales ni otros datos privados.

## 💬 Uso de GitHub

- **Wiki del repositorio:** funcionamiento y procedimientos.
- **Issues:** únicamente fallos reproducibles y separados.
- **Discussions:** anuncios y dudas generales en español.
- **Drive externo:** imagen y actualizaciones autorizadas.

## 📜 Licencia

Esta distribución beta de JeroMod-Tortillery X4 es de uso gratuito, pero **no
es actualmente software de código abierto**. La imagen y las actualizaciones
pueden descargarse e instalarse para uso personal en una impresora compatible,
pero no pueden venderse, modificarse, reempaquetarse ni volver a distribuirse
sin autorización.

Cuando el sistema esté estable, JeroMod podrá publicar el código y otros
componentes del proyecto con una licencia diferente. Esa publicación y su
alcance se anunciarán expresamente cuando corresponda.

Consultad la [licencia completa](LICENSE.md) antes de descargar o instalar la
beta. Los componentes de terceros conservan sus propias licencias.

Gracias por utilizar la beta y por comunicar los problemas de forma clara. Un informe bien preparado permite localizar y corregir un fallo mucho más rápido.
