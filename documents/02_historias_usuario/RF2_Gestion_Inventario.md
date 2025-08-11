# RF2 - Gestión de Inventario

## Historia de Usuario Principal

**Como** administrador del sistema de Milaccesorios  
**Quiero** controlar el inventario de todos los productos de bisutería  
**Para que** pueda mantener un control preciso del stock y evitar problemas de disponibilidad

---

## RF2.1: Controlar el stock por producto

### Historia de Usuario RF2.1.1 - Visualizar Stock Actual

**Como** administrador  
**Quiero** visualizar el stock actual de todos los productos  
**Para que** pueda conocer la disponibilidad en tiempo real

#### Criterios de Aceptación

- [ ] Debo poder ver una lista de todos los productos con su stock actual
- [ ] Debo poder filtrar productos por categoría, material o rango de stock
- [ ] Debo poder buscar productos específicos por nombre o código
- [ ] El sistema debe mostrar el stock mínimo definido para cada producto
- [ ] Debo poder ver el historial de movimientos de stock de cada producto
- [ ] El sistema debe actualizar el stock en tiempo real tras cada transacción
- [ ] Debo poder exportar el reporte de inventario a Excel/PDF

#### Escenarios de Prueba

- **Escenario 1:** Visualización correcta de stock de todos los productos
- **Escenario 2:** Filtrado por categoría específica
- **Escenario 3:** Búsqueda de producto por código
- **Escenario 4:** Verificación de actualización en tiempo real tras venta

---

### Historia de Usuario RF2.1.2 - Ajustar Stock Manualmente

**Como** administrador  
**Quiero** ajustar manualmente el stock de los productos  
**Para que** pueda corregir discrepancias o registrar movimientos especiales

#### Criterios de Aceptación

- [ ] Debo poder aumentar o disminuir el stock de cualquier producto
- [ ] Debo poder especificar el motivo del ajuste (robo, daño, corrección, etc.)
- [ ] El sistema debe registrar quién hizo el ajuste y cuándo
- [ ] Debo poder hacer ajustes masivos mediante carga de archivo
- [ ] El sistema debe validar que el stock no quede en números negativos
- [ ] Debo poder ver un historial completo de todos los ajustes realizados

#### Escenarios de Prueba

- **Escenario 1:** Ajuste individual exitoso con motivo válido
- **Escenario 2:** Intento de ajuste que deje stock negativo
- **Escenario 3:** Ajuste masivo mediante archivo Excel
- **Escenario 4:** Verificación de registro en historial de movimientos

---

### Historia de Usuario RF2.1.3 - Registrar Entradas de Mercancía

**Como** administrador  
**Quiero** registrar las entradas de nueva mercancía al inventario  
**Para que** el stock se actualice correctamente cuando reciba productos

#### Criterios de Aceptación

- [ ] Debo poder registrar entrada de productos existentes
- [ ] Debo poder especificar cantidad, fecha de entrada y proveedor
- [ ] Debo poder asignar un número de lote o referencia de entrada
- [ ] El sistema debe actualizar automáticamente el stock disponible
- [ ] Debo poder registrar el costo de adquisición por unidad
- [ ] Debo poder imprimir un comprobante de la entrada registrada

#### Escenarios de Prueba

- **Escenario 1:** Registro exitoso de entrada de mercancía nueva
- **Escenario 2:** Entrada con información de proveedor y costos
- **Escenario 3:** Verificación de actualización automática de stock
- **Escenario 4:** Generación de comprobante de entrada

---

## RF2.2: Generar alertas de inventario bajo

### Historia de Usuario RF2.2.1 - Configurar Alertas de Stock Mínimo

**Como** administrador  
**Quiero** configurar alertas automáticas cuando el stock esté bajo  
**Para que** pueda reabastecer productos antes de quedarme sin inventario

#### Criterios de Aceptación

- [ ] Debo poder establecer un stock mínimo diferente para cada producto
- [ ] Debo poder definir múltiples niveles de alerta (bajo, crítico)
- [ ] El sistema debe generar alertas automáticamente cuando se alcancen los límites
- [ ] Debo poder recibir notificaciones por email o en el sistema
- [ ] Debo poder configurar qué usuarios reciben las alertas
- [ ] Debo poder activar/desactivar alertas para productos específicos

#### Escenarios de Prueba

- **Escenario 1:** Configuración exitosa de stock mínimo para producto
- **Escenario 2:** Generación automática de alerta al alcanzar límite
- **Escenario 3:** Envío de notificación por email
- **Escenario 4:** Desactivación de alertas para producto específico

---

### Historia de Usuario RF2.2.2 - Visualizar Panel de Alertas

**Como** administrador  
**Quiero** visualizar un panel centralizado con todas las alertas de inventario  
**Para que** pueda tomar acciones rápidas sobre los productos con stock bajo

#### Criterios de Aceptación

- [ ] Debo poder ver una lista de todos los productos con alertas activas
- [ ] Debo poder filtrar alertas por nivel de criticidad
- [ ] Debo poder marcar alertas como "revisadas" o "en proceso"
- [ ] El sistema debe mostrar la fecha en que se activó cada alerta
- [ ] Debo poder acceder directamente al producto desde la alerta
- [ ] Debo poder generar órdenes de compra desde el panel de alertas

#### Escenarios de Prueba

- **Escenario 1:** Visualización correcta de panel con alertas activas
- **Escenario 2:** Filtrado por nivel de criticidad
- **Escenario 3:** Marcado de alerta como revisada
- **Escenario 4:** Navegación directa al producto desde alerta

