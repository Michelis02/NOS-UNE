# SPEC 02 — TRANSMISIÓN EN VIVO

## Objetivo
Permitir que los usuarios acompañen las transmisiones y contenidos audiovisuales del Padre Freddy directamente desde NOS UNE.

## Fuente de contenido
Los videos provienen del canal oficial de YouTube del Padre Freddy. La plataforma se conectará con **YouTube Data API** para consultar automáticamente el contenido publicado en el canal.

## Contenido
El componente incluye:
- Reproductor principal de YouTube.
- Estado de transmisión en vivo cuando corresponda.
- Bloque lateral **Últimas celebraciones**.
- Miniatura, título e información básica de cada contenido.

## Funcionamiento
Al seleccionar uno de los videos laterales:
- cambia el contenido del reproductor principal;
- no se recarga la página;
- el video seleccionado queda visualmente activo.

## Actualización automática
Los últimos videos publicados en YouTube deberán aparecer automáticamente en NOS UNE sin modificar manualmente el HTML. Se obtendrá como mínimo:
- ID del video;
- título;
- miniatura;
- fecha de publicación;
- enlace.

## Criterio de aceptación
Cuando el canal publique contenido nuevo, NOS UNE podrá mostrarlo automáticamente mediante la integración con YouTube.

## Fidelidad al diseño y estados
- Conservar encabezado **Acompáñanos / Transmisión en vivo**, descripción **Vive nuestras celebraciones desde donde estés.** y botón **Ver canal de YouTube**.
- Conservar una composición de reproductor principal a la izquierda y bloque **Últimas celebraciones** a la derecha en escritorio, según las clases `live-layout`, `main-live-video` y `recent-column` del HTML.
- El HTML de referencia presenta **tres elementos laterales** con miniatura, título, texto de apoyo y acción; conservar tres entradas visibles como diseño inicial, con el elemento seleccionado marcado visualmente.
- Mantener la interacción de sustitución del video principal sin recargar la página; preservar los estados de carga, sin resultados y error de la API.
- La etiqueta **EN VIVO** existe en el HTML, pero no debe señalar transmisiones grabadas como directos: mostrarla solo cuando la fuente confirme una emisión en vivo; cuando no haya directo, presentar contenido reciente y un estado informativo.
- El HTML contiene IDs de video fijos; sustituirlos por datos automáticos como funcionalidad nueva, sin modificar el aspecto base de las tarjetas.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
