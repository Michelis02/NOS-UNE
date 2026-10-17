# SPEC 04 — REFLEXIONES / BLOG

## Objetivo
Crear un espacio editorial para publicar reflexiones escritas por el Padre Freddy.

**Las reflexiones no son videos.** Funcionan como entradas de blog.

## Visualización pública
Cada reflexión mostrará:
- imagen opcional;
- fecha;
- título;
- extracto corto;
- botón **Leer reflexión**.

Al seleccionarla se abrirá el contenido completo mediante el modal de lectura de la landing (`reflectionModal`); una página interna requerirá una especificación adicional.

## Almacenamiento
Las reflexiones se guardarán en una **base de datos**, no directamente dentro del HTML.

Cada registro podrá contener:
- ID;
- título;
- texto;
- imagen;
- fecha;
- autor;
- estado;
- fecha de publicación.

## Administración
Se creará una zona privada en `/admin` desde donde el Padre Freddy o una persona autorizada podrá:
- crear reflexiones;
- agregar imágenes;
- escribir el contenido;
- editar publicaciones;
- eliminar publicaciones;
- publicar o despublicar.

## Flujo
ADMIN → Nueva reflexión → Título + texto + imagen → Publicar → Base de datos → Landing pública.

## Criterio de aceptación
Una reflexión publicada desde el administrador aparece en la sección pública sin editar el código de la página.

## Fidelidad al diseño y navegación editorial
- Conservar la cabecera **Un mensaje para tu día / Reflexiones**, el texto **Palabras del Padre Freddy para acompañarte.** y el botón **Ver todas las reflexiones**.
- La vista inicial contiene **cuatro tarjetas** dentro de `reflections-grid`, cada una con fotografía, fecha, título, extracto y botón **Leer reflexión →**.
- La lectura completa se hará prioritariamente mediante el **modal de reflexión ya previsto en el HTML** (`reflectionModal`), conservando título, fecha, cuerpo del texto, firma **Padre Freddy** y botón de cierre. No crear una página de detalle adicional sin especificación aprobada.
- Definir el destino/función del botón **Ver todas las reflexiones** para listar el archivo completo sin alterar la vista inicial de cuatro tarjetas.
- Las tarjetas hardcodeadas y sus atributos `data-*` son datos de muestra: deben alimentarse desde la base de datos; la gestión `/admin` es una funcionalidad futura, no está implementada por el HTML.
- El modal debe permitir cerrar por botón, Escape y tratamiento accesible del foco.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
