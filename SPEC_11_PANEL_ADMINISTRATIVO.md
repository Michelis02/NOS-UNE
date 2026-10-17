# SPEC 11 — PANEL ADMINISTRATIVO

## Objetivo
Permitir que personas autorizadas administren los contenidos variables de NOS UNE sin entrar al código.

## Acceso
Ruta privada: `/admin`.

Protegida mediante autenticación.

## Usuarios
Inicialmente:
- Padre Freddy;
- administrador autorizado de comunicaciones.

## Módulos
### Reflexiones
Permite crear, editar, publicar, despublicar y eliminar.

### Preguntas frecuentes
Permite crear, editar, ordenar, eliminar y activar/desactivar.

### Información parroquial
Podrá permitir actualizar:
- horarios;
- información de contacto;
- servicios.

## YouTube
Los videos **no se cargarán manualmente desde el administrador**. Serán obtenidos automáticamente desde YouTube.

## Donaciones
El panel no procesará pagos. La gestión financiera corresponderá a la pasarela y a la entidad receptora.

## Criterio de aceptación
Una persona autorizada puede gestionar el contenido editorial de NOS UNE sin conocimientos de HTML, CSS o JavaScript.

## Alcance visual y arquitectura React
- `index(2).html` representa **solo la landing pública**; no existe en él un panel `/admin`. Por tanto, no puede afirmarse concordancia visual para este SPEC.
- Implementar `/admin` como interfaz independiente y protegida; puede reutilizar logo, colores, tipografía y componentes de marca, pero **no** debe alterar el diseño público aprobado.
- Habilitar módulos para reflexiones y FAQ y, cuando se especifique, horarios y datos parroquiales. No permitir publicación de contenido sin autorización.
- En React, establecer rutas públicas y privadas con protección efectiva en backend/reglas de seguridad, no solo ocultación de botones en la UI.
- Registrar los estados de carga, vacío, error, guardado y publicación; definir permisos mínimos para cada rol.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
