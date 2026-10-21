# 🧪 Beta pública de JeroMod-Tortillery X4

**JeroMod-Tortillery X4** es un proyecto independiente creado y desarrollado
por JeroMod para las impresoras **Artillery X4 Pro** y **Artillery X4 Plus**.
Esta versión es una beta pública: puede contener errores y debe utilizarse con
precaución.

> 🇪🇸 **La documentación, las consultas y las incidencias se gestionarán
> únicamente en español.**

Este repositorio contiene la documentación, las guías de uso, el registro de
incidencias y las actualizaciones autorizadas publicadas mediante **Releases**.
La imagen completa y el código interno no se alojan aquí.

## ⚠️ Aviso importante antes de instalar

Todo el desarrollo y las comprobaciones físicas se han realizado con una
**Artillery X4 Pro**. No dispongo de una X4 Plus para validar personalmente su
funcionamiento completo. La imagen incluye una configuración para la X4 Plus,
pero debe considerarse pendiente de validación real por usuarios de ese modelo.

Este proyecto no es un firmware oficial de Artillery. Es una beta independiente
que puede contener errores y no se garantiza su compatibilidad con todas las
revisiones de hardware, modificaciones o accesorios. Instalar la imagen
sustituye el sistema existente de la eMMC: conservad antes una copia funcional
del sistema que utilizabais.

Cada usuario decide si instala la beta y asume los riesgos derivados de su uso.
En la medida permitida por la legislación aplicable, JeroMod no se hace
responsable de impresiones fallidas, pérdida de configuraciones ni daños
provocados por una instalación incorrecta, una configuración inadecuada o el
uso de la impresora sin supervisión.

### Perfil de laminador

Por ahora **no se proporciona un perfil oficial de laminador** para OrcaSlicer,
Cura, PrusaSlicer u otros programas. Utilizad vuestro perfil habitual para el
modelo exacto de impresora y revisad especialmente las dimensiones, los límites
de la máquina y el G-code de inicio y final antes de imprimir.

No utilicéis un perfil de la X4 Pro en una X4 Plus ni uno de la X4 Plus en una
X4 Pro. Cuando mi perfil personal esté preparado y suficientemente comprobado,
lo compartiré por separado.

> 🛑 Supervisad las primeras impresiones, movimientos y calentamientos. Ante
> cualquier comportamiento inesperado, detened la impresora y consultad la
> documentación antes de continuar.

## 🇪🇸 Idioma y soporte

La documentación, las consultas y la gestión de incidencias se realizarán **únicamente en español**. Podéis utilizar un traductor, pero el contenido publicado en GitHub deberá estar en español.

## 🐞 Cómo informar de un problema

Los problemas se gestionarán únicamente mediante la sección **Issues** de este
repositorio y solo se atenderán en español. Cada Issue debe tratar un único
problema y utilizar uno de estos títulos:

```text
[FALLO] Descripción breve del problema
[WIKI] Descripción breve del problema de documentación
```

Ejemplos correctos:

```text
[FALLO] Home Y mueve el eje en dirección incorrecta
[FALLO] Pre-Impresión no muestra la miniatura
[FALLO] La actualización válida no aparece en pantalla
[WIKI] El apartado de conexión WiFi no explica cómo borrar una red
```

Los Issues incompletos, duplicados, escritos en otro idioma, con títulos como
«No funciona» o que mezclen varios problemas se cerrarán sin diagnóstico.
Deberán enviarse de nuevo con la información necesaria.

En un fallo indicad, como mínimo:

- modelo: X4 Pro o X4 Plus;
- versión de la imagen, SysLCD y TFT;
- apartado afectado: Ajustes, WiFi, Herramientas, Impresión, Actualizaciones u
  otro;
- si ocurrió desde la pantalla, Mainsail o ambos;
- pantalla inicial y botón, icono u opción utilizada;
- pasos exactos para reproducirlo;
- resultado esperado y resultado real;
- si hubo movimiento, calentamiento o algún riesgo;
- fotografías, vídeos o logs cuando sean útiles.

El mantenimiento del repositorio aplicará la etiqueta `fallo` a los problemas
del sistema y `documentación` a los problemas de la wiki.

Antes de informar:

