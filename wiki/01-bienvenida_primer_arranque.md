# 👋 B01 — Bienvenida y primer arranque

La Bienvenida prepara el sistema después de instalar la imagen o completar una restauración de fábrica. Su recorrido reúne la configuración que debe realizarse antes de usar la impresora.

> No utilicéis **Omitir/Skip** ni **Más tarde** durante la configuración inicial. La única excepción es la conexión WiFi, que puede omitirse si todavía no queréis conectar la impresora.

## 1. Idioma

La pantalla **Idiomas** permite seleccionar chino, inglés, español, francés, italiano, ruso, alemán o japonés. El idioma puede cambiarse posteriormente desde **Ajustes**.

## 2. Extender partición EMMC

Esta pantalla solo aparece si la eMMC dispone de espacio adicional. Una unidad de 8 GB normalmente continúa directamente a la selección de modelo. En unidades mayores puede ampliarse la partición para utilizar toda su capacidad.

La ampliación no es reversible desde esta pantalla. Elegidla únicamente cuando queráis dedicar todo el espacio disponible al sistema.

## 3. Selecciona modelo

Elegid el modelo físico instalado:

- **X4 Pro**;
- **X4 Plus**.

Después de confirmar, **Configuración inicial** instala el perfil correspondiente. La pantalla o Klipper pueden reiniciarse durante el proceso. No cortéis la alimentación.

> 🛑 Un perfil equivocado puede utilizar dimensiones, movimientos y configuraciones que no corresponden a la impresora real.

## 4. Lista Wifi

La pantalla busca las redes disponibles. Al seleccionar una red se abre el teclado para introducir la contraseña. Después de **Comprobando Password...**, una conexión correcta muestra la dirección IP.

Aquí sí puede utilizarse **Omitir/Skip**. El WiFi podrá configurarse más tarde desde **Ajustes Wifi**.

## 5. Calibraciones pendientes

La opción **Calibrar** inicia el recorrido inicial de Z-Offset, tornillos y malla. **Más tarde** permite posponerlo, pero la impresión quedará bloqueada mientras falten calibraciones obligatorias.

Durante estas calibraciones permaneced junto a la impresora y vigilad especialmente la distancia entre la boquilla y la cama.

## Final de la Bienvenida

Al terminar se abre la pantalla principal. Si existe WiFi, la dirección mostrada puede utilizarse para acceder a Mainsail desde otro dispositivo de la misma red.

## Informar de un fallo de B01

```text
[B01][X4 PLUS] Configuración inicial queda en Preparando
```

Indicad tamaño de eMMC, ampliación elegida, modelo seleccionado, última pantalla alcanzada, texto exacto y si el sistema se reinició.

[Volver al índice](README.md)
