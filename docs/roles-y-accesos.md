# Definición de Roles y Niveles de Acceso

## Roles de Usuario

### Administrador
- Acceso completo a todos los módulos
- Gestión de usuarios y permisos
- Configuración del sistema
- Reportes y análisis
- Acceso a datos financieros

### Gerente
- Gestión de tours y reservas
- Ver reportes y métricas
- Gestión de usuarios (solo lectura)
- Configuración de precios y promociones

### Agente de Ventas
- Crear y gestionar reservas
- Ver disponibilidad de tours
- Acceso a información de clientes
- Registro de ventas

### Cliente
- Ver y reservar tours
- Gestionar perfil propio
- Ver historial de reservas
- Realizar pagos

## Permisos por Recurso

| Recurso | Admin | Gerente | Agente | Cliente |
|---------|-------|---------|--------|---------|
| Tours - Ver | ✓ | ✓ | ✓ | ✓ |
| Tours - Crear | ✓ | ✓ | ✓ | ✗ |
| Tours - Editar | ✓ | ✓ | ✗ | ✗ |
| Tours - Eliminar | ✓ | ✗ | ✗ | ✗ |
| Reservas - Ver todas | ✓ | ✓ | Propias | Propias |
| Reservas - Crear | ✓ | ✓ | ✓ | ✓ |
| Reservas - Cancelar | ✓ | ✓ | ✓ | Propias |
| Usuarios - Gestionar | ✓ | ✗ | ✗ | ✗ |
| Pagos - Ver | ✓ | ✓ | ✗ | Propios |
| Reportes - Acceso | ✓ | ✓ | ✗ | ✗ |

## Autenticación y Autorización

- JWT tokens con expiración de 24 horas
- Refresh tokens para sesión persistente
- MFA opcional para administradores
- Logging de todas las acciones敏感
