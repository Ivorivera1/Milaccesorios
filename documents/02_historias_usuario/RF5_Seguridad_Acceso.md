# RF5 - Seguridad y Acceso

## Historia de Usuario Principal

**Como** propietario del sistema de Milaccesorios  
**Quiero** implementar un sistema robusto de seguridad y control de acceso  
**Para que** la información de mi negocio esté protegida y solo usuarios autorizados puedan acceder

---

## RF5.1: Autenticación de usuarios

### Historia de Usuario RF5.1.1 - Inicio de Sesión

**Como** usuario del sistema  
**Quiero** iniciar sesión de manera segura  
**Para que** pueda acceder a las funcionalidades según mi rol asignado

#### Criterios de Aceptación del RF5.1.1

- [ ] Debo poder ingresar mi nombre de usuario y contraseña
- [ ] El sistema debe validar las credenciales contra la base de datos
- [ ] La contraseña debe estar encriptada en la base de datos
- [ ] Debo recibir mensaje de error claro si las credenciales son incorrectas
- [ ] El sistema debe registrar fecha y hora de cada intento de acceso
- [ ] Debo poder permanecer conectado por tiempo definido (sesión)
- [ ] El sistema debe bloquear temporalmente tras varios intentos fallidos
- [ ] Debo poder acceder directamente al panel según mi rol tras login exitoso

#### Escenarios de Prueba del RF5.1.1

- **Escenario 1:** Login exitoso con credenciales válidas
- **Escenario 2:** Login fallido con credenciales incorrectas
- **Escenario 3:** Bloqueo temporal tras múltiples intentos fallidos
- **Escenario 4:** Redirección correcta según rol del usuario

---

### Historia de Usuario RF5.1.2 - Gestión de Contraseñas

**Como** usuario del sistema  
**Quiero** gestionar mi contraseña de manera segura  
**Para que** pueda mantener mi cuenta protegida

#### Criterios de Aceptación del RF5.1.2

- [ ] Debo poder cambiar mi contraseña actual proporcionando la anterior
- [ ] Las contraseñas deben cumplir política de seguridad (mínimo 8 caracteres, mayúsculas, números)
- [ ] Debo recibir confirmación cuando se cambie la contraseña exitosamente
- [ ] No debo poder usar las últimas 3 contraseñas utilizadas
- [ ] El sistema debe forzar cambio de contraseña cada 90 días (opcional)
- [ ] Debo poder solicitar restablecimiento si olvido mi contraseña
- [ ] Las contraseñas temporales deben expirar en 24 horas

#### Escenarios de Prueba del RF5.1.2

- **Escenario 1:** Cambio exitoso de contraseña con política cumplida
- **Escenario 2:** Intento de cambio con contraseña débil
- **Escenario 3:** Intento de reutilizar contraseña reciente
- **Escenario 4:** Restablecimiento por olvido de contraseña

---

### Historia de Usuario RF5.1.3 - Gestión de Sesiones

**Como** administrador del sistema  
**Quiero** gestionar las sesiones de usuarios activos  
**Para que** pueda controlar el acceso y seguridad del sistema

#### Criterios de Aceptación del RF5.1.3

- [ ] Debo poder ver lista de usuarios actualmente conectados
- [ ] Debo poder ver información de cada sesión (usuario, IP, tiempo de conexión)
- [ ] Debo poder cerrar sesiones de usuarios específicos remotamente
- [ ] Las sesiones deben expirar automáticamente tras inactividad (30 minutos)
- [ ] Los usuarios deben recibir advertencia antes de expiración de sesión
- [ ] Debo poder configurar tiempo de expiración de sesiones
- [ ] El sistema debe registrar todos los inicios y cierres de sesión

#### Escenarios de Prueba del RF5.1.3

- **Escenario 1:** Visualización correcta de sesiones activas
- **Escenario 2:** Cierre remoto exitoso de sesión específica
- **Escenario 3:** Expiración automática por inactividad
- **Escenario 4:** Advertencia de expiración próxima

---

## RF5.2: Gestión de roles (Administrador, Vendedor)

### Historia de Usuario RF5.2.1 - Definir Roles y Permisos

