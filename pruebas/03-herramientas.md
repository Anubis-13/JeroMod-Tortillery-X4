# 🛠️ Bloque 03 — Herramientas

**ID del bloque:** `BT-FLOW-HERRAMIENTAS-001`  
**Modelos:** Artillery X4 Pro y X4 Plus  
**Inicio:** pantalla principal  
**Final:** movimiento, temperatura y filamento comprobados

## Objetivo

Comprobar las tres pantallas de **Herramientas**, sus controles y la información mostrada.

Desde la pantalla principal, pulsad el **icono de herramientas**. Se abrirá directamente la pantalla de movimiento.

Los tres iconos superiores aparecen en este orden:

1. **Cruz de flechas:** movimiento.
2. **Termómetro:** temperatura.
3. **Boquilla con flechas hacia arriba y abajo:** filamento.
- en la barra de la pantalla principal inferior encontraréis el **icono Principal** para volver al inicio, el **icono de herramientas**, el **icono de opciones** y el **icono de ajustes**.


## ⚠️ Antes de empezar

- Máxima atención para quienes tengan una X4 Plus.
- Dejad libres los ejes y retirad cualquier objeto de la cama.
- Permaneced junto a la impresora durante los movimientos y calentamientos.
- No mováis un eje hacia su límite con pasos grandes.
- No toquéis la boquilla cuando esté caliente.
- Detened la prueba si aparece un golpe, un movimiento incorrecto o un calentamiento descontrolado.

## 1. Movimiento — icono de la cruz de flechas

**ID:** `BT-PAGE-TOOLS-001`

### Home completo obligatorio

Lo primero que debéis hacer al entrar es pulsar **ALL Homing**. Los movimientos manuales no funcionaran antes de completar este paso;

Resultado esperado:

- se abre la pantalla de espera;
- los ejes X, Y y Z hacen Home en la dirección correcta;
- los mensajes mostrados son correctos;
- no hay golpes ni movimientos fuera de recorrido;
- al terminar se regresa a la pantalla de movimiento;
- las posiciones mostradas se actualizan.

> 🛑 Si un eje se mueve en la dirección equivocada, apagad la impresora y comunicad **BLOQUEADO POR SEGURIDAD**. No repitáis el Home.

### Home individual

Después de completar **ALL Homing**:

1. Probad **Home X**.
2. Probad **Home Y**.
3. Probad **Home Z**.
4. Comprobad el eje, la dirección y los mensajes mostrados.

Cada botón debe mover únicamente el eje indicado y regresar a la pantalla de movimiento al terminar.

### Movimiento manual

1. Seleccionad los pasos de **0,1 mm**, **1 mm** y **10 mm**.
2. Con cada paso, probad `+` y `−` en X, Y y Z.
3. Comprobad que el eje, la dirección y la distancia son correctos.
4. Confirmad en Mainsail que las coordenadas coinciden con los movimientos realizados.

Utilizad primero el paso más pequeño y dejad margen suficiente antes de probar **10 mm**.

### Liberar motores y comprobar Mainsail

1. Pulsad el botón con el que se liberan los motores.
2. Comprobad con suavidad que dejan de mantener la posición. No forcéis el eje Z.
3. Abrid Mainsail y realizad primero un Home completo, porque los motores acaban de liberarse.
4. Comprobad que la pantalla muestra la espera y los mensajes del Home y que, al terminar, vuelve al inicio.
5. Desde los controles de Mainsail, probad Home X, Home Y y Home Z.
6. Realizad movimientos pequeños de X, Y y Z y comprobad que la posición también se actualiza en la pantalla.

> En este bloque utilizad solamente los controles normales de Mainsail. **No ejecutéis macros todavía.**

## 2. Temperatura — icono del termómetro

**ID:** `BT-PAGE-TOOLS-002`

Pulsad el icono del termómetro. Deben mostrarse las temperaturas actuales y objetivo de la boquilla y la cama.

### Perfiles de temperatura

Los valores iniciales son:

| Perfil | Boquilla | Cama |
|---|---:|---:|
| PLA | 200 °C | 60 °C |
| ABS | 245 °C | 100 °C |
| PETG | 225 °C | 70 °C |
| TPU | 220 °C | 60 °C |

1. Pulsad el **engranaje** de la barra inferior y, dentro de **Ajustes**, abrid **Perfiles temperatura**.
2. Abrid cada material y comprobad sus valores.
3. Cambiad ligeramente al menos un valor de cada perfil y anotadlo.
4. En uno de los perfiles, probad `+` y `−` con pasos de **1 °C**, **5 °C** y **10 °C**.
5. Salid y volved a entrar para comprobar que los cambios se conservan.
6. Volved a **Herramientas** y pulsad el icono del termómetro.
7. Activad PLA, ABS, PETG y TPU, uno por uno.
8. Comprobad en la pantalla y en Mainsail que cada perfil aplica los valores guardados.
9. Detened la boquilla y la cama después de cada perfil. No esperéis a que alcancen la temperatura.
10. Devolved todos los perfiles a sus valores iniciales al terminar.

