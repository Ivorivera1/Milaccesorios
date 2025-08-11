# RF4 - Gestión de Pedidos

## Historia de Usuario Principal

**Como** administrador del sistema de Milaccesorios  
**Quiero** gestionar todo el ciclo de vida de los pedidos de bisutería  
**Para que** pueda controlar eficientemente el proceso desde la creación hasta la entrega

---

## RF4.1: Crear y hacer seguimiento de pedidos

### Historia de Usuario RF4.1.1 - Crear Nuevo Pedido

**Como** administrador  
**Quiero** crear nuevos pedidos para los clientes  
**Para que** pueda registrar sus solicitudes de compra de manera organizada

#### Criterios de Aceptación del RF4.1.1

- [ ] Debo poder seleccionar un cliente existente o crear uno nuevo
- [ ] Debo poder agregar múltiples productos al pedido con sus cantidades
- [ ] El sistema debe verificar la disponibilidad de stock automáticamente
- [ ] Debo poder aplicar descuentos al pedido (porcentaje o monto fijo)
- [ ] El sistema debe calcular automáticamente el total del pedido
- [ ] Debo poder especificar fecha estimada de entrega
- [ ] Debo poder agregar notas especiales o instrucciones del cliente
- [ ] El sistema debe generar automáticamente un número de pedido único
- [ ] Debo poder guardar el pedido como borrador antes de confirmarlo

#### Escenarios de Prueba del RF4.1.1

- **Escenario 1:** Creación exitosa de pedido con productos disponibles
- **Escenario 2:** Intento de crear pedido con productos sin stock suficiente
- **Escenario 3:** Aplicación de descuento y cálculo correcto del total
- **Escenario 4:** Guardado como borrador y posterior confirmación

---

### Historia de Usuario RF4.1.2 - Modificar Pedido Existente

**Como** administrador  
**Quiero** modificar pedidos existentes mientras estén en estados permitidos  
**Para que** pueda ajustar cantidades o productos según cambios del cliente

#### Criterios de Aceptación del RF4.1.2

- [ ] Debo poder modificar pedidos en estado "Pendiente" o "En Preparación"
- [ ] No debo poder modificar pedidos "Enviados" o "Entregados"
- [ ] Debo poder agregar, quitar o cambiar cantidades de productos
- [ ] El sistema debe recalcular automáticamente el total tras modificaciones
- [ ] Debo poder cambiar la fecha estimada de entrega
- [ ] El sistema debe registrar un historial de todas las modificaciones
- [ ] Debo poder notificar al cliente sobre los cambios realizados

#### Escenarios de Prueba del RF4.1.2

- **Escenario 1:** Modificación exitosa de pedido en estado "Pendiente"
- **Escenario 2:** Intento de modificación de pedido "Enviado"
- **Escenario 3:** Adición de productos y recálculo automático
- **Escenario 4:** Registro correcto en historial de modificaciones

---

### Historia de Usuario RF4.1.3 - Hacer Seguimiento de Pedidos

**Como** administrador  
**Quiero** hacer seguimiento detallado del estado de todos los pedidos  
**Para que** pueda monitorear el progreso y informar a los clientes

#### Criterios de Aceptación del RF4.1.3

- [ ] Debo poder ver una lista de todos los pedidos con filtros por estado
- [ ] Debo poder buscar pedidos por número, cliente o fecha
- [ ] El sistema debe mostrar tiempo transcurrido desde creación del pedido
- [ ] Debo poder ver detalles completos de cada pedido
- [ ] Debo poder generar reportes de pedidos por período
- [ ] El sistema debe mostrar alertas para pedidos con retrasos
- [ ] Debo poder exportar lista de pedidos a Excel/PDF

#### Escenarios de Prueba del RF4.1.3

- **Escenario 1:** Visualización correcta de lista con filtros
- **Escenario 2:** Búsqueda exitosa por diferentes criterios
- **Escenario 3:** Generación de alerta para pedido con retraso
- **Escenario 4:** Exportación correcta de reporte

---

## RF4.2: Actualizar estado del pedido

### Historia de Usuario RF4.2.1 - Gestionar Estados de Pedido

**Como** administrador  
**Quiero** actualizar los estados de los pedidos de manera controlada  
**Para que** refleje correctamente el progreso en el proceso de producción y entrega

