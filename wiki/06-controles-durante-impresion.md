# 🎛️ B06 — Controles durante la impresión

Este bloque reúne **Ajuste velocidades** y los controles disponibles cuando un trabajo ya está activo. Los cambios pueden realizarse desde la pantalla o desde Mainsail y deben mantenerse sincronizados.

## Ajuste velocidades

Desde la pantalla principal, el acceso de ajuste permite guardar valores manuales para:

- factor de velocidad: **0–200 %**;
- factor de flujo: **0–200 %**;
- ventilador de capa: **0–100 %**.

También permite elegir si el ventilador sigue el G-code o utiliza el valor manual. Estos valores sirven como preferencia; no mueven ni calientan la impresora por sí solos.

Cuando un trabajo se inicia desde Mainsail y el modo manual está preparado, la pantalla puede preguntar si debe utilizar **G-CODE** o **MANUAL**. La elección se aplica a ese trabajo.

## Herramientas del trabajo activo

Las herramientas permanecen bloqueadas durante las primeras fases de preparación y se habilitan cuando el trabajo ha comenzado correctamente.

### Temperatura de boquilla y cama

Permiten cambiar los objetivos durante la impresión. Un cambio también debe verse en Mainsail. No reduzcáis una temperatura hasta un valor incompatible con el material mientras continúa extruyendo.

### Velocidad

Modifica el factor de velocidad de Klipper. El valor normal es 100 %. Los cambios realizados desde Mainsail deben reflejarse en la pantalla y viceversa.

### Flujo

Modifica el factor de extrusión. El valor normal es 100 %. Utilizad cambios moderados: un flujo excesivo puede provocar sobreextrusión o presión anormal.

### Ventilador de capa

Controla el ventilador del modelo entre 0 y 100 %. No debe confundirse con los ventiladores de sistema configurados en Ajustes avanzados.

### Z-Offset durante la impresión

Permite corregir ligeramente la distancia de la boquilla. Utilizad pasos pequeños. Al terminar el trabajo, si el valor cambió, el sistema puede preguntar si debe guardarse o descartarse.

> 🛑 Detened el trabajo si la boquilla roza o presiona la cama. No intentéis corregir una diferencia grande durante una impresión.

## LED

El control LED permite cambiar el estado de iluminación durante el trabajo. Los colores automáticos proceden de **Ajuste Neopixel**.

## Consola y macros

La consola muestra mensajes de Klipper y permite enviar comandos. El apartado de macros presenta las macros disponibles en el sistema.

No ejecutéis comandos o macros cuyo efecto no conozcáis. Una orden enviada desde la consola puede mover, calentar, pausar o cancelar la impresora sin una confirmación adicional.

## Mainsail

Para comparar valores, utilizad los controles normales de velocidad, flujo, ventilador y temperatura de Mainsail. Si una cifra tarda unos instantes en actualizarse, esperad antes de volver a pulsar; no enviéis varios cambios seguidos para forzarla.

## Informar de un fallo de B06

```text
[B06][X4 PLUS] El factor de velocidad no se actualiza en Mainsail
```

Indicad origen del trabajo, control utilizado, valor anterior, valor solicitado, valor final en pantalla y Mainsail, y si el problema desaparece al volver a 100 %.

[Volver al índice](README.md)
