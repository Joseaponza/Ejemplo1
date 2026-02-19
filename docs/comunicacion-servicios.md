# Diseño de Comunicación entre Servicios y Flujo API

## Arquitectura de Comunicación

### Comunicación Síncrona (REST API)
- API Gateway como punto de entrada
- Endpoints REST para operaciones CRUD
- Autenticación via JWT en headers
- Rate limiting y throttling

### Comunicación Asíncrona (Message Queues)
- RabbitMQ o Apache Kafka para mensajería
- Eventos para actualizaciones entre servicios
- Patrón Pub/Sub para notificaciones
- Colas de mensajes para procesos largos

## API Gateway

### Rutas Principales
```
/api/auth/* - Autenticación
/api/tours/* - Gestión de tours
/api/bookings/* - Reservas
/api/users/* - Perfiles de usuarios
/api/payments/* - Pagos
/api/notifications/* - Notificaciones
```

### Seguridad
- JWT tokens para autenticación
- API keys para servicios externos
- HTTPS obligatorio
- Validación de requests

## Flujo de Datos

1. Cliente → API Gateway → Servicio específico
2. Servicio → Message Queue → Otros servicios
3. Respuesta síncrona o callback asíncrono
