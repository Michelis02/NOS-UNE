# SPEC 05 — NUESTRA PARROQUIA

## Objetivo
Presentar información básica de la Parroquia Santa María de los Ángeles de forma clara y accesible.

## Contenido
El componente incluye:
- fotografía de la parroquia;
- nombre oficial;
- descripción;
- misión;
- ubicación;
- horarios de misa;
- servicios parroquiales.

## Información presentada
**Ubicación:** El Poblado, Medellín.

**Horarios de misa:** administrables según la información oficial de la parroquia.

**Servicios:** sacramentos, atención espiritual, formación y acciones pastorales.

## Criterio de aceptación
El visitante comprende quiénes son, dónde están y cuáles son los principales servicios sin navegar a otra página.

## Fidelidad al diseño de referencia
- Reproducir el encabezado **Comunidad / Nuestra parroquia** y el párrafo de presentación existente.
- Conservar la estructura identificada por `parish-layout` con tres áreas: **imagen de la parroquia**, **texto institucional y Nuestra misión**, y **bloque de información**.
- El bloque informativo contiene exactamente tres tarjetas iniciales, con iconos: **Ubicación**, **Horarios de misa** y **Nuestros servicios**. Mantener su jerarquía y textos del HTML hasta contar con información oficial verificada.
- El HTML solo presenta la indicación **Consulta nuestros horarios parroquiales.**; no inventar horarios específicos. La edición de horarios desde `/admin` es una ampliación posterior.
- Mantener la fotografía y los textos aprobados sin introducir información institucional no confirmada.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
