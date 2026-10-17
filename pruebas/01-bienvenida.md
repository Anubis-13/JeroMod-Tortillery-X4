# 👋 Bloque 01 — Bienvenida y primer arranque

**ID:** `BT-FLOW-BIENVENIDA-001`  
**Modelos:** Artillery X4 Pro y X4 Plus  
**Inicio:** primer encendido después de grabar la imagen beta  
**Final:** llegada a la pantalla principal

## Objetivo

Comprobar el recorrido completo del primer arranque: idioma, eMMC, modelo, instalación del perfil, WiFi y calibraciones iniciales.

Llegar a la pantalla principal confirma que la Bienvenida ha terminado. **En este bloque no se prueban sus botones.**

## Antes de empezar

- Confirmad que habéis grabado la imagen indicada en el README.
- Anotad el modelo real de la impresora y el tamaño de la eMMC.
- Retirad el adaptador utilizado para grabar la eMMC y montadla correctamente.
- Dejad libre el movimiento de los ejes y retirad cualquier pieza de la cama.
- Permaneced junto a la impresora durante todo el proceso.
- No seleccionéis **X4 Plus** en una X4 Pro ni **X4 Pro** en una X4 Plus.

> 🔵 Durante esta prueba no utilicéis el botón azul **Omitir/Skip** de la esquina superior derecha ni la opción **Más tarde**. La única excepción es la conexión WiFi: podéis omitirla si no queréis conectar la impresora en ese momento.

> ⚠️ Si aparece un movimiento incorrecto, un golpe, calentamiento inesperado o cualquier riesgo, apagad la impresora y comunicad **BLOQUEADO POR SEGURIDAD**. No repitáis el movimiento para grabarlo.

## 1. Idioma

La primera pantalla debe ser **Idiomas**.

1. Comprobad que aparecen las banderas de los idiomas disponibles.
2. Seleccionad el idioma que prefiráis; el chino va muy bien para estos casos, jajaja.
3. Comprobad que el título y los textos cambian al idioma seleccionado. Si podéis probarlos todos antes de continuar, mejor.
4. Pulsad **Siguiente** en vuestro idioma.

Resultado esperado:

- la pantalla responde al primer toque;
- los textos aparecen correctamente;
- el proceso continúa sin volver al inicio.

## 2. Expansión de la eMMC

Esta pantalla solo debe aparecer si la eMMC tiene más de 8 GB y existe espacio disponible para ampliar.

El título visible será **Extender partición EMMC**. Si tenéis varias eMMC y alguna es de 32 GB, podéis aprovechar para probar esta opción. Yo la he probado con eMMC de 8 y 32 GB y funciona correctamente.

### Si aparece

1. Comprobad que muestra el aviso sobre el uso de todo el espacio.
2. Anotad el tamaño de vuestra eMMC.
3. Elegid la opción indicada para vuestra prueba.
4. Pulsad **Siguiente**.

> ⚠️ La ampliación no es reversible. No cambiéis la opción asignada por iniciativa propia.

### Si no aparece

Continuad con la selección de modelo e indicad esta parte como **NO APLICA**.

Resultado esperado:

- una eMMC de 8 GB continúa directamente al modelo;
- la pantalla solo aparece con una eMMC ampliable;
- **Atrás** regresa a Idiomas;
- **Siguiente** continúa hacia la selección de modelo.

## 3. Selección del modelo

La pantalla visible será **Selecciona modelo**.

1. Comprobad que aparecen **X4 Pro** y **X4 Plus**.
2. Seleccionad exclusivamente vuestro modelo real. No seleccionéis el modelo equivocado, que la liamos. **Especial atención a quienes tengáis una X4 Plus:** yo no dispongo de una Plus y su configuración está basada en la de Tortillery, por lo que esta parte necesita especialmente vuestra validación.
3. Confirmad la selección cuando aparezca el aviso.

Resultado esperado:

- se abre **Configuración inicial**;
- aparece **Preparando...** y avanza el proceso;
- se instala el perfil correspondiente al modelo elegido;
- la pantalla puede reiniciarse o perder la conexión momentáneamente;
- el proceso continúa por sí solo.

> 🛑 No cortéis la alimentación durante **Configuración inicial**. Si aparece **Reintentar**, anotad el mensaje mostrado antes de pulsarlo.

## 4. Conexión WiFi

La pantalla visible será **Lista Wifi**.

1. Esperad a que termine la búsqueda.
2. Comprobad que aparecen las redes disponibles.
3. Seleccionad vuestra red.
4. Introducid la contraseña y confirmad.
5. Esperad en **Comprobando Password...**.
6. Cuando aparezca **Conexión exitosa**, pulsad **Confirmar**.

Si no queréis conectar la impresora en este momento, podéis utilizar aquí el botón azul **Omitir/Skip**. Esta es la única pantalla de la prueba en la que se permite omitir un paso.

Resultado esperado:

- la red se conecta correctamente;
- aparece una dirección IP;
- el proceso continúa hacia las calibraciones pendientes;
- si se omite el WiFi, el proceso continúa sin exigir una conexión.


