# 🖨️ B05 — Archivos e inicio de impresión

El **icono de archivo/impresión** de la pantalla principal abre el explorador. Desde aquí pueden iniciarse archivos almacenados en la impresora o en un USB. También pueden iniciarse trabajos desde Mainsail.

## Conectar un USB

Al conectar un dispositivo compatible aparece el indicador USB. El explorador utiliza una vista unificada: en la raíz de archivos aparece la carpeta **usb** junto a los archivos internos.

Si el USB se conecta o retira mientras el explorador, **Pre-Impresión** o la confirmación están abiertos, aparece un mensaje de actualización y la lista vuelve a cargarse.

No retiréis el USB mientras se está leyendo un archivo o mientras imprime un trabajo iniciado desde él.

## Explorador de archivos

- Las carpetas aparecen antes que los archivos.
- Se muestran archivos `.gcode` y `.3mf` compatibles.
- Las flechas inferiores cambian de página cuando existen más elementos.
- La flecha de regreso sube una carpeta; desde la raíz vuelve a la pantalla principal.
- Si no existen archivos imprimibles aparece **No hay archivos para imprimir en la impresora**.

## Pre-Impresión

Al seleccionar un archivo se carga la miniatura y la información disponible:

- nombre;
- tiempo estimado;
- material;
- peso;
- longitud de filamento.

Los datos dependen de lo que haya escrito el laminador en el G-code. Una miniatura o un campo ausente no siempre significa que el archivo sea inválido.

El icono de la papelera abre **¿Desea realmente eliminar el archivo?**. **Confirmar** borra el archivo seleccionado; **Cancelar** regresa sin eliminarlo.

## Iniciar desde la pantalla

**Imprimir** abre **¿Imprimir este modelo?**. Al confirmar, la pantalla pasa a la preparación, realiza los pasos definidos por el G-code y muestra el trabajo activo. Pulsad Confirmar una sola vez y esperad.

La pantalla de impresión muestra el nombre, miniatura, estado, temperaturas, tiempo, porcentaje, velocidad, flujo, ventilador y Z-Offset disponibles.

## Iniciar desde Mainsail

Un archivo iniciado en Mainsail se detecta automáticamente y abre la pantalla de impresión. Si aparece la elección:

- **G-CODE:** utiliza los ajustes enviados por el laminador.
- **MANUAL:** aplica los factores guardados en **Ajuste velocidades**.

No hay que iniciar el mismo archivo otra vez desde la pantalla. El nombre, estado, temperaturas y progreso deben mantenerse sincronizados con Mainsail.

## Finalizar y reimprimir

Al completar el trabajo se muestra el 100 % y después **¡Impresión completa!**:

- **Finalizar:** cierra el trabajo y vuelve a la pantalla principal.
- **Reimprimir:** inicia de nuevo el mismo archivo.

## Detener una impresión

El icono de parada abre **¿Desea detener la impresión?**. **Cancelar** vuelve al trabajo. **Confirmar** cancela la impresión, detiene los calentadores, realiza la secuencia segura de parada y regresa a la pantalla principal.

Esperad mientras se procesa la parada y no pulséis repetidamente. Las variantes de pausa y filamento se explican en B07 y B08.

## Informar de un fallo de B05

```text
[B05][X4 PRO] Reimprimir inicia un archivo diferente
```

Indicad si el archivo estaba en USB, almacenamiento interno o Mainsail; nombre visible; pantalla inicial; acción realizada; estado mostrado y si el trabajo llegó a calentar o moverse.

[Volver al índice](README.md)
