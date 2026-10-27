# SPEC 03 — MISAS ANTERIORES

## Objetivo
Permitir consultar las celebraciones anteriores de la parroquia.

## Contenido
Se mostrarán las misas más recientes mediante tarjetas con:
- miniatura;
- título;
- fecha;
- Padre Freddy;
- acción **Ver celebración**.

## Fuente
Los contenidos se obtendrán automáticamente desde YouTube. No se almacenarán archivos de video directamente dentro de NOS UNE.

## Interacción
Al seleccionar una misa se abrirá el video correspondiente para su reproducción mediante YouTube.

El botón **Ver todas las misas** dirige al canal oficial de YouTube.

## Criterio de aceptación
Los usuarios pueden consultar las celebraciones recientes sin que un administrador deba actualizar manualmente cada tarjeta.

## Fidelidad al diseño de referencia
- La sección conserva sobretexto **Celebraciones**, título **Misas anteriores**, descripción y enlace superior **Ver todas las misas** al canal oficial de YouTube.
- Renderizar inicialmente una cuadrícula de **cuatro tarjetas** como en `masses-grid` del HTML. Cada tarjeta muestra miniatura con icono de reproducción superpuesto, título, atribución al Padre Freddy y acción **Ver celebración**.
- El SPEC exige fecha; esta no aparece en las tarjetas del HTML de referencia. Incorporarla como metadato discreto sin desplazar ni sustituir los elementos visuales existentes, sujeto a aprobación si altera la altura de la tarjeta.
- Definir explícitamente que la interacción reproduce/abre el video seleccionado de YouTube; en la migración React comprobar el comportamiento original del `app.js`, que no se adjuntó.
- Los cuatro ejemplos actuales son datos de demostración; la actualización automática desde YouTube es un desarrollo pendiente.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
