
# Automatizar el despliegue de una aplicación
##  1. Contenedores backend + base de datos 
### Despliegue automatizado de una aplicación backend Java + PostgreSQL + pgAdmin mediante Docker y Docker Compose. 
## 2. Tiempo de duración
### 3 horas

## 3. Fundamentos

### ¿Qué es Docker?
Docker es una plataforma que permite desarrollar, ejecutar y desplegar aplicaciones dentro de contenedores. Un contenedor es una unidad ligera, portátil y autosuficiente que incluye todo lo necesario para ejecutar una aplicación.

### ¿Qué es Docker Compose?
Es una herramienta que permite definir y ejecutar múltiples contenedores Docker mediante un solo archivo YAML (`docker-compose.yml`). Facilita el despliegue de aplicaciones con varios servicios interconectados.

### ¿Qué es PostgreSQL?
Es un sistema de gestión de bases de datos relacional de código abierto, muy usado por su estabilidad, extensibilidad y cumplimiento de estándares.

### ¿Qué es pgAdmin?
pgAdmin es una herramienta visual para administrar bases de datos PostgreSQL desde un navegador web. Permite ver tablas, ejecutar consultas SQL y administrar usuarios, todo de forma gráfica.

### ¿Qué es una imagen multi-stage?
Es una técnica para construir imágenes Docker optimizadas, utilizando múltiples etapas. Se usa una imagen pesada para compilar y otra más ligera para correr el resultado final. Así se reduce el tamaño de la imagen final y mejora el rendimiento.

## 4. Conocimientos Previos

- Manejo básico de terminal/Git Bash.
- Conocimientos de Docker y Docker Compose.
- Conceptos de backend y conexión a bases de datos.
- Uso básico de archivos `.env` y configuración de variables.

## 5. Objetivos a Alcanzar

- Clonar el proyecto desde GitHub.
- Crear la base de datos PostgreSQL y pgAdmin con sus volúmenes y red.
- Crear el contenedor del backend usando `Dockerfile` y **multi-stage build**.
- Levantar todos los servicios con Docker Compose.
- Verificar la conexión entre backend y PostgreSQL.
- Validar acceso a pgAdmin desde el navegador.


## 6. Equipo Necesario

- PC con Windows 10 o superior.
- Docker Desktop instalado y funcionando.
- Editor de texto (recomendado: Visual Studio Code).
- Navegador (Chrome, Firefox, etc.).


## 7. Material de Apoyo

- [Documentación oficial de Docker](https://docs.docker.com)
- [Documentación oficial de PostgreSQL](https://www.postgresql.org/docs/)
- [Documentación de pgAdmin](https://www.pgadmin.org/docs/)
- [Proyecto base en GitHub](https://github.com/maguaman2/tendencias-mar22-security)

---

## 8. Procedimiento



