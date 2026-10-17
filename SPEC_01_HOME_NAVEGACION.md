# SPEC 01 — HOME / NAVEGACIÓN

## Objetivo
Presentar NOS UNE y permitir al usuario acceder rápidamente a las principales funciones de la plataforma desde una sola landing page.

## Contenido
El Home incluye:
- Logo NOS UNE.
- Menú principal: Inicio, Transmisión, Misas, Reflexiones, Nuestra parroquia y Aportes.
- Hero principal con imagen institucional.
- Mensaje principal: **“Una comunidad que camina contigo.”**
- Botón **Conoce más**.
- Botón destacado **Haz tu aporte**.

## Accesos rápidos
Debajo del hero se muestran cinco accesos:
- Transmisión en vivo
- Misas anteriores
- Reflexiones
- Nuestra parroquia
- Haz tu aporte

Cada tarjeta dirige mediante scroll a su componente correspondiente dentro de la landing.

## Comportamiento
- Navegación por anclas.
- Scroll suave.
- Header fijo.
- Menú responsive tipo hamburguesa en móvil.
- Hover dorado en opciones de navegación.

## Criterio de aceptación
El usuario puede llegar a cualquiera de las funciones principales desde el Home sin abandonar la landing.

## Fidelidad al diseño de referencia (`index(2).html`)
- Conservar este orden en el header: logo; navegación **Inicio, Transmisión, Misas, Reflexiones, Nuestra parroquia, Aportes**; botón destacado **Haz tu aporte**.
- Hero: sobretexto **NOS UNE**, título **Una comunidad / que camina contigo.**, párrafo institucional existente y botón **Conoce más** enlazado a `#parroquia`.
- Después del hero deben aparecer exactamente cinco tarjetas de acceso rápido, en este orden: Transmisión en vivo, Misas anteriores, Reflexiones, Nuestra parroquia, Haz tu aporte. Cada tarjeta conserva icono, título y descripción del HTML y apunta a `#transmision`, `#misas`, `#reflexiones`, `#parroquia`, `#aporte` respectivamente.
- Mantener identificadores de sección y navegación dentro de la misma landing; el menú hamburguesa está presente en el HTML, pero su funcionamiento concreto requiere implementar/verificar la lógica JavaScript.
- En React, reproducir la jerarquía estructural y reutilizar los recursos visuales originales disponibles, evitando rediseños sin aprobación.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