**Como** administrador del sistema  
**Quiero** definir roles con permisos específicos  
**Para que** cada usuario tenga acceso solo a las funcionalidades necesarias para su trabajo

#### Criterios de Aceptación del RF5.2.1

- [ ] Debo poder crear rol "Administrador" con acceso completo al sistema
- [ ] Debo poder crear rol "Vendedor" con acceso limitado a ventas y consultas
- [ ] Cada rol debe tener permisos específicos para cada módulo (Crear, Leer, Actualizar, Eliminar)
- [ ] Debo poder personalizar permisos por rol según necesidades del negocio
- [ ] Los permisos deben aplicarse automáticamente según el rol asignado
- [ ] Debo poder ver matriz de permisos por rol de manera clara
- [ ] Los cambios de permisos deben aplicarse inmediatamente

#### Permisos por Rol

**Administrador:**
- [ ] Gestión completa de productos (CRUD)
- [ ] Gestión completa de inventario (CRUD)
- [ ] Gestión completa de clientes (CRUD)
- [ ] Gestión completa de pedidos (CRUD)
- [ ] Acceso a todos los reportes
- [ ] Gestión de usuarios y roles
- [ ] Configuración del sistema

**Vendedor:**
- [ ] Consulta de productos (solo lectura)
- [ ] Consulta de inventario (solo lectura)
- [ ] Gestión básica de clientes (crear, editar, consultar)
- [ ] Gestión de pedidos (crear, editar estado hasta "En Producción")
- [ ] Reportes básicos de ventas
- [ ] No acceso a configuración ni gestión de usuarios

#### Escenarios de Prueba del RF5.2.1

- **Escenario 1:** Creación exitosa de roles con permisos diferenciados
- **Escenario 2:** Verificación de acceso según rol de Administrador
- **Escenario 3:** Verificación de limitaciones de rol Vendedor
- **Escenario 4:** Aplicación inmediata de cambios de permisos

---

### Historia de Usuario RF5.2.2 - Asignar Roles a Usuarios

**Como** administrador del sistema  
**Quiero** asignar roles específicos a cada usuario  
**Para que** tengan los permisos apropiados según su función en la empresa

#### Criterios de Aceptación del RF5.2.2

- [ ] Debo poder asignar un rol específico a cada usuario al crearlo
- [ ] Debo poder cambiar el rol de un usuario existente
- [ ] Los cambios de rol deben aplicarse inmediatamente
- [ ] Debo poder ver qué rol tiene asignado cada usuario
- [ ] No debo poder eliminar mi propio rol de administrador si soy el único
- [ ] Debo recibir confirmación antes de cambios importantes de rol
- [ ] El sistema debe registrar todos los cambios de rol con fecha y responsable

#### Escenarios de Prueba del RF5.2.2

- **Escenario 1:** Asignación exitosa de rol a usuario nuevo
- **Escenario 2:** Cambio de rol de usuario existente
- **Escenario 3:** Intento de eliminar último administrador
- **Escenario 4:** Registro correcto de cambios en historial

---

### Historia de Usuario RF5.2.3 - Control de Acceso Basado en Roles

**Como** usuario del sistema  
**Quiero** que el sistema me permita acceder solo a funcionalidades autorizadas  
**Para que** la interfaz muestre únicamente las opciones disponibles para mi rol

#### Criterios de Aceptación del RF5.2.3

- [ ] El menú principal debe mostrar solo opciones disponibles para mi rol
- [ ] Los botones y acciones en cada pantalla deben responder a mis permisos
- [ ] Debo recibir mensaje de error si intento acceder a función no autorizada
- [ ] Las URLs directas deben estar protegidas contra acceso no autorizado
- [ ] Los reportes deben mostrar solo información que tengo permitido ver
- [ ] La interfaz debe indicar claramente mi rol actual
- [ ] Debo poder cerrar sesión desde cualquier pantalla

#### Escenarios de Prueba del RF5.2.3

- **Escenario 1:** Menú muestra solo opciones autorizadas para vendedor
- **Escenario 2:** Administrador ve todas las opciones disponibles
- **Escenario 3:** Acceso directo por URL es bloqueado correctamente
- **Escenario 4:** Mensajes de error apropiados para acceso no autorizado

---

## Funcionalidades Adicionales de Seguridad

