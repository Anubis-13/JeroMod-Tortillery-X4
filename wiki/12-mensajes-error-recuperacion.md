# 🚨 B12 — Mensajes de error y recuperación

El sistema utiliza pantallas específicas para impedir una acción insegura, explicar por qué no puede continuar o permitir recuperar la comunicación con Klipper. Anotad siempre el texto exacto antes de pulsar un botón.

## Calibraciones pendientes

**Hay calibraciones pendientes** indica que faltan Z-Offset, malla o ambas. **Calibrar** abre el proceso correspondiente. **Más tarde** lo pospone, pero una impresión puede seguir bloqueada hasta completar las calibraciones obligatorias.

No intentéis evitar el aviso modificando archivos o enviando la impresión repetidamente desde Mainsail.

## Error de almacenamiento

**No se pudo leer o iniciar el archivo. Compruebe el USB o almacenamiento interno** puede aparecer si el archivo desaparece, el USB se retira, la ruta ya no existe o el G-code no puede abrirse.

Pulsad **Confirmar**, regresad al explorador y revisad el dispositivo y el archivo. El aviso no debe eliminar el G-code por sí mismo.

## USB no reconocido

**USB no formateado / USB formato no reconocido** indica que el sistema no ha podido montar el dispositivo. La pantalla no formatea el USB. Retiradlo, guardad su contenido desde un ordenador y preparadlo de nuevo con un formato compatible antes de reintentarlo.

No desconectéis otro USB que se esté utilizando para imprimir.

## WiFi

**Conexión fallida** devuelve a la gestión de redes después de confirmar. Revisad contraseña, intensidad de señal y compatibilidad de la red. No publiquéis la contraseña en el Issue.

## Acelerómetro y sonda

- **No se ha detectado acelerómetro:** no existe comunicación con un sensor compatible.
- **Fallo detección acelerómetro:** la consulta comenzó pero no terminó correctamente.
- **Detección fallida:** la sonda o el proceso esperado no respondieron como debía.

No repitáis movimientos o vibraciones si existe riesgo mecánico. Indicad modelo exacto del sensor y conexión utilizada.

## Reportes de Klipper

La pantalla **Reportes de Klipper** muestra el mensaje recibido y ofrece **FIRMWARE RESTART**. Utilizadlo una sola vez después de leer y anotar el error.

Un reinicio correcto pasa por la pantalla de espera y vuelve cuando Moonraker, Klipper, la conexión y la telemetría están disponibles. Si reaparece el mismo error, no encadenéis reinicios ni restauréis de fábrica: abrid un Issue con el texto completo y los logs de Mainsail.

## Reintentar y esperas

Durante la configuración inicial, una actualización, un guardado o un reinicio puede aparecer **Reintentar**. Esperad primero a que el proceso termine o muestre un error estable. No pulséis repetidamente ni cortéis la alimentación.

## Informar de un fallo de B12

```text
[FALLO] FIRMWARE RESTART vuelve al mismo error de Klipper
```

Indicad qué acción abrió el aviso, texto completo, pantalla anterior, botón utilizado, resultado del reinicio y logs disponibles. Si el error pertenece claramente a otro bloque, utilizad el código de ese bloque.

[Volver al índice](README.md)
