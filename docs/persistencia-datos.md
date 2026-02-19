# Diseño de Persistencia y Criticidad de Datos

## Modelo de Datos por Servicio

### Servicio de Autenticación
- **Base de datos**: PostgreSQL
- **Tablas principales**: users, sessions, oauth_providers
- **Criticidad**: ALTA - Sin usuarios no funciona nada

### Servicio de Tours
- **Base de datos**: PostgreSQL
- **Tablas**: tours, itineraries, prices, availability
- **Criticidad**: ALTA - Core del negocio

### Servicio de Reservas
- **Base de datos**: PostgreSQL
- **Tablas**: bookings, booking_items, payments
- **Criticidad**: MUY ALTA - Transacciones financieras

### Servicio de Usuarios
- **Base de datos**: MongoDB
- **Colecciones**: profiles, preferences, favorites
- **Criticidad**: MEDIA - Datos de usuario

### Servicio de Notificaciones
- **Base de datos**: MongoDB
- **Colecciones**: notifications, templates
- **Criticidad**: BAJA - No es crítico

## Estrategias de Respaldo

### PostgreSQL
- Backups diarios completos
- Replicación en tiempo real
- Point-in-time recovery

### MongoDB
- Backups hourly
- Replica sets para alta disponibilidad

## Retención de Datos

- Transacciones: 7 años (requerimiento legal)
- Logs: 1 año
- Sesiones: 30 días
- Notificaciones: 90 días
