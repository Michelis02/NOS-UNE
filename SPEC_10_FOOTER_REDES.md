# SPEC 10 — FOOTER / REDES SOCIALES

## Objetivo
Cerrar la experiencia de navegación y facilitar el acceso a información institucional y canales externos.

## Contenido
- Logo NOS UNE.
- Parroquia Santa María de los Ángeles.
- El Poblado, Medellín.
- Política de privacidad.
- Términos de uso.
- Ayuda.
- Contacto.

## Redes
Se incluirán botones funcionales para:
- Instagram del Padre Freddy;
- TikTok del Padre Freddy;
- YouTube oficial.

Los enlaces se abrirán en una pestaña nueva.

## Mensaje final
**“Juntos seguimos construyendo una Iglesia más cercana.”**

## Criterio de aceptación
Todos los enlaces sociales abren correctamente el canal correspondiente.

## Fidelidad al diseño de referencia y enlaces pendientes
- Conservar la composición `footer-main`: logo NOS UNE, ubicación institucional, enlaces **Política de privacidad**, **Términos de uso**, **Ayuda**, **Contacto** y grupo de redes sociales.
- Preservar iconos y orden: **Instagram**, **TikTok**, **YouTube**. Mantener por separado `footer-bottom` con la frase **“Juntos seguimos construyendo una Iglesia más cercana.”**
- Los enlaces de políticas y ayuda del HTML usan `href="#"` y son provisionales: crear destinos reales antes de dar el criterio de aceptación por cumplido.
- El TikTok existente apunta a una **búsqueda**, no a una cuenta oficial confirmada; reemplazar solo cuando se valide el perfil correcto.
- El enlace **Contacto** apunta actualmente a `#parroquia`, no a la caja de WhatsApp; definir el destino final explícitamente (por ejemplo, ancla del bloque de contacto) y garantizar que exista.
- Abrir redes externas en nueva pestaña con `rel="noopener noreferrer"`; probar cada enlace antes de la entrega.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