#### Criterios de Aceptación del RF4.2.1

- [ ] Debo poder cambiar estados siguiendo flujo: Pendiente → En Producción → Enviado → Entregado
- [ ] No debo poder saltar estados o retroceder sin justificación
- [ ] Debo poder agregar notas explicativas al cambiar estado
- [ ] El sistema debe registrar fecha/hora y usuario que hizo el cambio
- [ ] Debo poder establecer fecha estimada para cada estado
- [ ] El sistema debe enviar notificaciones automáticas al cliente (opcional)
- [ ] Debo poder ver timeline completo de cambios de estado

#### Escenarios de Prueba del RF4.2.1

- **Escenario 1:** Cambio exitoso siguiendo flujo correcto de estados
- **Escenario 2:** Intento de salto de estado no permitido
- **Escenario 3:** Adición de notas explicativas al cambio
- **Escenario 4:** Verificación de registro en timeline

---

### Historia de Usuario RF4.2.2 - Estado Pendiente

**Como** administrador  
**Quiero** gestionar pedidos en estado "Pendiente"  
**Para que** pueda revisar y confirmar antes de iniciar producción

#### Criterios de Aceptación del RF4.2.2

- [ ] Los pedidos nuevos deben iniciarse automáticamente en estado "Pendiente"
- [ ] Debo poder revisar disponibilidad de materiales antes de confirmar
- [ ] Debo poder estimar tiempo de producción requerido
- [ ] Debo poder confirmar o rechazar el pedido
- [ ] Si rechazo, debo poder especificar motivo y notificar al cliente
- [ ] Debo poder reservar stock al confirmar el pedido

#### Escenarios de Prueba del RF4.2.2

- **Escenario 1:** Confirmación exitosa de pedido pendiente
- **Escenario 2:** Rechazo de pedido con motivo justificado
- **Escenario 3:** Reserva automática de stock al confirmar
- **Escenario 4:** Verificación de disponibilidad de materiales

---

### Historia de Usuario RF4.2.3 - Estado En Producción

**Como** administrador  
**Quiero** gestionar pedidos "En Producción"  
**Para que** pueda monitorear el avance de fabricación de los productos

#### Criterios de Aceptación del RF4.2.3

- [ ] Debo poder ver lista de todos los pedidos en producción
- [ ] Debo poder registrar progreso de producción (porcentaje completado)
- [ ] Debo poder asignar responsable de producción
- [ ] Debo poder estimar fecha de finalización de producción
- [ ] Debo poder agregar fotos del progreso de producción
- [ ] El sistema debe alertar si hay retrasos en la producción

#### Escenarios de Prueba del RF4.2.3

- **Escenario 1:** Registro exitoso de progreso de producción
- **Escenario 2:** Asignación de responsable de producción
- **Escenario 3:** Carga de fotos de progreso
- **Escenario 4:** Generación de alerta por retraso

---

### Historia de Usuario RF4.2.4 - Estado Enviado

**Como** administrador  
**Quiero** gestionar pedidos "Enviados"  
**Para que** pueda hacer seguimiento de las entregas

#### Criterios de Aceptación del RF4.2.4

- [ ] Debo poder registrar información de envío (transportadora, guía)
- [ ] Debo poder especificar fecha de envío y estimada de entrega
- [ ] Debo poder generar documentos de envío
- [ ] El sistema debe notificar automáticamente al cliente del envío
- [ ] Debo poder hacer seguimiento del estado de entrega
- [ ] Debo poder registrar intentos de entrega fallidos

#### Escenarios de Prueba del RF4.2.4

- **Escenario 1:** Registro exitoso de información de envío
- **Escenario 2:** Generación automática de notificación al cliente
- **Escenario 3:** Seguimiento de estado de entrega
- **Escenario 4:** Registro de intento de entrega fallido

---

### Historia de Usuario RF4.2.5 - Estado Entregado

**Como** administrador  
**Quiero** gestionar pedidos "Entregados"  
**Para que** pueda confirmar la finalización exitosa del proceso

#### Criterios de Aceptación del RF4.2.5

