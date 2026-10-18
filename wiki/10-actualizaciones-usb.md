# 🔄 B10 — Actualizaciones USB

Las correcciones se distribuyen como paquetes `.mksp` firmados. Utilizad únicamente el archivo y el enlace publicados en el repositorio oficial de la beta.

## Preparar el USB

1. Descargad el paquete autorizado.
2. Comprobad nombre, tamaño y SHA-256 publicados.
3. Copiad **un único paquete `.mksp`** en la raíz del USB.
4. No lo renombréis, modifiquéis ni descomprimáis.
5. Expulsad el USB correctamente antes de conectarlo a la impresora.

Los G-code pueden permanecer en el dispositivo, pero no debe haber varios paquetes de actualización en la raíz.

## Detección

Con la impresora preparada, sin imprimir y en la pantalla principal, conectad el USB. El sistema comprueba firma, contenido, versión y modelo antes de permitir la instalación.

La pantalla **Actualización** puede mostrar:

- **Actualización detectada**;
- **Versión anterior: bloqueada**;
- **Versión ya instalada**;
- **Archivo no válido**;
- **Versión actual desconocida**;
- **Modelo incompatible**;
- **Hay varios archivos**.

Los estados bloqueados no modifican el sistema. Utilizad **Cancelar** o **Finalizar** según lo que aparezca y comunicad el texto exacto si no coincide con lo esperado.

## Instalar

Cuando el paquete sea válido:

1. Revisad la información mostrada.
2. Pulsad **Confirmar** una sola vez.
3. No retiréis el USB ni cortéis la alimentación.
4. Esperad durante **Actualización en curso**.
5. La pantalla o el sistema pueden reiniciarse.
6. Esperad **Actualización finalizada** y pulsad **Finalizar**.
7. Consultad **Ajustes avanzados → Info sistema** para revisar las versiones.

El instalador guarda copias y verifica el arranque. Si la nueva aplicación no completa su comprobación de salud, el sistema puede restaurar automáticamente la versión anterior.

## Compatibilidad entre modelos

Un paquete puede estar destinado a X4 Pro, X4 Plus o ambos. Si no corresponde al modelo instalado, debe aparecer **Modelo incompatible** y la instalación debe quedar bloqueada.

No cambiéis temporalmente el modelo para intentar instalar otro paquete.

## Qué no debe hacerse

- No instalar el `.mksp` manualmente desde Linux.
- No copiar archivos internos del paquete a la impresora.
- No usar paquetes recibidos de otras personas.
- No interrumpir una instalación para comprobar la recuperación.
- No intentar rollback salvo que se publique un procedimiento específico.

## Informar de un fallo de B10

```text
[B10][X4 PRO] La actualización queda detenida en Reiniciando
```

Indicad nombre y SHA-256 del paquete, modelo, versiones anteriores, mensaje inicial, última fase alcanzada, si hubo reinicio y versiones mostradas después. No adjuntéis paquetes no autorizados al Issue.

[Volver al índice](README.md)
