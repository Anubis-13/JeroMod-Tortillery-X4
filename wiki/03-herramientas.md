# 🛠️ B03 — Herramientas

Desde la pantalla principal, pulsad el **icono de herramientas**. La barra superior contiene, en este orden:

1. una cruz de flechas: movimiento;
2. un termómetro: temperaturas;
3. una boquilla con flechas arriba y abajo: filamento.

## Movimiento

Al entrar, realizad primero **ALL Homing**. Los movimientos manuales permanecen bloqueados hasta que la impresora conoce la posición de los ejes.

Después pueden utilizarse:

- Home X, Home Y y Home Z;
- pasos de 0,1 mm, 1 mm y 10 mm;
- movimientos `+` y `−` de X, Y y Z;
- liberación de motores.

Tras liberar motores debe realizarse de nuevo Home antes de confiar en las coordenadas. Los movimientos enviados desde los controles normales de Mainsail también actualizan la posición mostrada en pantalla.

> 🛑 Detened la impresora si un eje se mueve en la dirección equivocada, golpea un límite o la boquilla se acerca peligrosamente a la cama.

## Temperaturas

La pantalla muestra la temperatura actual y objetivo de boquilla y cama. Puede aplicar los perfiles PLA, ABS, PETG y TPU guardados en **Ajustes → Perfiles temperatura**, aceptar valores manuales y detener cada calentador por separado.

Límites admitidos:

- boquilla: hasta **350 °C**;
- cama: hasta **120 °C**.

Un valor superior muestra un aviso rojo y no debe aplicarse. La pantalla y Mainsail deben mostrar los mismos objetivos.

## Filamento

Permite definir longitud y velocidad, y después **Extruir** o **Retraer**.

- Longitud admitida: **10–350 mm**.
- Velocidad admitida: **10–360**.
- Temperatura mínima para mover el extrusor: aproximadamente **180 °C**.

Con la boquilla fría aparece **Boquilla con baja temperatura** y el extrusor no se mueve. Utilizad valores cortos y moderados al cargar o retirar filamento y detened el calentamiento al terminar.

## Mainsail

En este apartado pueden utilizarse los controles normales de movimiento y temperatura. No ejecutéis macros desconocidas para reproducir el funcionamiento de los botones de pantalla.

## Informar de un fallo de B03

```text
[FALLO] Home Z no regresa a Herramientas
```

Indicad pantalla, eje o calentador, valor utilizado, dirección observada, posición mostrada en Mainsail y si hubo riesgo térmico o mecánico.

[Volver al índice](README.md)
