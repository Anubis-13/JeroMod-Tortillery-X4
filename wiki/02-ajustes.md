# ⚙️ B02 — Ajustes

Desde la pantalla principal, pulsad el **icono del engranaje**. El menú contiene Idioma, Perfiles temperatura, Acciones de sitema, Ajustes Wifi, Ajuste Neopixel, Opciones de energía y Ajustes avanzados.

## Idioma

Permite cambiar el idioma de la pantalla. La selección se conserva al salir. Algunos nombres descritos en esta wiki corresponden al idioma español.

## Perfiles temperatura

Guarda las temperaturas de boquilla y cama utilizadas por los accesos PLA, ABS, PETG y TPU de **Herramientas**.

| Perfil | Boquilla inicial | Cama inicial |
|---|---:|---:|
| PLA | 200 °C | 60 °C |
| ABS | 245 °C | 100 °C |
| PETG | 225 °C | 70 °C |
| TPU | 220 °C | 60 °C |

Modificar un perfil cambia los objetivos enviados cuando se pulsa ese material; no inicia el calentamiento por sí mismo.

## Acciones de sitema

En la pantalla aparece escrito **Acciones de sitema**. La opción **Pregunta Home XYZ inicio** está reservada para posibles comportamientos futuros y actualmente no requiere ninguna acción del usuario.

## Ajustes Wifi

La lista muestra hasta seis redes por página, su intensidad y la dirección IP cuando existe conexión.

- **Aspa verde:** red guardada y conectada.
- **Aspa blanca:** red guardada, pero no conectada actualmente.
- Pulsación normal: conectar o abrir la introducción de contraseña.
- Pulsación mantenida sobre una red guardada: eliminarla.
- Buscar/Actualizar: repetir la búsqueda.

El sistema puede conservar varias redes. Al seleccionar otra red guardada debe conectarse sin solicitar de nuevo la contraseña. Tras borrar una red, la búsqueda se actualiza y puede volver a aparecer sin aspa si sigue disponible.

## Ajuste Neopixel

Permite elegir el color para Inicio/Reposo, Calentar, Homing/Calibrar, Impresión, Pausa/Cambio Filamento, Finalizado, Parada y Error/Restart_Firmware.

Cada estado ofrece **Predefinido**, **Apagar** y una paleta de colores. La selección se guarda por separado para cada estado.

## Opciones de energía

- **Apagar sistema:** prepara Linux y Klipper para cortar la alimentación de forma segura.
- **Reiniciar firmware:** reinicia Klipper sin reiniciar todo el sistema.
- **Reiniciar sistema:** reinicia Linux, la pantalla y los servicios.

No utilicéis estas acciones mientras la impresora se mueve, calienta o imprime. Durante un reinicio, Mainsail perderá temporalmente la conexión.

## Ajustes avanzados

- **Brillo:** intensidad de la pantalla.
- **Sonido:** activa el pitido; su icono cambia en la pantalla principal.
- **Sensor filamento:** activa la detección; al desactivarlo desaparece su icono de la pantalla principal.
- **Corte energía:** activa la recuperación tras un corte; al desactivarlo desaparece su icono.
- **Ventiladores Sitema:** configura los modos automáticos.
- **Info sistema:** muestra modelo, dimensiones y versiones.
- **Restaurar:** abre las opciones de restauración de fábrica.

### Ventiladores Sitema

Ventilador de boquilla:

- **KLIPPER:** control original y control manual disponible en Mainsail.
- **DYNAMIC:** adapta la velocidad a la temperatura.
- **SILENT:** reduce ruido manteniendo la protección térmica.

Ventilador de placa:

- **KLIPPER**, **DYNAMIC**, **MEDIUM** y **SILENT**.

> En modo **KLIPPER** pueden controlarse manualmente desde Mainsail. Hacedlo únicamente con la impresora fría y sin una impresión activa, y detened nuevamente los ventiladores al terminar.

### Info sistema

Debe identificar el modelo y sus dimensiones:

- X4 Pro: **240 × 240 × 260 mm**.
- X4 Plus: **300 × 300 × 400 mm**.

También muestra las versiones de firmware base, SysLCD, TFT, Klipper, Moonraker y Mainsail, además de dos códigos QR: grupo de Artillery y Facebook.

## Informar de un fallo de B02

```text
[B02][X4 PRO] Una red guardada no muestra el aspa blanca
```

Indicad el apartado, el nombre visible de la opción, el estado anterior y posterior y si el mismo cambio se refleja en Mainsail o en la pantalla principal.

[Volver al índice](README.md)
