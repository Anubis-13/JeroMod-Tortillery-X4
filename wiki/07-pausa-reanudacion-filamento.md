# ⏸️ B07 — Pausa, reanudación y cambio de filamento

La pausa normal y el cambio de filamento utilizan el estado de pausa de Klipper, pero son procesos diferentes. Esperad siempre a que el cabezal termine su movimiento antes de tocar la pieza o el filamento.

## Pausar desde la pantalla

El icono de pausa abre una confirmación. Al confirmar:

1. Klipper pausa el trabajo.
2. El cabezal se aparta según la configuración.
3. La pantalla muestra **Impresión pausada**.
4. El control cambia a reanudación.

Cancelar la confirmación vuelve a la impresión sin pausarla.

## Reanudar

Pulsad reanudar una sola vez. La interfaz puede bloquearse brevemente mientras Klipper cambia de `paused` a `printing`. El cabezal regresa al trabajo y la pantalla recupera **Imprimiendo**.

No enviéis simultáneamente Reanudar desde la pantalla y desde Mainsail.

## Pausa desde Mainsail

Una pausa solicitada desde Mainsail debe reflejarse en la pantalla. La reanudación puede realizarse desde uno de los dos sitios, pero no desde ambos a la vez.

## Cambio de filamento

Cuando el sistema recibe la orden de cambio de filamento —por ejemplo desde el G-code o una macro compatible— espera a que Klipper quede pausado y abre la pantalla correspondiente.

La pantalla permite retirar y cargar filamento con movimientos controlados. Mantened la boquilla a una temperatura adecuada y confirmad que el nuevo filamento sale correctamente antes de continuar.

Al finalizar, el sistema ejecuta la secuencia de cierre del cambio, vuelve a la pantalla de impresión y reanuda el trabajo.

## Precauciones

- No tiréis del filamento mientras el extrusor está moviéndose.
- No reanudéis si la boquilla está fría o el filamento no está cargado.
- Retirad el material purgado antes de que el cabezal vuelva a la pieza.
- No utilicéis Stop como sustituto de Pausa si pretendéis continuar el trabajo.
- Si aparece un aviso del sensor de filamento, seguid B08 en lugar de ignorarlo como una pausa normal.

## Informar de un fallo de B07

```text
[FALLO] Reanudar deja la pantalla en Impresión pausada
```

Indicad dónde se solicitó la pausa, estado mostrado en Mainsail, pantalla alcanzada, acción de filamento realizada y si el cabezal llegó a regresar a la pieza.

[Volver al índice](README.md)
