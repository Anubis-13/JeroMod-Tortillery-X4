# 🧵 B08 — Sensor de filamento

El sensor puede activarse o desactivarse desde **Ajustes → Ajustes avanzados → Sensor filamento**. Cuando está activo, su icono aparece en la pantalla principal y en la pantalla de impresión.

## Funcionamiento al iniciar

Durante la preparación inicial el sistema protege temporalmente el flujo para evitar avisos falsos mientras realiza Home y purga. Cuando comienza la impresión, vuelve a aplicar la preferencia guardada y comprueba el estado real del sensor.

Si no detecta filamento, pausa el trabajo y abre el aviso correspondiente.

## Falta de filamento durante una impresión

Cuando el sensor pasa de detectar filamento a no detectarlo:

1. Klipper pausa el trabajo.
2. La pantalla espera a que la pausa sea efectiva.
3. Aparece **No se detecta filamento**.
4. Se ofrecen **Continuar** e **Ignorar**.

### Continuar

Utilizad esta opción después de cargar filamento. Si el sensor continúa indicando ausencia, la reanudación queda bloqueada y vuelve a mostrarse el aviso.

### Ignorar

Desactiva temporalmente el sensor y reanuda la impresión. El sistema lo rearma cuando vuelve a detectar filamento. Utilizadlo solo si existe filamento y el problema está en la detección; después deberéis vigilar la impresión personalmente.

## Cargar el nuevo filamento

Con la impresión pausada:

1. Retirad el filamento agotado.
2. Mantened la boquilla a una temperatura adecuada.
3. Cargad el nuevo filamento.
4. Extruid lo necesario hasta obtener un flujo limpio.
5. Retirad el material purgado.
6. Pulsad **Continuar**.

No forcéis el filamento ni reanudéis mientras el cabezal está moviéndose.

## Mainsail

Mainsail debe mostrar el trabajo pausado durante el aviso y volver a `printing` al continuar o ignorar. No enviéis Resume desde Mainsail al mismo tiempo que pulsáis una opción en la pantalla.

## Informar de un fallo de B08

```text
[FALLO] Continuar reanuda aunque el sensor sigue sin filamento
```

Indicad si el sensor estaba activado, estado físico del filamento, texto de la pantalla, opción elegida y estado observado en Mainsail.

[Volver al índice](README.md)