1. Consultad la [wiki de funciones](wiki/README.md).
2. Buscad si ya existe un Issue con el mismo problema.
3. Si existe, añadid allí vuestro modelo, versiones y resultado.
4. Si no existe, abrid **un Issue por cada problema**.

No se utilizarán Issues para confirmar que algo funciona, pedir nuevas
funciones o solicitar modificaciones personales. Durante la beta se
priorizarán los fallos reproducibles del sistema actual.

> 🔐 No publiquéis contraseñas WiFi, claves SSH, tokens, direcciones ni otros
> datos privados. Revisad también las fotografías, vídeos y logs antes de
> adjuntarlos.

## 📥 Descarga de la imagen

La imagen se distribuirá mediante un enlace externo porque supera el tamaño máximo permitido para un archivo en GitHub.

**Enlace de descarga:**

[AQUÍ LA DESCARGA](https://drive.google.com/file/d/1r7LGBq6CZ-2WhnRB_oMauw3_ysZvVpYi/view?usp=drive_link)


## 📋 Datos del archivo publicado:

```text
Nombre: JeroMod_Tortillery_X4_Beta_001_FB1.0.5_LCD0.0.23_TFT0.165_8GB.img
Tamaño total en disco: 7.818.182.656 bytes
Tamaño equivalente: 7,28 GiB
SHA-256: 586EED3297EBDC4522E80F3D8E908681B2758531C6C7D0799B92A3EA61BE26FD
```

> 🔒 Antes de grabar la imagen, comprobad que el nombre, el tamaño y el SHA-256 coinciden exactamente con los publicados.

## 📋 Versiones de la imagen inicial

```text
Imagen: JeroMod-Tortillery X4 BETA-001
Firmware base: Tortillery v1.0.5
Sistema: JeroMod SYS v0.0.23
Pantalla: JeroMod TFT v0.165
```

Modelos incluidos:

- **Artillery X4 Pro:** modelo principal y físicamente validado.
- **Artillery X4 Plus:** perfil instalable, pendiente de validación física completa por usuarios con una X4 Plus real.

> 🛑 Seleccionad siempre el modelo físico correcto. No instaléis ni seleccionéis el perfil X4 Plus en una X4 Pro, ni el perfil X4 Pro en una X4 Plus.

## 📚 Wiki de funciones

La wiki explica el sistema por bloques:  

[ ENTRAR EN LA WIKI ](wiki/README.md)

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

Si encontráis un error, un enlace roto, información incompleta o una explicación
que no se entienda bien, abrid un Issue cuyo título comience por `[WIKI]`.
Indicad la página y el apartado concreto, explicando qué información debería
revisarse. No mezcléis en él un fallo de la impresora.

## 🔄 Actualizaciones USB

Las correcciones de la beta se publicarán en los
[Releases del repositorio](https://github.com/Anubis-13/JeroMod-Tortillery-X4/releases)
mediante paquetes autorizados con un nombre similar a:

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

- **Documentación (`wiki/`):** funcionamiento y procedimientos.
- **Issues:** fallos reproducibles con título `[FALLO]` y problemas de la wiki
  con título `[WIKI]`.
- **Discussions:** anuncios y dudas generales en español.
- **Releases:** actualizaciones USB autorizadas.
- **Enlace externo:** descarga de la imagen completa.

## 📜 Licencia y responsabilidad

Los componentes originales de JeroMod-Tortillery X4 se distribuyen bajo la
[GNU General Public License v3.0](LICENSE). Los programas y componentes de
terceros conservan sus respectivas licencias.

Este proyecto se proporciona gratuitamente, **tal cual y sin ninguna
garantía**. Su instalación y utilización se realizan bajo la responsabilidad
del usuario. En la medida permitida por la legislación aplicable, el autor no
será responsable de daños en la impresora, pérdida de configuraciones,
impresiones fallidas ni otras consecuencias derivadas de su instalación o uso.

JeroMod-Tortillery X4 es un proyecto independiente creado y desarrollado por
JeroMod. No está afiliado, patrocinado ni aprobado por Artillery.

Gracias por utilizar la beta y por comunicar los problemas de forma clara. Un informe bien preparado permite localizar y corregir un fallo mucho más rápido.
