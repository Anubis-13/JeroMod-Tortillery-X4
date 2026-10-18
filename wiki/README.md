# 📚 Wiki de JeroMod-Tortillery X4

Esta wiki explica las funciones disponibles en la beta pública. No es una campaña de pruebas: podéis utilizar la impresora con normalidad y consultar únicamente el apartado que necesitéis.

## Antes de empezar

- Seleccionad siempre el modelo físico correcto.
- Consultad las advertencias antes de mover ejes, calentar o restaurar el sistema.
- Las opciones mostradas pueden variar según el modelo, la configuración y la actualización instalada.
- Cuando una función también pueda manejarse desde Mainsail, se indicará en su apartado.
- El soporte y las incidencias se gestionan únicamente en español.

## Índice

| Código | Guía | Contenido |
|---|---|---|
| `B00` | [Instalación de la imagen](00-instalacion-imagen.md) | Descarga, verificación, grabación y primer encendido |
| `B01` | [Bienvenida y primer arranque](01-bienvenida.md) | Idioma, eMMC, modelo, WiFi y calibraciones iniciales |
| `B02` | [Ajustes](02-ajustes.md) | Idioma, WiFi, NeoPixel, energía y ajustes avanzados |
| `B03` | [Herramientas](03-herramientas.md) | Movimiento, temperaturas y filamento |
| `B04` | [Menú de nivel](04-menu-nivel.md) | Z-Offset, tornillos, malla, PID y resonancias |
| `B05` | [Archivos e inicio de impresión](05-archivos-inicio-impresion.md) | USB, archivos, Pre-Impresión, Mainsail, finalizar y reimprimir |
| `B06` | [Controles durante la impresión](06-controles-durante-impresion.md) | Velocidad, flujo, ventilador, temperaturas, Z-Offset, LED y consola |
| `B07` | [Pausa, reanudación y cambio de filamento](07-pausa-reanudacion-filamento.md) | Pausa normal y cambio manual de filamento |
| `B08` | [Sensor de filamento](08-sensor-filamento.md) | Detección, aviso, ignorar, cargar y continuar |
| `B09` | [Recuperación tras corte eléctrico](09-recuperacion-corte-electrico.md) | PLR, reanudación y descarte de una recuperación |
| `B10` | [Actualizaciones USB](10-actualizaciones-usb.md) | Instalación, compatibilidad y errores de paquetes `.mksp` |
| `B11` | [Restauración de fábrica](11-restauracion-fabrica.md) | Opciones de borrado y restauración del sistema |
| `B12` | [Mensajes de error y recuperación](12-mensajes-error-recuperacion.md) | Almacenamiento, USB, Klipper, calibraciones y reinicios |

## Cómo informar de un fallo

Los Issues deben crearse mediante el formulario oficial y conservar este título:

```text
[BLOQUE][MODELO] Descripción breve
```

Ejemplo:

```text
[B04][X4 PLUS] La malla intenta medir fuera de la cama
```

Un Issue debe describir un solo problema. Indicad el nombre visible de la pantalla, el botón o icono utilizado y los pasos exactos. Si el problema también aparece en Mainsail, añadid ese dato en el mismo informe.

Los informes incompletos, duplicados, escritos en otro idioma o con varios problemas mezclados se cerrarán sin diagnóstico.

[Volver al README principal](../README.md)
