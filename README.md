
Podéis utilizar esta plantilla:

```text
ID de prueba:
Fecha y hora:
Modelo: X4 Pro / X4 Plus
Tamaño de eMMC:
Expansión seleccionada:
Idioma:
Página desde la que empezasteis:
Página en la que terminó:
Botón que pulsasteis:
Pasos realizados:
Resultado esperado:
Resultado real:
¿Ocurre siempre o solo algunas veces?:
¿Hubo movimiento?: Sí / No
¿Hubo calentamiento?: Sí / No
¿Existió algún riesgo?: Sí / No
Foto o vídeo, si está disponible:
Observaciones:
```

Ejemplo:

```text
ID de prueba: BT-FLOW-003
Página inicial: Movimiento
Botón: Home Y
Esperaba que se moviese el eje Y, pero se movió el eje X.
Apagué la impresora y no repetí la prueba por seguridad.
Resultado: BLOQUEADO POR SEGURIDAD
```

La coordinación de la beta añadirá después el identificador de incidencia, las versiones completas y los logs disponibles. Una incidencia corresponderá siempre a un único problema.

## 🔗 Seguimiento de una corrección

Cuando un fallo reciba una actualización, se conservará toda la relación:

```text
Prueba → Incidencia → Actualización → Repetición
```

Ejemplo:

```text
BT-FLOW-WIFI-002
→ BUG-2026-10-06-001
→ UPD-BETA-02
→ RETEST-UPD-BETA-02
→ OK
```

La lista de repetición incluirá:

- la prueba que fallaba;
- la comprobación de instalación;
- el reinicio posterior;
- las páginas o flujos relacionados;
- el resultado después de actualizar.

No será necesario repetir toda la campaña después de cada actualización. Se indicarán únicamente las pruebas afectadas y las comprobaciones relacionadas.

## ⚠️ Seguridad

Durante cualquier prueba con movimiento o calentamiento, permaneced junto a la impresora y mantened despejada la zona de trabajo.

Detened la prueba si observáis:

- un eje moviéndose en una dirección incorrecta;
- golpes o ruidos mecánicos anormales;
- la boquilla acercándose de forma peligrosa a la cama o a una pieza;
- calentamiento no solicitado;
- una temperatura que aumenta de forma inesperada;
- humo, olor a quemado o cableado caliente;
- cualquier comportamiento que pueda dañar la impresora o resultar peligroso.

> 🛑 No repitáis una situación peligrosa para conseguir una foto o un vídeo. Indicad **BLOQUEADO POR SEGURIDAD** y explicad brevemente lo ocurrido.

No cortéis la alimentación, forcéis una recuperación ni iniciéis una restauración de fábrica salvo que la prueba lo indique expresamente.

## 📷 Fotos, vídeos e información privada

Las fotos y vídeos solo serán necesarios cuando ayuden a entender el problema. Antes de publicarlos, comprobad que no muestren:

- contraseñas Wi-Fi;
- claves SSH;
- tokens o códigos privados;
- direcciones o datos personales;
- información que no esté relacionada con la prueba.

No compartáis fuera del grupo las imágenes, actualizaciones, enlaces ni documentos de esta beta.

## 📌 Reglas generales

- Realizad únicamente las pruebas asignadas.
- Describid lo que hicisteis y lo que ocurrió.
- Utilizad los nombres visibles en la pantalla.
- Comunicad cada problema por separado.
- Preguntad si alguna instrucción no está clara.
- No modifiquéis archivos internos de la impresora.
- No instaléis archivos sueltos ni paquetes no autorizados.
- No probéis el perfil Plus en una X4 Pro.
- No repitáis movimientos o calentamientos peligrosos.
- No compartáis el material de la beta fuera del grupo.

## 🤝 Objetivo

El proceso será sencillo:

```text
Beta-testing detecta y documenta
        ↓
Diagnóstico y corrección en desarrollo
        ↓
Se publica una actualización USB autorizada
        ↓
Beta-testing repite las pruebas afectadas
        ↓
Resultados estables
        ↓
Publicación de la versión final
```

El objetivo es comprobar **JeroMod-Tortillery X4** de forma ordenada, segura y fácil de seguir. Gracias por dedicar vuestro tiempo y vuestra impresora a estas pruebas.
