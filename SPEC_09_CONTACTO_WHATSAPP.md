# SPEC 09 — CONTACTO / WHATSAPP

## Objetivo
Ofrecer un canal de comunicación inmediato sin crear un sistema propio de mensajería.

## Interfaz
Mensaje principal:

**¿Necesitas hablar con nosotros?**

Texto:

**Escríbenos directamente por WhatsApp. Estamos aquí para orientarte y acompañarte.**

Botón:

**Abrir WhatsApp**

## Funcionamiento
El botón redirigirá al contacto oficial configurado para el Padre Freddy/parroquia.

Referencia original pendiente de verificación: **@fabuca29**. No utilizar este usuario como URL de WhatsApp; falta número o enlace oficial confirmado.

Si posteriormente se define un número institucional diferente, el enlace será actualizado desde configuración.

## Criterio de aceptación
Al seleccionar el botón, se abre WhatsApp y el visitante puede iniciar la conversación.

## Fidelidad al diseño y contacto efectivo
- WhatsApp comparte `contact-faq-section` con las preguntas frecuentes: mantener la tarjeta `whatsapp-box` a la izquierda/primero en el DOM, sin separarla en otra sección independiente.
- Preservar icono de WhatsApp y estos textos exactos: **¿Necesitas hablar con nosotros?**, **Escríbenos directamente por WhatsApp. Estamos aquí para orientarte y acompañarte.**, botón **Abrir WhatsApp**.
- El HTML identifica un botón `id="whatsappBtn"`, pero su URL efectiva depende de `app.js` (no adjuntado); no afirmar que el vínculo funciona sin revisar ese archivo.
- **@fabuca29 no es por sí solo un enlace válido de WhatsApp.** Sustituir la mención del identificador como destino técnico por un número institucional verificado en formato internacional o un enlace oficial `https://wa.me/...`, cargado desde configuración; nunca inventar el número.
- Abrir una conversación con el contacto autorizado y manejar la ausencia de configuración sin enviar a un contacto incorrecto.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