### Historia de Usuario RF5.3 - Auditoría y Registros

**Como** administrador del sistema  
**Quiero** mantener registros detallados de todas las actividades  
**Para que** pueda auditar el uso del sistema y detectar problemas de seguridad

#### Criterios de Aceptación del RF5.3

- [ ] El sistema debe registrar todos los accesos exitosos y fallidos
- [ ] Debo poder ver quién hizo qué cambios y cuándo
- [ ] Los registros deben incluir IP de origen y navegador utilizado
- [ ] Debo poder filtrar registros por usuario, fecha o tipo de acción
- [ ] Los registros de auditoría no deben ser modificables por usuarios
- [ ] Debo poder exportar registros de auditoría
- [ ] Los registros deben conservarse por al menos 6 meses

#### Escenarios de Prueba del RF5.3

- **Escenario 1:** Registro correcto de acceso exitoso
- **Escenario 2:** Registro de cambios realizados por usuario
- **Escenario 3:** Filtrado exitoso de registros por criterios
- **Escenario 4:** Exportación de registros de auditoría

---

### Historia de Usuario RF5.4 - Configuración de Seguridad

**Como** administrador del sistema  
**Quiero** configurar parámetros de seguridad del sistema  
**Para que** pueda adaptar las políticas a las necesidades de mi empresa

#### Criterios de Aceptación del RF5.4

- [ ] Debo poder configurar política de contraseñas (longitud, complejidad)
- [ ] Debo poder establecer tiempo de expiración de sesiones
- [ ] Debo poder configurar número de intentos fallidos antes de bloqueo
- [ ] Debo poder definir tiempo de bloqueo por intentos fallidos
- [ ] Debo poder activar/desactivar registro de auditoría detallado
- [ ] Debo poder configurar notificaciones de seguridad
- [ ] Los cambios de configuración deben aplicarse inmediatamente

#### Escenarios de Prueba del RF5.4

- **Escenario 1:** Configuración exitosa de política de contraseñas
- **Escenario 2:** Cambio de tiempo de expiración de sesiones
- **Escenario 3:** Aplicación inmediata de nueva configuración
- **Escenario 4:** Validación de nuevas políticas en login

---

## Entradas, Salidas y Procedimientos

### RF5.1: Autenticación de usuarios

#### Entradas
- **Credenciales de usuario:** Nombre de usuario y contraseña
- **Información de sesión:** IP de origen, navegador, dispositivo
- **Políticas de seguridad:** Reglas de contraseña, intentos permitidos, duración de sesión
- **Tokens de seguridad:** Para autenticación multifactor si está habilitada

#### Salidas
- **Token de sesión:** JWT o cookie segura para mantener autenticación
- **Perfil de usuario:** Información básica y roles asignados
- **Permisos activos:** Lista de funcionalidades accesibles
- **Logs de auditoría:** Registro de intentos de acceso exitosos y fallidos
- **Alertas de seguridad:** Notificaciones por accesos sospechosos

#### Procedimiento
1. **Recibir credenciales** a través de formulario seguro con HTTPS
2. **Validar formato** de usuario y contraseña según políticas
3. **Consultar base de datos** para verificar existencia del usuario
4. **Verificar contraseña** usando hash seguro (bcrypt, Argon2)
5. **Aplicar políticas** de bloqueo por intentos fallidos
6. **Generar token de sesión** con expiración configurada
7. **Registrar evento** en logs de auditoría con detalles completos
8. **Establecer contexto** de seguridad para requests posteriores

---

### RF5.2: Gestión de roles (Administrador, Vendedor)

#### Entradas
- **Definición de roles:** Nombre, descripción, permisos específicos por módulo
- **Asignación de usuarios:** Mapeo de usuarios a roles específicos
- **Matriz de permisos:** CRUD detallado por cada funcionalidad del sistema
- **Configuración de acceso:** Restricciones por IP, horarios, dispositivos

#### Salidas
- **Roles configurados:** Sistema de roles activo con permisos definidos
- **Control de acceso:** Verificación automática en cada operación
- **Mensajes de autorización:** Respuestas claras sobre permisos denegados
- **Reportes de acceso:** Estadísticas de uso por rol y usuario
- **Configuración exportable:** Backup de políticas de seguridad