## 5. Calibraciones pendientes

Debe aparecer un aviso con el texto **Hay calibraciones pendientes** y las opciones:

- **Calibrar**.
- **Más tarde**.

### Recorrido normal

Pulsad **Calibrar** y continuad con los apartados siguientes.

> 🚫 En esta prueba no pulséis **Más tarde**. Deben completarse todas las calibraciones de la Bienvenida.

## 6. Calibrar sonda y Z-Offset

La pantalla visible será **Calibrar sonda**.

Controles disponibles:

- Ajustes de aproximación del Z-Offset.
- **Calibrar Z-Offset en caliente**.
- **INICIAR**.
- **GUARDAR**.

Seguid el procedimiento indicado en la pantalla. Esta calibración es la base del resto del proceso, por lo que debe completarse antes de continuar.

1. Colocad una hoja de papel bajo la boquilla.
2. Elegid si la calibración se realizará en frío o en caliente, según la variante asignada.
3. Pulsad **INICIAR**.
4. Ajustad la altura hasta obtener un roce ligero y uniforme con el papel.
5. Pulsad **GUARDAR**.
6. Esperad mientras Klipper guarda la configuración y se reinicia.

Resultado esperado:

- los controles responden;
- la boquilla se mueve en la dirección esperada;
- **GUARDAR** inicia una espera y un reinicio controlado;
- la pantalla continúa automáticamente con la siguiente calibración;
- no aparece un error permanente de Klipper.

> ⚠️ Vigilad la distancia entre la boquilla y la cama. Detened la prueba si la boquilla intenta presionar la cama.

## 7. Calibración de nivel

La pantalla visible será **Calibración nivel**.

Controles disponibles:

- posiciones manuales numeradas de **0 a 8**;
- botón azul **CÁLCULO TORNILLOS**;
- **DETENER TEMPERATURA** cuando corresponda.

1. Comprobad que la impresora se desplaza al punto elegido. Probad todos los puntos.
2. Como mínimo, colocad una hoja de papel bajo la boquilla en el punto 1.
3. Pulsad **CÁLCULO TORNILLOS**.
4. En la X4 Plus deben aparecer 6 tornillos y en la X4 Pro, 4.
5. Seguid las indicaciones mostradas para ajustar los tornillos de la cama.
6. Repetid el cálculo, si queréis, hasta conseguir que no aparezcan flechas en las ruedas de la pantalla. Finalizad el proceso y continuad hacia la malla.

Resultado esperado:

- cada número lleva al punto correspondiente;
- ningún movimiento termina fuera de la cama;
- el cálculo automático completa el homing y las mediciones;
- la pantalla muestra los ajustes necesarios;
- al terminar se abre **Malla de cama**.

## 8. Malla de cama

La pantalla visible será **Malla de cama**.

Debe mostrar:

- límites mínimo y máximo de la malla;
- cantidad de puntos;
- velocidad;
- **Iniciar**;
- **Guardar**.

Podéis utilizar la cantidad de puntos que queráis, aunque para esta prueba es preferible seleccionar la más alta.

1. Comprobad que los límites corresponden al modelo seleccionado.
2. Comprobad que aparecen la cantidad de puntos y la velocidad.
3. Pulsad **Iniciar**.
4. Permaneced junto a la impresora durante todas las mediciones.
5. Cuando termine correctamente, pulsad **Guardar**.
6. Esperad el reinicio controlado.

Resultado esperado:

- la sonda mide todos los puntos previstos;
- no se intenta medir fuera de la cama;
- la malla termina sin errores;
- **Guardar** conserva la configuración;
- después del reinicio se llega a la pantalla principal.
- en la barra de la pantalla principal inferior encontraréis el **icono Principal** para volver al inicio, el **icono de herramientas**, el **icono de opciones** y el **icono de ajustes**.
## 9. Comprobación en Mainsail

Cuando la impresora tenga conexión WiFi:

1. Abrid Mainsail desde otro dispositivo.
2. Utilizad la dirección IP mostrada por la pantalla.
3. Confirmad que la impresora aparece conectada y preparada.
4. Comprobad que no queda ningún aviso permanente de reinicio o configuración pendiente.

No realicéis desde Mainsail las calibraciones de esta Bienvenida.

Si habéis omitido la conexión WiFi, indicad **Mainsail: NO PROBADO**.

## Resultado del bloque

Responded al anuncio del bloque con:

```text
Bloque: Bienvenida y primer arranque
Modelo: X4 Pro / X4 Plus
Tamaño de eMMC:
Expansión: realizada / conservada / no aplica
WiFi: conectado / omitido
Calibraciones: completadas / fallo
Mainsail: OK / FALLO / NO PROBADO
Resultado: OK / FALLO / BLOQUEADO POR SEGURIDAD
Observaciones:
```

Si aparece un fallo, abrid un Issue independiente e indicad la pantalla, el botón pulsado y lo ocurrido.
