# ♻️ B11 — Restauración de fábrica

La restauración se abre desde **Ajustes → Ajustes avanzados → Restaurar**. Detiene calentadores y motores, restablece preferencias básicas y prepara nuevamente el recorrido inicial.

> ⚠️ No utilicéis esta función como solución rápida para una incidencia. Anotad primero el fallo y conservad los datos necesarios para reproducirlo.

## Opciones disponibles

- **Borrar redes WiFi:** elimina los perfiles inalámbricos guardados.
- **Borrar contenido G-code:** elimina los archivos internos y vacía la cola de trabajos. No debe borrar el contenido físico del USB.
- **Borrar historial impresora:** elimina trabajos anteriores y totales registrados.
- **Restaurar printer/macros.cfg:** recupera los perfiles base del modelo y vuelve a pedir su selección durante la Bienvenida.
- **Seleccionar todos:** activa todas las opciones anteriores.

Aunque no se marque un borrado opcional, la restauración devuelve a valores iniciales las preferencias de pantalla, perfiles de temperatura, malla y Z-Offset. Las calibraciones volverán a figurar como pendientes.

## Cancelar

**Cancelar** regresa a Ajustes avanzados sin borrar información ni reiniciar el sistema.

## Confirmar

Antes de confirmar:

1. Terminad o cancelad cualquier impresión.
2. Comprobad que boquilla y cama están dejando de calentar.
3. Retirad el USB si no es necesario.
4. Revisad cuidadosamente las casillas seleccionadas.

Al confirmar aparece **Procesando...**. El sistema detiene calentadores, ventilador de capa y motores; restaura los datos seleccionados; reinicia Klipper y abre de nuevo la Bienvenida.

No cortéis la alimentación ni toquéis la pantalla durante el proceso.

## Después de restaurar

- Seleccionad el idioma.
- Si se conservaron los perfiles del modelo, el sistema puede omitir su instalación.
- Si se restauró `printer/macros.cfg`, elegid nuevamente el modelo físico correcto.
- Configurad WiFi si se borraron las redes.
- Completad Z-Offset, tornillos y malla antes de imprimir.

## Informar de un fallo de B11

```text
[FALLO] Cancelar borra las redes WiFi guardadas
```

Indicad las casillas seleccionadas, opción pulsada, última pantalla, datos que se conservaron o borraron y si el reinicio terminó correctamente.

[Volver al índice](README.md)