---

### Historia de Usuario RF2.2.3 - Generar Reportes de Alertas

**Como** administrador  
**Quiero** generar reportes sobre las alertas de inventario  
**Para que** pueda analizar patrones y mejorar la gestión del stock

#### Criterios de Aceptación

- [ ] Debo poder generar reportes de alertas por período de tiempo
- [ ] Debo poder ver estadísticas de productos que más alertas generan
- [ ] Debo poder exportar reportes en formato Excel y PDF
- [ ] El sistema debe mostrar tiempo promedio de resolución de alertas
- [ ] Debo poder filtrar reportes por categoría de producto
- [ ] Debo poder programar reportes automáticos periódicos

#### Escenarios de Prueba

- **Escenario 1:** Generación exitosa de reporte mensual de alertas
- **Escenario 2:** Exportación a Excel con datos correctos
- **Escenario 3:** Filtrado por categoría específica
- **Escenario 4:** Configuración de reporte automático semanal

---

## Entradas, Salidas y Procedimientos

### RF2.1: Controlar el stock por producto

#### Entradas

- **Filtros de consulta:** Categoría, material, rango de stock, fechas
- **Criterios de búsqueda:** Código de producto, nombre, SKU
- **Ajustes de stock:** Cantidad, motivo, referencia, usuario responsable
- **Datos de entrada:** Proveedor, lote, fecha, costo unitario, cantidad

#### Salidas

- **Reporte de stock:** Lista completa con disponibilidades actuales
- **Historial de movimientos:** Registro cronológico de entradas/salidas
- **Alertas automáticas:** Notificaciones de stock bajo o agotado
- **Comprobantes:** Documentos de ajustes y entradas de mercancía
- **Métricas:** Valor total de inventario, rotación de productos

#### Procedimiento

1. **Autenticar usuario** y validar permisos de acceso
2. **Procesar filtros** y criterios de búsqueda aplicados
3. **Consultar base de datos** con índices optimizados
4. **Calcular métricas** en tiempo real (stock disponible, reservado, comprometido)
5. **Generar reporte** con formato solicitado
6. **Registrar auditoría** de consultas realizadas
7. **Notificar alertas** si se detectan productos bajo mínimo

---

### RF2.2: Generar alertas de inventario bajo

#### Entradas

- **Configuración de alertas:** Stock mínimo por producto, niveles de criticidad
- **Parámetros de notificación:** Usuarios destinatarios, frecuencia, canales
- **Umbrales personalizados:** Límites específicos por categoría o temporada
- **Preferencias de usuario:** Tipos de alerta a recibir

#### Salidas

- **Alertas automáticas:** Notificaciones en tiempo real y programadas
- **Panel de alertas:** Dashboard con estado actual de todas las alertas
- **Reportes de alertas:** Estadísticas y tendencias de alertas generadas
- **Notificaciones:** Emails, mensajes in-app, reportes programados
- **Recomendaciones:** Sugerencias de reabastecimiento automáticas

#### Procedimiento

1. **Monitorear niveles de stock** continuamente mediante jobs programados
2. **Evaluar umbrales** configurados para cada producto
3. **Generar alertas** cuando se superen los límites establecidos
4. **Clasificar criticidad** (bajo, crítico, agotado)
5. **Enviar notificaciones** según preferencias de usuarios
6. **Actualizar dashboard** de alertas en tiempo real
7. **Registrar historial** de alertas para análisis posterior
8. **Generar recomendaciones** de compra automáticas

---

## Dependencias Técnicas

### Integraciones Requeridas

- **Sistema de productos:** Para obtener información básica y categorías
- **Sistema de pedidos:** Para actualizar stock automáticamente tras ventas
- **Sistema de notificaciones:** Para envío de alertas por email/SMS
- **Sistema de reportes:** Para generación de informes consolidados

### Consideraciones de Rendimiento

- **Índices de base de datos:** Optimizados para consultas frecuentes de stock
- **Caché de consultas:** Para reportes que no cambian frecuentemente  
- **Procesamiento asíncrono:** Para cálculos complejos de métricas
- **Monitoreo en tiempo real:** Jobs ligeros que no impacten rendimiento

---

## Definición de Terminado (Definition of Done)

Para considerar completado el requerimiento RF2, se debe cumplir:

- [ ] Todas las historias de usuario están implementadas y probadas
- [ ] Las pruebas unitarias cubren al menos el 80% del código
- [ ] Las pruebas de integración funcionan correctamente
- [ ] El sistema de alertas funciona en tiempo real
- [ ] Las notificaciones se envían correctamente
- [ ] La interfaz de usuario es responsive y accesible
- [ ] La documentación técnica está actualizada
- [ ] Se han realizado pruebas de carga para el sistema de alertas
- [ ] El código ha sido revisado y aprobado
- [ ] No existen bugs críticos o de alta prioridad pendientes

---

## Estimación de Esfuerzo

- **RF2.1:** 10 puntos de historia (20 horas)
- **RF2.2:** 8 puntos de historia (16 horas)

**Total RF2:** 18 puntos de historia (36 horas aproximadamente)

---

## Dependencias

- **Depende de:** RF1 (Gestión de Productos) - Necesario para tener productos en el sistema
- **Prerrequisito:** Base de datos configurada y funcional
- **Integración con:** RF4 (Gestión de Pedidos) - Para actualizar stock automáticamente