- [ ] Debo poder confirmar la entrega exitosa del pedido
- [ ] Debo poder registrar fecha y hora exacta de entrega
- [ ] Debo poder registrar quién recibió el pedido
- [ ] El sistema debe actualizar automáticamente el stock vendido
- [ ] Debo poder solicitar confirmación de satisfacción al cliente
- [ ] El pedido debe quedar marcado como completado permanentemente

#### Escenarios de Prueba del RF4.2.5

- **Escenario 1:** Confirmación exitosa de entrega
- **Escenario 2:** Actualización automática de stock vendido
- **Escenario 3:** Registro de datos de recepción
- **Escenario 4:** Envío de solicitud de satisfacción al cliente

---

## Funcionalidades Adicionales

### Historia de Usuario RF4.3 - Cancelar Pedidos

**Como** administrador  
**Quiero** poder cancelar pedidos cuando sea necesario  
**Para que** pueda manejar situaciones excepcionales

#### Criterios de Aceptación del RF4.3

- [ ] Debo poder cancelar pedidos en cualquier estado antes de "Enviado"
- [ ] Debo especificar motivo de cancelación (cliente, falta stock, otros)
- [ ] El sistema debe liberar automáticamente el stock reservado
- [ ] Debo poder notificar al cliente sobre la cancelación
- [ ] El pedido cancelado debe mantener su historial para auditoría
- [ ] Debo poder generar nota de crédito si hubo pago adelantado

#### Escenarios de Prueba del RF4.3

- **Escenario 1:** Cancelación exitosa de pedido pendiente
- **Escenario 2:** Liberación automática de stock reservado
- **Escenario 3:** Intento de cancelación de pedido enviado
- **Escenario 4:** Generación de nota de crédito

---

## Entradas, Salidas y Procedimientos

### RF4.1: Crear y hacer seguimiento de pedidos

#### Entradas
- **Información del cliente:** Identificador de cliente existente o datos para nuevo cliente
- **Detalles del pedido:** Lista de productos, cantidades, precios, descuentos aplicables
- **Datos de entrega:** Dirección, fecha estimada, instrucciones especiales, método de envío
- **Información de pago:** Método, estado, referencia de transacción
- **Usuario operador:** Vendedor o administrador autenticado con permisos

#### Salidas
- **Número de pedido:** Identificador único generado automáticamente
- **Confirmación de pedido:** Documento PDF con detalles completos
- **Reserva de stock:** Productos apartados del inventario disponible
- **Notificaciones:** Alerts al cliente y equipo interno sobre nuevo pedido
- **Estados actualizados:** Dashboard con progreso en tiempo real

#### Procedimiento
1. **Validar autenticación** del usuario y permisos para crear pedidos
2. **Verificar cliente** existente o crear nuevo registro si es necesario
3. **Validar disponibilidad** de stock para todos los productos solicitados
4. **Calcular totales** incluyendo impuestos, descuentos y costos de envío
5. **Generar número único** de pedido según secuencia establecida
6. **Reservar stock** de productos para evitar sobreventa
7. **Insertar pedido** en base de datos con estado inicial "Pendiente"
8. **Enviar confirmación** al cliente y notificar al equipo de producción

---

### RF4.2: Actualizar estado del pedido

#### Entradas
- **Identificador de pedido:** Número único para localizar el pedido específico
- **Nuevo estado:** Pendiente, En Producción, Enviado, Entregado, Cancelado
- **Notas de actualización:** Comentarios explicativos sobre el cambio de estado
- **Información adicional:** Datos de envío, guía de transportadora, fecha estimada
- **Usuario responsable:** Operador autorizado para realizar el cambio

#### Salidas
- **Confirmación de cambio:** Verificación del estado actualizado exitosamente
- **Timeline actualizado:** Historial cronológico con todos los cambios
- **Notificaciones automáticas:** Comunicación al cliente sobre el progreso
- **Documentos generados:** Guías de envío, facturas, comprobantes según estado
- **Métricas actualizadas:** Dashboard con estadísticas de pedidos por estado

#### Procedimiento
1. **Localizar pedido** en base de datos usando identificador único
2. **Validar transición** de estado según reglas de negocio establecidas
3. **Verificar permisos** del usuario para realizar el cambio solicitado
4. **Actualizar registro** del pedido con nuevo estado y timestamp
5. **Registrar en timeline** el cambio con usuario responsable y notas
6. **Ejecutar acciones específicas** según el nuevo estado (envío de documentos, liberación de stock)
7. **Enviar notificaciones** automáticas al cliente según configuración
8. **Actualizar métricas** y dashboard de seguimiento en tiempo real