### Temperatura manual y límites

1. Pulsad el valor objetivo de la boquilla e introducid una temperatura segura.
2. Repetidlo con la cama.
3. Comprobad en la pantalla y en Mainsail que ambos objetivos coinciden.
4. Introducid **351 °C** para la boquilla y comprobad que aparece en rojo **Valor max nozzle 350C** y que el valor no se aplica.
5. Introducid **121 °C** para la cama y comprobad que aparece en rojo **Valor max cama 120C** y que el valor no se aplica.
6. Pulsad por separado los botones de parada de la boquilla y de la cama.
7. Confirmad que ambos objetivos vuelven a `0` en la pantalla y en Mainsail.

> Los límites son **350 °C para la boquilla** y **120 °C para la cama**. No seleccionéis esos máximos para calentar; esta prueba solo comprueba que un valor superior queda bloqueado.

Resultado esperado:

- las temperaturas actuales se actualizan;
- los perfiles conservan y aplican los cambios;
- los valores manuales seguros se aplican correctamente;
- los avisos rojos muestran el límite correcto;
- los dos botones de parada funcionan por separado;
- la pantalla y Mainsail muestran los mismos objetivos.

## 3. Filamento — icono de la boquilla con flechas

**ID:** `BT-PAGE-TOOLS-003`

Pulsad el icono de la boquilla con flechas hacia arriba y abajo. Deben mostrarse:

- la temperatura de la boquilla;
- la longitud;
- la velocidad;
- **Extruir**;
- **Retraer**.

### Valores y límites

1. Pulsad el valor de longitud e introducid **5**. Al ser menor que el mínimo, no debe guardarse y debe recuperarse el valor anterior.
2. Introducid **351** y comprobad que aparece en rojo **Longitud filamento max 350**.
3. Pulsad el valor de velocidad e introducid **5**. Tampoco debe guardarse.
4. Introducid **361** y comprobad que aparece en rojo **Velocidad filamento max 360**.
5. Dejad una longitud corta válida, por ejemplo **10 mm**, y una velocidad moderada válida.

Los valores admitidos son de **10 a 350** para la longitud y de **10 a 360** para la velocidad. No pulséis **Extruir** ni **Retraer** mientras comprobáis valores que están fuera de esos límites.

### Protección en frío

Con la boquilla fría:

1. Pulsad una vez **Extruir**.
2. Comprobad que aparece el aviso **Boquilla con baja temperatura** y que el extrusor no se mueve.
3. Confirmad el aviso y repetidlo una sola vez con **Retraer**.

La pantalla indica que la boquilla debe estar a **180 °C** para extruir o retraer. No repitáis esta comprobación más veces.

### Extrusión y retracción

1. Calentad la boquilla a una temperatura adecuada para el filamento utilizado y esperad hasta alcanzar al menos **180 °C**.
2. Dejad una longitud corta, por ejemplo **10 mm**, y una velocidad moderada.
3. Pulsad **Extruir** y comprobad que el extrusor gira en el sentido correcto.
4. Pulsad **Retraer** y comprobad que gira en el sentido contrario.
5. Confirmad que cada movimiento termina después de la longitud indicada.
6. Comprobad en Mainsail que no aparece ningún error.
7. Detened el calentamiento de la boquilla al terminar.

> 🛑 Si el extrusor gira en el sentido contrario, no sale filamento cuando debería o el movimiento no se detiene, parad la prueba y comunicadlo.

## Resultado del bloque

Responded al anuncio con:

```text
Bloque: Herramientas
Modelo: X4 Pro / X4 Plus
Movimiento desde la pantalla: OK / FALLO / BLOQUEADO POR SEGURIDAD
Movimiento desde Mainsail: OK / FALLO / BLOQUEADO POR SEGURIDAD
Temperatura: OK / FALLO / BLOQUEADO POR SEGURIDAD
Perfiles guardados y aplicados: OK / FALLO
Límites y avisos: OK / FALLO
Filamento: OK / FALLO / BLOQUEADO POR SEGURIDAD
Resultado general: OK / FALLO / BLOQUEADO POR SEGURIDAD
Observaciones:
```

Si aparece un problema, abrid un Issue independiente e indicad la pantalla, el icono o botón pulsado y lo ocurrido.
