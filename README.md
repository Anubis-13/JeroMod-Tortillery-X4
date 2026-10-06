- pieza desechable que debe utilizarse;
- altura o momento aproximado del corte;
- posición segura del operador;
- comportamiento esperado al encender;
- movimientos que deben observarse;
- condición de parada inmediata;
- datos y vídeo necesarios.

Una prueba PLR correcta debe comprobar tanto la oferta de recuperación como los movimientos físicos y la continuación real de la impresión.

## 15. Restauración de fábrica

Las pruebas `BT-RESET` pueden borrar configuración, redes, historial o archivos. Solo deben realizarse en una campaña expresamente preparada.

Antes de comenzar debe estar indicado:

- qué opciones seleccionar;
- qué información se espera que se borre;
- qué información se espera conservar;
- cómo recuperar la impresora;
- qué imagen o copia de seguridad está disponible.

No realices una restauración para intentar solucionar por tu cuenta una incidencia.

## 16. Reglas específicas para X4 Plus

La X4 Plus comparte interfaz y software principal con la X4 Pro, pero utiliza un perfil físico diferente.

Por ello:

- identifica siempre el modelo como `X4 Plus`;
- no extrapoles un resultado Pro a Plus;
- no pruebes el perfil Plus sobre una Pro;
- detén inmediatamente la prueba si un eje se mueve en dirección incorrecta;
- presta especial atención a límites, centros, homing, malla, tornillos, limpieza y purga;
- no declares una función Plus validada porque la interfaz se comporte correctamente sin movimiento.

La validación Plus requiere comprobar el comportamiento físico en una X4 Plus real.

## 17. Qué no debe hacer un beta tester

- No modificar Python, HMI, TFT, CFG ni macros.
- No instalar archivos sueltos.
- No usar paquetes de procedencia desconocida.
- No cambiar versiones manualmente.
- No intentar corregir el firmware durante una prueba.
- No ejecutar comandos destructivos sin instrucciones.
- No sellar ni preparar imágenes.
- No compartir el contenido del repositorio privado.
- No publicar enlaces de descarga fuera del grupo autorizado.
- No compartir contraseñas, claves, tokens ni información privada.
- No probar el perfil Plus en una X4 Pro.

## 18. Flujo completo de trabajo

```text
Beta-testing detecta y documenta
        ↓
Diagnóstico y corrección en entorno DEV
        ↓
Se crea una actualización .mksp firmada
        ↓
Beta-testing repite las pruebas afectadas
        ↓
Resultados estables
        ↓
WORKING → publicación → sellado → RELEASE
```

Los beta testers participan hasta la validación posterior a la actualización. La preparación DEV, construcción de paquetes, publicación, sellado y RELEASE son responsabilidades separadas.

## 19. Resumen rápido

Antes de probar:

- confirma modelo y versión;
- lee toda la prueba;
- prepara una zona segura;
- no improvises pasos.

Si funciona:

- registra `OK`;
- añade la evidencia solicitada.

Si falla:

- detén la prueba si existe riesgo;
- registra `FALLO` o `BLOQUEADO POR SEGURIDAD`;
- crea una incidencia independiente;
- describe acciones y resultados, no causas técnicas.

Si aparece una actualización:

- comprueba que sea compatible con tu modelo y versión;
- instala únicamente el paquete autorizado;
- repite las pruebas indicadas;
- no marques la incidencia como resuelta hasta completar la repetición.

---

**Este programa de beta-testing no autoriza la distribución pública de JeroMod, sus imágenes, actualizaciones ni documentación privada.**
