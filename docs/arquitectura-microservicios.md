# Justificación de Arquitectura de Microservicios

## Reasons for Choosing Microservices

### 1. Escalabilidad Independiente
- Cada servicio puede escalar horizontalmente según demanda
- Servicios de alta demanda (reservas) pueden escalarse más que otros
- Optimización de recursos por servicio

### 2. Despliegue Independiente
- Despliegues sin tiempo de inactividad
- Deployment continuo por servicio
- Rollback rápido si hay problemas

### 3. Tecnologías Diversas
- Cada servicio puede usar la tecnología óptima
- Flexibilidad para actualizar tecnologías por servicio
- No hay lock-in de tecnología

### 4. Fault Isolation
- Fallos en un servicio no afectan a otros
- Mejor manejo de errores y recuperación
- Mayor estabilidad general del sistema

### 5. Equipos Pequeños y Autónomos
- Equipos pueden trabajar en servicios independientes
- Faster time-to-market
- Mejor propiedad del código por equipo

## Desventajas y Mitigaciones

### Complejidad Operativa
- Solución: Kubernetes para orquestación
- Monitoreo centralizado con Prometheus/Grafana
- Logging centralizado con ELK Stack

### Distribución de Datos
- Solución: API Gateway para aggregates
- Bases de datos por servicio
- Eventos para consistencia eventual