---

### RF4.3: Cancelar pedidos

#### Entradas
- **Identificador de pedido:** Número único del pedido a cancelar
- **Motivo de cancelación:** Razón específica (cliente, falta stock, error, otros)
- **Autorización:** Confirmación del usuario con permisos para cancelación
- **Información de reembolso:** Datos para procesamiento de devolución si aplica

#### Salidas
- **Confirmación de cancelación:** Verificación del pedido cancelado exitosamente
- **Liberación de stock:** Productos devueltos al inventario disponible
- **Documentos de cancelación:** Nota de crédito, comprobante de cancelación
- **Notificación al cliente:** Comunicación sobre la cancelación y próximos pasos
- **Registro de auditoría:** Trazabilidad completa de la acción realizada

#### Procedimiento
1. **Verificar estado actual** del pedido (solo cancelable antes de "Enviado")
2. **Validar permisos** del usuario para realizar cancelaciones
3. **Solicitar confirmación** explícita del usuario operador
4. **Liberar stock reservado** devolviendo productos al inventario
5. **Actualizar estado** del pedido a "Cancelado" con motivo registrado
6. **Generar documentos** de cancelación según políticas empresariales
7. **Procesar reembolso** si hay pagos adelantados registrados
8. **Notificar stakeholders** relevantes sobre la cancelación

---

## Integraciones y Dependencias del Sistema

### Módulos Relacionados
- **Gestión de inventario:** Para verificación y actualización de stock en tiempo real
- **Gestión de clientes:** Para validación de información y historial de compras
- **Sistema de productos:** Para obtener precios, descripciones y disponibilidad
- **Motor de notificaciones:** Para comunicaciones automáticas con clientes
- **Sistema de pagos:** Para procesamiento de transacciones y reembolsos

### APIs y Servicios Externos
- **Servicios de mensajería:** Email, SMS para notificaciones a clientes
- **Transportadoras:** Integración para generación de guías y seguimiento
- **Pasarelas de pago:** Para procesamiento seguro de transacciones
- **Sistemas ERP:** Si existe integración con contabilidad externa

### Consideraciones de Rendimiento
- **Transacciones ACID:** Para garantizar consistencia en operaciones críticas
- **Índices optimizados:** Para búsquedas rápidas por número, cliente, estado
- **Cache de consultas:** Para reportes de estado que se consultan frecuentemente
- **Procesamiento asíncrono:** Para notificaciones y actualizaciones no críticas

---

## Definición de Terminado (Definition of Done)

Para considerar completado el requerimiento RF4, se debe cumplir:

- [ ] Todas las historias de usuario están implementadas y probadas
- [ ] Las pruebas unitarias cubren al menos el 80% del código
- [ ] Las pruebas de integración funcionan correctamente
- [ ] El flujo de estados funciona sin errores
- [ ] Las notificaciones automáticas funcionan correctamente
- [ ] La integración con inventario actualiza stock correctamente
- [ ] La interfaz de usuario es responsive y accesible
- [ ] La documentación técnica está actualizada
- [ ] Se han realizado pruebas de flujo completo end-to-end
- [ ] El código ha sido revisado y aprobado
- [ ] No existen bugs críticos o de alta prioridad pendientes

---

## Estimación de Esfuerzo

- **RF4.1:** 12 puntos de historia (24 horas)
- **RF4.2:** 15 puntos de historia (30 horas)
- **RF4.3:** 5 puntos de historia (10 horas)

**Total RF4:** 32 puntos de historia (64 horas aproximadamente)

---

## Dependencias

- **Depende de:** RF2 (Gestión de Inventario) - Para verificar y actualizar stock
- **Depende de:** RF3 (Gestión de Clientes) - Para asociar pedidos con clientes
- **Se integra con:** RF1 (Gestión de Productos) - Para agregar productos a pedidos
- **Prerrequisito:** Base de datos configurada y funcional
- **Integración opcional:** Sistema de notificaciones por email/SMS
