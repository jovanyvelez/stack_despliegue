
# Stack de Deployment Self-Hosted a Costo $0

## Resumen
Infraestructura completa de producción para aplicaciones web, aprovechando servicios gratuitos y herramientas open-source. Control total, seguridad robusta y cero costos operativos.

## Infraestructura Base

### Servidor
- **Proveedor**: Oracle Cloud Free Tier
- **Recursos**: 4 núcleos CPU, 24 GB RAM
- **SO**: Linux
- **Costo**: $0

### Protección y DNS
- **Cloudflare**: Gestión de DNS con protección DDoS
- **Beneficios**: Caché edge, SSL/TLS, protección de IP origen
- **Costo**: $0

## Stack Técnico

### Web Server
- **Caddy**: Servidor web y reverse proxy
- **Características**:
  - Certificados SSL automáticos
  - Configuración simple con Caddyfile
  - Servicio de archivos estáticos (imágenes)
- **Gestión**: Servicio systemd

### Base de Datos
- **PostgreSQL**: Self-hosted en el mismo VPS
- **Administración**: pgAdmin4 vía túnel SSH
- **Backups**: Crontab automatizado para:
  - Respaldos de base de datos
  - Código fuente
  - Archivos de configuración (systemd, Caddyfile, etc.)

### Deployment y Gestión

#### Actualización de Aplicaciones
- **SFTP**: Transferencia de archivos
- **SSH**: Acceso remoto para administración
- **Systemd**: Control de servicios (start/stop/restart)

#### Administración Segura
- **Túnel SSH**: Acceso seguro a pgAdmin4
- **Sin puertos expuestos**: Base de datos protegida

## Ventajas del Stack

### Económicas
- Costo total mensual: **$0**
- Evita servicios pagos como:
  - Supabase (backend as a service)
  - Cloudinary (gestión de imágenes)
  - Cloudflare R2 (almacenamiento de objetos)

### Técnicas
- **Control total**: Acceso completo a toda la infraestructura
- **Seguridad**: Múltiples capas de protección
- **Velocidad**: Recursos dedicados sin throttling
- **Flexibilidad**: Configuración personalizada según necesidades

### Operativas
- **Respaldos automatizados**: Sin intervención manual
- **Recuperación**: Backups de código, BD y configuraciones
- **Mantenimiento**: Scripts y servicios bien organizados
- **Escalabilidad**: Recursos generosos para crecimiento

## Casos de Uso Ideales
- Proyectos personales o MVPs
- Startups en etapa inicial
- Aplicaciones con tráfico moderado
- Desarrolladores que buscan control total
- Proyectos que priorizan privacidad y ownership de datos

## Consideraciones
Este stack requiere conocimientos de:
- Administración de sistemas Linux
- Configuración de servicios web
- Gestión de bases de datos
- Seguridad básica de servidores

**Trade-off**: Más control y costo $0 a cambio de responsabilidad directa sobre la infraestructura.