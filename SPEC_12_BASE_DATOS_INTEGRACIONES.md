# SPEC 12 — BASE DE DATOS E INTEGRACIONES

## Objetivo
Centralizar los contenidos administrables y conectar NOS UNE con servicios externos.

## Base de datos
### Reflexiones
Campos principales:
- id
- titulo
- extracto
- contenido
- imagen
- autor
- fecha
- estado

### Preguntas frecuentes
Campos principales:
- id
- pregunta
- respuesta
- orden
- estado

### Usuarios administradores
Campos principales:
- id
- nombre
- correo
- rol
- autenticacion

## Integraciones
### YouTube Data API
Responsable de obtener:
- videos;
- miniaturas;
- títulos;
- fechas;
- IDs.

### Pasarela de pago
Responsable de:
- PSE;
- procesamiento;
- resultado financiero;
- referencia de transacción.

### WhatsApp
Responsable de la comunicación directa con la parroquia.

## Criterio de aceptación
Cada servicio externo tiene una responsabilidad clara y NOS UNE no duplica funcionalidades innecesarias.

## Alineación técnica con React y Firebase
- Este SPEC describe infraestructura y **no tiene equivalencia visual directa** en el HTML; no se debe modificar el diseño público para satisfacer decisiones de base de datos.
- **Firebase Hosting** aloja la aplicación React compilada y necesita regla de reescritura SPA para rutas como `/admin`. Hosting por sí solo no ofrece base de datos ni autenticación.
- Propuesta a confirmar en planificación: **Cloud Firestore** para reflexiones y FAQ, **Firebase Authentication** para usuarios administradores y, si se requieren imágenes nuevas, **Cloud Storage** con permisos restringidos.
- Aplicar reglas de seguridad server-side y control por roles; no confiar en el estado de React para controlar acceso a documentos.
- YouTube Data API debe alimentarse desde una integración que gestione límites, errores y, cuando corresponda, credenciales fuera del frontend; no exponer secretos de servicios.
- La creación y verificación de pagos debe ejecutarse en un entorno seguro de servidor o servicios confiables del proveedor; nunca marcar pagos como aprobados solo desde el navegador.
- Distinguir datos estáticos de referencia en el HTML frente a datos dinámicos requeridos por los SPECS; documentar migración y valores por defecto.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
