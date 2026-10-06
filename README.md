BT-PLR-RECOVERY-001
```

Cuando informes de un problema, copia siempre el ID completo de la prueba.

## 6. Estados permitidos

Selecciona solamente uno:

| Estado | Cuándo utilizarlo |
|---|---|
| `OK` | La prueba se completó exactamente como estaba descrita |
| `FALLO` | El resultado fue distinto del esperado |
| `NO PROBADO` | La prueba todavía no se ha realizado |
| `NO APLICA` | La prueba no corresponde a ese modelo o configuración |
| `BLOQUEADO POR SEGURIDAD` | Continuar podría causar daño o riesgo |
| `PENDIENTE DE ACTUALIZACIÓN` | Existe una corrección prevista, pero todavía no está instalada |
| `CORREGIDO, PENDIENTE DE REPETIR` | La corrección está instalada, pero falta repetir la prueba |
| `VALIDADO DESPUÉS DE ACTUALIZAR` | La prueba se repitió correctamente tras una actualización |

No marques una prueba como `OK` si solo funcionó parcialmente o si fue necesario usar una solución alternativa. En ese caso, registra `FALLO` y explica lo ocurrido.

## 7. Cómo realizar una prueba

Cada prueba indicará:

- ID estable;
- modelo permitido;
- nivel de riesgo;
- condiciones previas;
- pantalla inicial;
- acción exacta;
- resultado esperado;
- evidencias necesarias;
- condición de parada;
- pruebas relacionadas.

Procedimiento general:

1. Confirma que el modelo y las versiones son los solicitados.
2. Lee las condiciones previas y el riesgo.
3. Sitúa la impresora en la pantalla inicial indicada.
4. Sigue únicamente los pasos publicados.
5. No pruebes botones o combinaciones adicionales por iniciativa propia.
6. Observa la pantalla y el comportamiento físico.
7. Registra el resultado.
8. Si hay un fallo, crea una incidencia separada.

## 8. Cómo informar de una incidencia

Reglas principales:

- Una incidencia por problema.
- No agrupes fallos diferentes en el mismo informe.
- Usa el título visible de la pantalla.
- Indica siempre desde qué pantalla llegaste.
- Indica exactamente qué botón pulsaste.
- Escribe los pasos en el orden real.
- Diferencia el resultado esperado del resultado observado.
- Indica si sucede siempre o solo algunas veces.
- No repitas una acción peligrosa para conseguir un vídeo.

Formato del título:

```text
[ID DE PRUEBA] [MODELO] Resumen breve
```

Ejemplo:

```text
[BT-PAGE-PREMOVE-001] [X4 PRO] Home Y mueve el eje equivocado
```

La incidencia recibirá después un identificador como:

```text
BUG-2026-10-06-001
```

### Información solicitada

- ID de prueba.
- Fecha y hora.
- Modelo.
- Tamaño de eMMC.
- Elección de expansión.
- Idioma.
- Versión de imagen.
- Versión SYS.
- Versión TFT.
- Versiones de Klipper y Moonraker, si están disponibles.
- Página inicial.
- Página final.
- Pasos exactos.
- Resultado esperado.
- Resultado real.
- Frecuencia.
- Gravedad.
- Si hubo movimiento.
- Si hubo calentamiento.
- Si existió riesgo.
- Foto o vídeo.
- Logs disponibles.
- Observaciones.

## 9. Gravedad de una incidencia

| Gravedad | Significado |
|---|---|
| Baja | Problema visual o de texto que no impide utilizar la función |
| Media | La función falla, pero existe una alternativa segura |
| Alta | Bloquea una función importante, una calibración o una impresión |
| Crítica | Puede provocar movimiento peligroso, calentamiento incorrecto, pérdida grave de datos o daño físico |

Si dudas entre dos niveles y existe movimiento, temperatura o riesgo, selecciona el nivel más alto y detén la prueba.

## 10. Fotos, vídeos y logs

Una evidencia útil debe mostrar:

- la pantalla completa;
- el botón pulsado, si es posible;
- el movimiento relevante de la impresora;
- el mensaje visible;
- el momento en que aparece el problema.

Antes de adjuntar archivos, revisa que no contengan:

- contraseñas Wi-Fi;
- claves SSH;
- tokens o credenciales;
- direcciones o datos personales;
- nombres privados de redes;
- información que no esté relacionada con la prueba.

No publiques archivos completos de configuración salvo que un responsable los solicite mediante un procedimiento autorizado.

## 11. Actualizaciones beta

Las actualizaciones se entregarán mediante una publicación autorizada identificada como:

```text
UPD-BETA-NN
```

Cada actualización debe indicar:

- versión de origen requerida;
- versión de destino;
- modelos compatibles;
- componentes incluidos;
- incidencias corregidas;
- pruebas que deben repetirse;
- hash SHA-256;
- instrucciones visibles;
- condiciones de recuperación o rollback.

### Reglas obligatorias

- Instala únicamente paquetes beta publicados en este repositorio privado.
- No instales archivos sueltos enviados por mensajes.
- No ejecutes scripts recibidos mediante USB.
- No renombres ni modifiques el paquete.
- No combines archivos de actualizaciones diferentes.
- No instales una actualización destinada a otro modelo.
- No retires la alimentación durante la actualización salvo que la prueba lo ordene expresamente.

Una actualización no convierte automáticamente una incidencia en resuelta. La prueba original debe repetirse.

Trazabilidad esperada:

```text
BT-FLOW-WIFI-002
→ BUG-2026-10-06-001
→ UPD-BETA-02
→ RETEST-UPD-BETA-02
→ VALIDADO DESPUÉS DE ACTUALIZAR
```

## 12. Pruebas posteriores a una actualización

Después de instalar una actualización se comprobará, como mínimo:

1. Que la instalación informa de éxito.
2. Que la impresora reinicia correctamente.
3. Que la versión visible es la esperada.
4. Que la prueba que fallaba ahora funciona.
5. Que las páginas y funciones relacionadas no han sufrido regresiones.
6. Que no aparecen nuevos errores de movimiento, temperatura, red o almacenamiento.

El resultado debe conservar la relación entre la prueba, la incidencia, la actualización y la repetición.