#### Procedimiento
1. **Definir roles base** (Administrador, Vendedor) con permisos estándar
2. **Crear matriz de permisos** detallada por cada endpoint/funcionalidad
3. **Implementar middleware** de autorización en todas las rutas protegidas
4. **Validar permisos** en tiempo real antes de cada operación
5. **Cachear permisos** del usuario para optimizar rendimiento
6. **Aplicar principio** de menor privilegio por defecto
7. **Registrar violaciones** de acceso para análisis de seguridad
8. **Sincronizar cambios** inmediatamente en sesiones activas

---

### RF5.3: Auditoría y registros

#### Entradas
- **Eventos del sistema:** Todas las acciones de usuarios y sistema
- **Contexto de seguridad:** Usuario, IP, timestamp, recurso accedido
- **Configuración de auditoría:** Nivel de detalle, retención, filtros
- **Criterios de búsqueda:** Filtros para consultas de logs

#### Salidas
- **Logs estructurados:** Registros en formato JSON para análisis
- **Reportes de auditoría:** Resúmenes por período, usuario, acción
- **Alertas de seguridad:** Detección automática de patrones sospechosos
- **Exports de compliance:** Datos formateados para auditorías externas

#### Procedimiento
1. **Interceptar todas las acciones** mediante middleware universal
2. **Extraer contexto completo** de cada operación realizada
3. **Estructurar logs** con formato estándar y campos requeridos
4. **Almacenar de forma inmutable** en sistema de logs dedicado
5. **Indexar para búsquedas** rápidas por múltiples criterios
6. **Implementar retención** automática según políticas definidas
7. **Generar alertas** automáticas por patrones anómalos
8. **Exportar bajo demanda** con filtros y formato requerido

---

## Arquitectura de Seguridad

### Componentes Principales
- **Servidor de autenticación:** Manejo centralizado de credenciales y tokens
- **Motor de autorización:** Evaluación de permisos en tiempo real
- **Sistema de auditoría:** Captura y almacenamiento inmutable de eventos
- **Monitor de seguridad:** Detección de anomalías y respuesta automática

### Tecnologías Implementadas
- **Hashing de contraseñas:** bcrypt con salt único por usuario
- **Tokens de sesión:** JWT con firma HMAC y expiración configurable
- **Encriptación de datos:** AES-256 para información sensible
- **Comunicación segura:** TLS 1.3 para todas las conexiones

### Políticas de Seguridad
- **Contraseñas fuertes:** Mínimo 8 caracteres, mayúsculas, números, símbolos
- **Bloqueo por intentos:** 5 intentos fallidos = bloqueo temporal de 15 minutos
- **Expiración de sesión:** 30 minutos de inactividad o 8 horas máximo
- **Rotación de tokens:** Renovación automática antes de expiración

---

## Definición de Terminado (Definition of Done)

Para considerar completado el requerimiento RF5, se debe cumplir:

- [ ] Todas las historias de usuario están implementadas y probadas
- [ ] Las pruebas de seguridad han sido realizadas y aprobadas
- [ ] Las contraseñas están correctamente encriptadas
- [ ] Los roles y permisos funcionan según especificaciones
- [ ] Los registros de auditoría funcionan correctamente
- [ ] Las sesiones se gestionan de manera segura
- [ ] Las pruebas de penetración básicas han sido superadas
- [ ] La documentación de seguridad está completa
- [ ] El código ha sido revisado por experto en seguridad
- [ ] No existen vulnerabilidades críticas o de alta prioridad

---

## Estimación de Esfuerzo

- **RF5.1:** 10 puntos de historia (20 horas)
- **RF5.2:** 12 puntos de historia (24 horas)
- **RF5.3:** 6 puntos de historia (12 horas)
- **RF5.4:** 4 puntos de historia (8 horas)

**Total RF5:** 32 puntos de historia (64 horas aproximadamente)

---

## Dependencias

- **Prerrequisito fundamental** para todos los demás módulos
- **Base de datos:** Tablas de usuarios, roles y permisos configuradas
- **Integración con:** Todos los módulos del sistema para control de acceso
- **Tecnología:** Framework de autenticación y autorización (.NET Identity)
- **Seguridad:** Certificados SSL/TLS para conexiones seguras
