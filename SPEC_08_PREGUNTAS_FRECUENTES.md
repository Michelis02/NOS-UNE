# SPEC 08 — PREGUNTAS FRECUENTES

## Objetivo
Resolver rápidamente las dudas recurrentes de los visitantes.

## Interfaz
Se utilizará un sistema de acordeón.

Preguntas iniciales:
- ¿Cuáles son los horarios de las misas?
- ¿Cómo puedo recibir un sacramento?
- ¿De qué manera puedo hacer un aporte?
- ¿Cómo puedo ser voluntario?
- ¿Dónde queda la parroquia?

## Administración
Las FAQ deberán ser administrables desde `/admin`.

El administrador podrá:
- crear preguntas;
- modificar respuestas;
- eliminar preguntas;
- cambiar su orden;
- activar o desactivar contenido.

## Almacenamiento
Las preguntas y respuestas se almacenarán en la base de datos.

## Criterio de aceptación
La parroquia puede actualizar las FAQ sin modificar código.

## Fidelidad al diseño de referencia
- **FAQ y WhatsApp comparten una sola sección** (`contact-faq-section`) y una composición `contact-faq-grid`; no crear una sección FAQ independiente de ancho completo en escritorio.
- Mantener el bloque FAQ al lado del bloque de WhatsApp y respetar el encabezado **Preguntas frecuentes / Resuelve aquí algunas dudas comunes.**
- Conservar inicialmente estas **cinco preguntas**, en el mismo orden del HTML, con botón de acordeón y símbolo **+**; el contenido de respuestas existente se mantiene mientras no sea editado desde `/admin`.
- En móvil, ambos bloques deben apilarse manteniendo su contenido y accesibilidad; el orden visual debe seguir el DOM de referencia: WhatsApp antes de FAQ.
- El acordeón debe funcionar mediante botones accesibles, con `aria-expanded`, vínculo al panel correspondiente y navegación por teclado.
- La edición desde `/admin` y la base de datos es funcionalidad prevista, no demostrada por el HTML estático.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
