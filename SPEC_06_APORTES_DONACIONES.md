# SPEC 06 — APORTES / DONACIONES

## Objetivo
Permitir realizar aportes económicos a la parroquia mediante una pasarela de pagos segura.

## Interfaz
La sección tendrá identidad visual diferenciada en tono vino oscuro y el mensaje principal:

**“Tu aporte sostiene una Iglesia más cercana.”**

## Valores
No se permitirá escribir libremente cualquier monto. Se mostrarán montos predeterminados:
- $10.000
- $30.000
- $50.000
- $100.000
- $200.000
- $500.000

Los valores podrán ajustarse posteriormente según decisión de la parroquia.

## Flujo
Usuario selecciona monto → Continuar al pago → Pasarela de pago → PSE / medio disponible → Proceso bancario → Volver al comercio → Verificación de transacción → Resultado en NOS UNE.

## Pasarela
La transacción deberá realizarse mediante una plataforma externa autorizada, por ejemplo **PlaceToPay** u otra elegida por la parroquia.

NOS UNE no almacenará:
- claves bancarias;
- números de tarjeta;
- credenciales financieras.

## Estados
Los estados de pago son responsabilidad de la pasarela. NOS UNE solo mostrará el resultado después de verificar la transacción.

Estados posibles:
- aprobada;
- pendiente;
- rechazada;
- cancelada.

## Criterio de aceptación
El usuario puede seleccionar un monto y ser transferido de forma segura al proceso de pago correspondiente.

## Fidelidad al diseño y flujo de interacción
- Conservar las **dos zonas** de `donation-layout`: mensaje institucional y caja de selección de aportes.
- Mantener los textos del HTML: sobretexto **HAZ TU APORTE**, título **Tu aporte sostiene una Iglesia más cercana.**, descripción, cierre **Gracias por caminar con nosotros.** y nota de pago seguro.
- La selección presenta exactamente **seis botones** en el orden: $10.000, $30.000, $50.000, $100.000, $200.000 y $500.000 COP. En el HTML **$30.000 está seleccionado inicialmente**; mantener dicho estado por defecto salvo decisión posterior.
- Al pulsar **Continuar al pago**, abrir primero el modal de confirmación existente (`paymentModal`), que muestra el monto seleccionado y la acción **Ir a la pasarela**.
- El texto del HTML indica que la pasarela todavía no está conectada. No presentar este prototipo como un pago real hasta integrar un proveedor autorizado y su verificación segura.
- El modal previo al pago es distinto del modal posterior de agradecimiento descrito en SPEC 07.

## Validación para la migración SDD / React
- Conservar el diseño y textos visibles del `index(2).html` salvo cambio expresamente especificado.
- Marcar por separado las funcionalidades presentes en el HTML y las que requieren implementación nueva.
- Revisar `styles.css`, `app.js` y recursos `img/` antes de declarar fidelidad visual completa; estos recursos no fueron suministrados.
- Verificar los criterios de aceptación del presente SPEC mediante pruebas reproducibles.
