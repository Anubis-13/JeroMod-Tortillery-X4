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

Durante una impresión activa, Mainsail muestra el botón **Cambio de filamento** en el panel del extrusor. Este botón utiliza internamente `T600`; no es necesario escribir el comando manualmente.

Al pulsarlo:

1. Se inicia el cambio de filamento mediante `M600`.
2. Klipper pausa la impresión y aparta el cabezal.
3. La pantalla abre la página de cambio de filamento cuando la pausa está preparada.
4. Podéis retirar el filamento, cargar el nuevo y comprobar que sale correctamente.
5. Al finalizar, el sistema recupera la temperatura anterior cuando corresponda, vuelve a la pantalla de impresión y reanuda el trabajo.

`T600` solo está disponible mientras el estado sea **Imprimiendo**. Fuera de una impresión activa, el sistema rechazará la orden y mostrará que el cambio no está disponible.

Un cambio solicitado desde el G-code mediante `M600` también utiliza este proceso.

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
