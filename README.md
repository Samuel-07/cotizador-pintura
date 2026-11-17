# Cotizador de Pintura

Sistema web completo para cotizar y gestionar el negocio de pintura (Bonao, RD). Funciona desde el iPhone con conexión o sin ella (offline).

## Funciones

### Cotizador
- Medición de paredes por área: ancho × alto en **metros, pies o centímetros** (conversión automática a m²).
- Descuento automático de **puertas, ventanas y otras aberturas**.
- **Techos** opcionales con precio propio.
- **Precios editables** de mano de obra (RD$/m²) y cargos adicionales.
- Resumen con áreas brutas/netas y total en RD$ (barra fija inferior siempre visible).
- Documento de cotización detallado por área (folio, mediciones pared por pared, plan de trabajo, pagos y firmas) listo para **Imprimir / Guardar PDF**.

### Gestión del negocio
- **Autoguardado**: todo se queda guardado en el dispositivo; si cierras y abres la app, sigues donde estabas.
- **Historial de cotizaciones**: "Guardar cotización del cliente" registra cada cotización con **folio (CT-2026-NNN)**, cliente, dirección y fecha. Filtra por estado, busca por cliente y vuelve a abrir o imprimir cualquier cotización.
- **Estados del trabajo**: borrador, confirmada, completada, cancelada.
- **Pagos de clientes**: registra cobros por cotización (monto, fecha, método, nota) y ve lo pagado vs. pendiente.
- **Agenda / calendario**: plan de trabajo con días estimados según m² y pintores, fecha de inicio/fin y calendario mensual con los días de trabajo marcados.
- **Empleados y pagos**: registra a tu equipo, el pago por día y los pagos realizados.
- **Dashboard**: cotizaciones activas/confirmadas/completadas, total cotizado, cobrado, por cobrar, pagado a empleados y margen aproximado, próximos trabajos y deudores.

### Calculadora de pintura
- Calcula **galones y cubetas** necesarias según el área a pintar, las manos (capas) y el rendimiento por galón (por defecto 30 m²·manos; una cubeta = 5 galones = 18.9 L cubre ~60–90 m² a dos manos).
- Botón para usar el área exacta de la cotización (paredes netas + techos).
- **Cobro de la consulta**: agrega el importe de la asesoría de cálculo como cargo a la cotización.

## Publicado
- GitHub Pages: https://samuel-07.github.io/cotizador-pintura/
- Cloudflare Pages: https://cotizador-pintura-c60.pages.dev/

## Uso offline en iPhone
Abre el enlace en Safari → botón Compartir → **"Añadir a pantalla de inicio"**. La app queda como ícono y funciona aunque no haya internet.

## Notas técnicas
- Datos en `localStorage` del propio dispositivo (sin servidor): `cp_db_v1` (cotizaciones, empleados, pagos), `cotizador_pintura_current` (borrador), `cotizador_pin` (PIN).
- **Acceso con PIN**: crea tu código la primera vez que entra (solo tú). "Restablecer PIN" también borra todos los datos.
- El PIN es una protección de cortesía en el navegador, suficiente para uso personal; no sustituye una autenticación de servidor.
