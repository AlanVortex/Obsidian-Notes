## Control de Versiones

Potente sistema que registra los cambios realizados en archivos y carpetas a lo largo del tiempo. Permite al equipo de desarrollo contar con un registro de revisiones, restaurar a versiones específicas en el tiempo y colaborar de manera efectiva en un proyecto.

**Importancia en DevOps**
- Colaboración
- Seguimiento de cambios
- Gestión de conflictos
- Despliegue continuo

**Sistemas:** Git, Subversion, Mercurial, Perforce.

---
## Elementos de DevOps

### Virtualización

Proporciona una capa adicional de flexibilidad, escalabilidad y eficiencia en la gestión de recursos de hardware y entornos de desarrollo y producción.

- Abstracción de Recursos
- Ambientes Aislados
- Replicación de Entornos
- Escalabilidad y Despliegue Rápido
- Eficiencia de Recursos
- Snapshotting y Rollbacks
- Orquestación y Administración
- Portabilidad
- Pruebas de Carga y Rendimiento

---
### Contenedores

Los contenedores son elementos fundamentales en DevOps debido a su capacidad para simplificar la implementación, la gestión y la escalabilidad de aplicaciones y servicios.

- Aislamiento y Portabilidad
- Desarrollo y Pruebas Consistentes
- Integración Continua y Entrega Continua (CI/CD)
- Escalabilidad y Orquestación
- Rollbacks y Actualizaciones
- Gestión de Configuración y Versionamiento
- Seguridad
- Colaboración

---
### Infraestructura como código

Implica tratar la infraestructura de TI (servidores, redes, almacenamiento, etc.) de la misma manera que se trata el código fuente de una aplicación. Dejar de configurar manualmente servidores y recursos.

Se utilizan scripts o definiciones de configuración para automatizar la creación, configuración y gestión de la infraestructura.

- Automatización en aprovisionamiento
- Versionamiento de archivos de infraestructura
- Documentación Viva
- Reproducibilidad
- Pruebas Automatizadas
- Seguridad y Cumplimiento

---
## Docker

### Elementos

- **Contenedor:** Un contenedor es una instancia aislada de una aplicación y su entorno, que incluye el código de la aplicación, las bibliotecas y otras dependencias.
- **Imagen:** Una imagen Docker es un paquete estático que contiene todo lo necesario para ejecutar una aplicación, incluyendo el código, las dependencias y las configuraciones. Los contenedores se crean a partir de imágenes.
- **Orquestación:** Docker Swarm y Kubernetes son herramientas de orquestación que te permiten administrar y escalar contenedores en clústeres de servidores.
- **Dockerfile:** Un Dockerfile es un archivo de texto que define los pasos necesarios para construir una imagen Docker personalizada.

