# RF1 - Gestión de Productos

## Historia de Usuario Principal

**Como** administrador del sistema de Milaccesorios  
**Quiero** gestionar el catálogo completo de productos de bisutería  
**Para que** pueda mantener actualizada la información de todos los productos disponibles

---

## RF1.1 Registrar, editar y eliminar productos

### Historia de Usuario RF1.1.1 - Registrar Producto

**Como** administrador  
**Quiero** registrar un nuevo producto en el sistema  
**Para que** esté disponible en el catálogo y pueda ser vendido

#### Criterios de Aceptación

- [ ] Debo poder ingresar nombre del producto (obligatorio, máximo 100 caracteres)
- [ ] Debo poder ingresar descripción del producto (obligatorio, máximo 500 caracteres)
- [ ] Debo poder establecer el precio de venta (obligatorio, mayor a 0)
- [ ] Debo poder asignar una categoría (obligatorio)
- [ ] Debo poder especificar el material principal (obligatorio)
- [ ] Debo poder definir el stock inicial (obligatorio, mayor o igual a 0)
- [ ] El sistema debe generar automáticamente un código único para el producto
- [ ] El sistema debe validar que todos los campos obligatorios estén completos
- [ ] El sistema debe mostrar un mensaje de confirmación al registrar exitosamente

#### Escenarios de Prueba

- **Escenario 1:** Registro exitoso con todos los datos válidos
- **Escenario 2:** Intento de registro con campos obligatorios vacíos
- **Escenario 3:** Intento de registro con precio negativo o cero
- **Escenario 4:** Registro con descripción que excede el límite de caracteres

---

### Historia de Usuario RF1.1.2 - Editar Producto

**Como** administrador  
**Quiero** editar la información de un producto existente  
**Para que** pueda mantener actualizada la información del catálogo

#### Criterios de Aceptación

- [ ] Debo poder buscar y seleccionar un producto por código o nombre
- [ ] Debo poder modificar todos los campos del producto excepto el código único
- [ ] El sistema debe mantener un historial de cambios con fecha y usuario
- [ ] El sistema debe validar que las modificaciones cumplan las mismas reglas que el registro
- [ ] Debo poder cancelar la edición sin guardar cambios
- [ ] El sistema debe mostrar un mensaje de confirmación al actualizar exitosamente

#### Escenarios de Prueba

- **Escenario 1:** Edición exitosa de producto existente
- **Escenario 2:** Búsqueda de producto inexistente
- **Escenario 3:** Modificación con datos inválidos
- **Escenario 4:** Cancelación de edición sin guardar

---

### Historia de Usuario RF1.1.3 - Eliminar Producto

**Como** administrador  
**Quiero** eliminar un producto del catálogo  
**Para que** no aparezca más en las consultas ni esté disponible para venta

#### Criterios de Aceptación

- [ ] Debo poder buscar y seleccionar un producto para eliminar
- [ ] El sistema debe solicitar confirmación antes de eliminar
- [ ] No debo poder eliminar productos que tienen pedidos pendientes
- [ ] El sistema debe realizar eliminación lógica (marcar como inactivo)
- [ ] Debo poder ver un historial de productos eliminados
- [ ] El sistema debe mostrar un mensaje de confirmación al eliminar exitosamente

#### Escenarios de Prueba

- **Escenario 1:** Eliminación exitosa de producto sin pedidos pendientes
- **Escenario 2:** Intento de eliminación de producto con pedidos pendientes
- **Escenario 3:** Cancelación de eliminación
- **Escenario 4:** Verificación de eliminación lógica

---

## RF1.2 Gestionar categorías y materiales de productos

### Historia de Usuario RF1.2.1 - Gestionar Categorías

**Como** administrador  
**Quiero** gestionar las categorías de productos  
**Para que** pueda clasificar y organizar el catálogo de manera eficiente

#### Criterios de Aceptación

- [ ] Debo poder crear nuevas categorías con nombre y descripción
- [ ] Debo poder editar categorías existentes
- [ ] Debo poder eliminar categorías que no estén siendo utilizadas
- [ ] El sistema debe validar que no existan categorías duplicadas
- [ ] Debo poder ver una lista de todas las categorías activas
- [ ] El sistema debe mostrar cuántos productos tiene cada categoría

#### Escenarios de Prueba

- **Escenario 1:** Creación exitosa de nueva categoría
- **Escenario 2:** Intento de crear categoría duplicada
- **Escenario 3:** Eliminación de categoría sin productos asociados
- **Escenario 4:** Intento de eliminación de categoría con productos asociados

---

### Historia de Usuario RF1.2.2 - Gestionar Materiales

**Como** administrador  
**Quiero** gestionar los materiales de los productos  
**Para que** pueda especificar correctamente los materiales utilizados en cada producto

#### Criterios de Aceptación

- [ ] Debo poder crear nuevos materiales con nombre y propiedades
- [ ] Debo poder editar materiales existentes
- [ ] Debo poder eliminar materiales que no estén siendo utilizados
- [ ] El sistema debe validar que no existan materiales duplicados
- [ ] Debo poder asignar múltiples materiales a un producto
- [ ] Debo poder especificar el porcentaje de cada material en un producto

#### Escenarios de Prueba
- **Escenario 1:** Creación exitosa de nuevo material
- **Escenario 2:** Asignación de múltiples materiales a un producto
- **Escenario 3:** Eliminación de material no utilizado
- **Escenario 4:** Intento de eliminación de material en uso

---

## RF1.3 Cargar imágenes y descripciones detalladas

