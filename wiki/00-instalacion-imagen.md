# 💾 B00 — Instalación de la imagen

Esta guía describe la preparación de la eMMC y el primer encendido. La descarga autorizada, el nombre, el tamaño y el SHA-256 se publican en el [README principal](../README.md).

## Antes de grabar

1. Confirmad que la imagen corresponde a **JeroMod-Tortillery X4**.
2. Verificad el SHA-256 antes de descomprimirla o grabarla.
3. Conservad una copia funcional de vuestra eMMC original.
4. Identificad correctamente la unidad de la eMMC antes de iniciar la escritura.

La imagen base está preparada para una eMMC de 8 GB. Si se instala en una unidad mayor, el asistente puede ofrecer la ampliación del espacio durante la Bienvenida.

## Grabación

Utilizad una herramienta de escritura de imágenes compatible con archivos `.img`. Seleccionad la imagen descargada y la eMMC correcta. La grabación elimina el contenido anterior de la unidad seleccionada.

Cuando la herramienta termine:

1. Expulsad la eMMC de forma segura.
2. Instaladla correctamente en la impresora.
3. Comprobad conexiones y orientación antes de encender.
4. Dejad libres la cama y todos los ejes.
5. Encended la impresora y esperad al asistente de Bienvenida.

No interrumpáis el primer arranque aunque la pantalla tarde, se reinicie o pierda momentáneamente la conexión con Klipper.

## Si no arranca

No grabéis repetidamente sin revisar primero:

- nombre y SHA-256 de la imagen;
- resultado de la herramienta de grabación;
- orientación y conexión de la eMMC;
- alimentación de la impresora;
- mensajes visibles en pantalla.

## Informar de un fallo de B00

Título:

```text
[FALLO] Descripción breve
```

Indicad herramienta de grabación, tamaño de eMMC, verificación SHA-256, pantalla alcanzada y mensaje exacto. No publiquéis imágenes completas de discos, claves ni datos privados.

[Volver al índice](README.md)
