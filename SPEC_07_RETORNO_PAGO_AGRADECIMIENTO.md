# SPEC 07 — RETORNO DE PAGO / AGRADECIMIENTO

## Objetivo
Informar al usuario sobre el resultado de su aporte cuando regrese desde la pasarela.

## Funcionamiento
Después de seleccionar **Volver al comercio**, el usuario regresará a NOS UNE. La plataforma verificará el estado real de la transacción.

Si el pago fue aprobado y el servidor confirmó su estado, aparecerá un modal de agradecimiento independiente del modal previo al pago.

## Contenido del modal
**Gracias por tu aporte**

Se mostrará:
- valor;
- referencia;
- fecha;
- estado.

## Acciones
### Descargar comprobante
Generará un comprobante del aporte con:
- referencia;
- fecha;
- monto;
- estado;
- entidad receptora.

### Solicitar certificado tributario
Permitirá solicitar el documento correspondiente cuando aplique.

La solicitud podrá requerir:
- nombre completo;
- identificación;
- correo;
- referencia del aporte.

## Importante
El certificado tributario **no será generado automáticamente por la página**. La parroquia deberá definir:
- entidad que lo expide;
- formato;
- información requerida;
- responsable administrativo;
- condiciones legales.

## Criterio de aceptación
El usuario recibe confirmación clara de su aporte y puede acceder al comprobante o iniciar la solicitud del certificado.

## Alineación con el HTML y nuevos componentes necesarios
- **Estado real del HTML:** solo existe el modal **Continuar al pago** (`paymentModal`) antes de la transacción, con monto seleccionado y botón **Ir a la pasarela**. **No existe todavía** un modal de pago exitoso.
- Mantener intacto el modal previo del SPEC 06 y crear un **segundo modal independiente** para la respuesta posterior de la pasarela, sin sustituir el anterior.
- Mostrar **Gracias por tu aporte** únicamente después de verificar un pago **aprobado** con el proveedor, nunca solo por un parámetro URL o por una acción del frontend.
- Para los estados **pendiente**, **rechazado** o **cancelado**, presentar mensajes diferenciados; no mostrar una confirmación de éxito ni ofrecer comprobante de pago aprobado cuando no proceda.
- El modal de resultado aprobado debe contener monto, referencia, fecha y estado; acciones separadas **Descargar comprobante** y **Solicitar certificado tributario**.
- El certificado tributario requiere proceso institucional verificable; el sitio no lo genera automáticamente. La solicitud y el comprobante no son equivalentes.
- El diseño del nuevo modal debe heredar tipografía, colores, botones y espaciados del sistema visual vigente, pendientes de cotejo con `styles.css`.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
