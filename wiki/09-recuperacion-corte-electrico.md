# 🔌 B09 — Recuperación tras corte eléctrico

La recuperación tras pérdida de alimentación —PLR— puede activarse desde **Ajustes → Ajustes avanzados → Corte energía**. Su icono aparece en la pantalla principal y durante la impresión cuando está habilitada.

## Qué guarda el sistema

Durante una impresión compatible se crean puntos de recuperación. Si la alimentación se interrumpe, el siguiente arranque puede detectar el trabajo incompleto y mostrar:

**La impresión se interrumpió por un apagón. ¿Continuar desde el último punto guardado?**

## Confirmar la recuperación

Al pulsar **Confirmar**, la pantalla muestra las fases:

1. Cargando datos guardados.
2. Restaurando impresión.
3. Reanudando impresión.
4. Recuperación completada.

El sistema restaura el archivo y el estado disponible desde el último punto guardado. Permaneced junto a la impresora: la pieza puede haberse enfriado o despegado y la posición recuperada puede no ser segura.

## Cancelar la recuperación

**Cancelar** descarta la reanudación y elimina el estado y los puntos guardados. Después se vuelve a la pantalla principal. Una recuperación descartada no debe volver a ofrecerse en cada arranque.

## Limitaciones

- Debe estar activado **Corte energía** antes del apagón.
- El archivo original debe continuar disponible.
- Se recupera desde el último punto guardado, no necesariamente desde la última línea ejecutada.
- La adhesión de la pieza y el estado mecánico no pueden restaurarse por software.
- Un apagado normal desde **Opciones de energía** no equivale a un corte durante la impresión.

> 🛑 No cortéis la alimentación deliberadamente salvo que se haya publicado una comprobación específica. Esta guía explica el funcionamiento y la actuación ante una interrupción real.

## Informar de un fallo de B09

```text
[FALLO] Cancelar no elimina la recuperación guardada
```

Indicad si PLR estaba activo, origen del archivo, fase aproximada de la impresión, pantalla del siguiente arranque, opción elegida y última fase mostrada.

[Volver al índice](README.md)
