# 📐 B04 — Menú de nivel

Desde la pantalla principal, pulsad el **icono de los dos controles deslizantes**. El menú reúne:

1. Calib. Sonda-Z Offset.
2. Ajustar Tornillos Cama.
3. Autonivel-Malla Cama.
4. Calibrar PID.
5. Medición resonancias.

Estas funciones pueden mover todos los ejes, calentar y reiniciar Klipper. Retirad piezas y objetos de la cama y permaneced junto a la impresora.

## Calib. Sonda-Z Offset

Coloca la boquilla en la zona de calibración y permite ajustar su distancia respecto a la cama. Puede trabajar en frío o con **Calibrar Z-Offset en caliente**, que utiliza aproximadamente 150 °C en la boquilla y 60 °C en la cama.

- **INICIAR:** realiza Home y comienza el ajuste.
- Pasos de **0,01**, **0,05** y **0,1 mm:** suben o bajan el Z-Offset.
- **ABORTAR:** detiene el proceso sin guardar.
- **GUARDAR:** conserva el valor y realiza el reinicio controlado necesario.

Utilizad una hoja de papel y buscad un roce ligero. Si la boquilla presiona la cama, abortad inmediatamente.

## Ajustar Tornillos Cama

La pantalla **Calibración nivel** ofrece posiciones manuales numeradas del 0 al 8. Al pulsar una posición, la boquilla se desplaza a esa zona para ajustar la cama con una hoja de papel.

**CÁLCULO TORNILLOS** realiza Home, calienta, mide los puntos y abre **Ruedas cama**:

- X4 Pro: cuatro tornillos.
- X4 Plus: seis tornillos.

Cada rueda indica sentido y cantidad aproximada de giro. **Recalcular** repite la medición. **DETENER TEMPERATURA** devuelve a cero los objetivos de boquilla y cama.

## Autonivel-Malla Cama

Configura la cantidad de puntos y la velocidad de medición.

- Puntos disponibles: de **3×3** a **6×6**.
- Velocidad: de **90** a **200**.
- Límites X4 Pro: **20,20** a **220,220**.
- Límites X4 Plus: **20,20** a **290,290**.

**Guardar** conserva la configuración elegida. **Iniciar** realiza Home, calienta, mide la malla completa, guarda el perfil `default` y reinicia Klipper. La malla resultante puede consultarse en Mainsail.

## Calibrar PID

Calibra el control térmico de la boquilla o de la cama. Valores habituales:

- boquilla: **200 °C**;
- cama: **60 °C**.

Durante el proceso la temperatura oscilará varias veces alrededor del objetivo. Al terminar se guardan los valores `kp`, `ki` y `kd` y se reinicia Klipper. No iniciéis ambos PID a la vez.

## Medición resonancias

Requiere un acelerómetro compatible. Permite medir por separado el eje X y el eje Y. La impresora realizará Home y un barrido de vibraciones antes de guardar el resultado y reiniciar.

Si no se detecta el acelerómetro, aparece **No se ha detectado acelerómetro** y no comienza el barrido.

> ⚠️ Retirad objetos sueltos y no apoyéis las manos sobre la impresora durante la medición. La compatibilidad física confirmada actualmente corresponde al sensor SPI de Artillery; otros sensores deben indicarse al informar.

## Informar de un fallo de B04

```text
[B04][X4 PRO] Guardar Z-Offset no completa el reinicio
```

Indicad calibración, valores elegidos, punto o eje, último mensaje visible, estado de Mainsail y cualquier movimiento o temperatura peligrosa.

[Volver al índice](README.md)