### Historia de Usuario RF1.3.1 - Gestionar Imágenes de Productos
**Como** administrador  
**Quiero** cargar y gestionar imágenes de los productos  
**Para que** los clientes puedan visualizar los productos antes de comprar

#### Criterios de Aceptación

- [ ] Debo poder cargar múltiples imágenes por producto (máximo 5)
- [ ] El sistema debe aceptar formatos JPG, PNG y WebP
- [ ] Las imágenes no deben superar los 2MB cada una
- [ ] Debo poder establecer una imagen como principal
- [ ] Debo poder eliminar imágenes existentes
- [ ] El sistema debe redimensionar automáticamente las imágenes
- [ ] Debo poder cambiar el orden de las imágenes

#### Escenarios de Prueba

- **Escenario 1:** Carga exitosa de imagen válida
- **Escenario 2:** Intento de carga de archivo con formato no válido
- **Escenario 3:** Intento de carga de imagen que excede el tamaño máximo
- **Escenario 4:** Establecimiento de imagen principal
- **Escenario 5:** Eliminación de imagen existente

---

### Historia de Usuario RF1.3.2 - Descripciones Detalladas

**Como** administrador  
**Quiero** agregar descripciones detalladas a los productos  
**Para que** los clientes tengan toda la información necesaria sobre cada producto

#### Criterios de Aceptación

- [ ] Debo poder agregar una descripción corta (máximo 200 caracteres)
- [ ] Debo poder agregar una descripción detallada (máximo 1000 caracteres)
- [ ] Debo poder especificar dimensiones del producto
- [ ] Debo poder agregar instrucciones de cuidado y mantenimiento
- [ ] Debo poder incluir tiempo estimado de fabricación
- [ ] El sistema debe permitir formato básico de texto (negrita, cursiva)

#### Escenarios de Prueba

- **Escenario 1:** Agregado exitoso de descripciones completas
- **Escenario 2:** Validación de límites de caracteres
- **Escenario 3:** Uso de formato de texto básico
- **Escenario 4:** Guardado de información adicional del producto

---

## Entradas, Salidas y Procedimientos

### RF1.1 Registrar, editar y eliminar productos

#### Entradas

- **Datos del producto:** Nombre, descripción, precio, categoría, material, stock inicial
- **Imágenes:** Archivos JPG/PNG/WebP (máximo 5, hasta 2MB cada una)
- **Código de producto:** Generado automáticamente o manual
- **Usuario autenticado:** Con permisos de administración

#### Salidas

- **Confirmación de registro:** Mensaje de éxito con código de producto generado
- **Lista actualizada:** Catálogo de productos actualizado
- **Notificaciones:** Alertas de validación o errores
- **Logs de auditoría:** Registro de acciones realizadas

#### Procedimiento

1. **Validar autenticación y permisos** del usuario
2. **Validar datos de entrada** según reglas de negocio
3. **Verificar unicidad** del código de producto
4. **Procesar imágenes** (redimensionar, optimizar)
5. **Insertar/Actualizar** registro en base de datos
6. **Actualizar índices** de búsqueda
7. **Registrar en auditoría** la acción realizada
8. **Enviar notificación** de confirmación al usuario

---

### RF1.2 Gestionar categorías y materiales

#### Entradas

- **Datos de categoría:** Nombre, descripción, categoría padre (opcional)
- **Datos de material:** Nombre, propiedades, porcentaje de composición
- **Usuario autenticado:** Con permisos de administración

#### Salidas

- **Listas actualizadas:** Catálogos de categorías y materiales
- **Relaciones:** Mapeo de productos con categorías/materiales
- **Validaciones:** Mensajes de error por duplicados o referencias

#### Procedimiento

1. **Validar permisos** de usuario
2. **Verificar duplicados** en nombres
3. **Validar dependencias** antes de eliminaciones
4. **Actualizar relaciones** con productos existentes
5. **Sincronizar índices** de búsqueda
6. **Registrar cambios** en auditoría

---

### RF1.3 Cargar imágenes y descripciones detalladas

#### Entradas

- **Archivos de imagen:** JPG, PNG, WebP (máximo 2MB)
- **Descripciones:** Texto corto (200 chars) y detallado (1000 chars)
- **Metadatos:** Dimensiones, instrucciones de cuidado, tiempo de fabricación

#### Salidas

- **Imágenes procesadas:** Diferentes tamaños (thumbnail, medium, large)
- **URLs de acceso:** Rutas públicas a las imágenes
- **Metadatos estructurados:** Información organizada para búsqueda

#### Procedimiento

1. **Validar formato y tamaño** de archivos
2. **Procesar imágenes** (redimensionar, comprimir, generar thumbnails)
3. **Almacenar archivos** en sistema de archivos/cloud
4. **Generar URLs** de acceso público
5. **Asociar con producto** en base de datos
6. **Indexar contenido** para búsquedas

---

## Definición de Terminado (Definition of Done)

Para considerar completado el requerimiento RF1, se debe cumplir:

- [ ] Todas las historias de usuario están implementadas y probadas
- [ ] Las pruebas unitarias cubren al menos el 80% del código
- [ ] Las pruebas de integración funcionan correctamente
- [ ] La interfaz de usuario es responsive y accesible
- [ ] La documentación técnica está actualizada
- [ ] Se han realizado pruebas de usabilidad
- [ ] El código ha sido revisado y aprobado
- [ ] No existen bugs críticos o de alta prioridad pendientes

---

## Estimación de Esfuerzo

- **RF1.1:** 8 puntos de historia (16 horas)
- **RF1.2:** 5 puntos de historia (10 horas)  
- **RF1.3:** 8 puntos de historia (16 horas)

**Total RF1:** 21 puntos de historia (42 horas aproximadamente)


