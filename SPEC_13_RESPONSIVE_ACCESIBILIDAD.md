# SPEC 13 — RESPONSIVE Y ACCESIBILIDAD

## Objetivo
Garantizar que NOS UNE sea fácil de utilizar especialmente para usuarios adultos y adultos mayores.

## Requisitos
La web deberá funcionar correctamente en:
- computador;
- tablet;
- celular.

## Accesibilidad
Se prioriza:
- tipografía legible;
- botones amplios;
- buen contraste;
- navegación simple;
- áreas completas clickeables;
- textos claros;
- no depender únicamente del color;
- imágenes con `alt`;
- navegación mediante teclado donde aplique.

Ninguna funcionalidad principal deberá desaparecer en móvil.

## Criterio de aceptación
El usuario puede realizar las acciones principales desde celular y escritorio sin pérdida de contenido o funcionalidad.

## Fidelidad responsive verificable
- El HTML contiene `meta viewport` y botón de menú móvil, pero **no se adjuntaron `styles.css`, `app.js` ni los archivos de imagen**; por ello no se pueden certificar colores, tamaños, breakpoints, interacciones ni renderización real.
- Conservar el orden del DOM de las secciones y de sus contenidos: header → hero → cinco accesos → transmisión con columna reciente → cuatro misas → cuatro reflexiones → parroquia → aportes → WhatsApp + FAQ → footer.
- En pantallas estrechas, adaptar sin ocultar contenido: accesos rápidos, videos, cuadrículas de cuatro tarjetas, tres bloques de parroquia, dos zonas de donación y dos bloques WhatsApp/FAQ.
- Verificar navegación del menú hamburguesa, tamaño de objetivos táctiles, foco visible, teclado, `alt` significativos, encabezados jerárquicos, contraste y legibilidad para personas mayores.
- Los modales de reflexión, confirmación de pago y resultado de pago deben tener etiqueta accesible, control de foco, Escape y retorno del foco al disparador.
- Definir breakpoints tras inspeccionar `styles.css`; no inventar valores como si provinieran del diseño original. Comparar capturas en escritorio, tablet y móvil con la referencia antes de aprobar la migración.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
