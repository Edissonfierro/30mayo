
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


## 8. Procedimiento

1 Clonar el repositorio 
 ![Texto alternativo](https://github.com/Edissonfierro/30mayo/blob/main/uno.jpg)

1 Crear los archivos -env docker compose, docker file y application yml 
 ![Texto alternativo](https://github.com/Edissonfierro/30mayo/blob/main/dos.jpg)
Para automatizar el despliegue del backend con Docker y Docker Compose, se crearon cuatro archivos principales. El archivo .env se utilizó para guardar de forma segura las variables de entorno, como el usuario, contraseña y nombre de la base de datos, permitiendo separar esta información del resto de la configuración. Luego, se construyó el archivo docker-compose.yml, que fue el encargado de levantar tres servicios: PostgreSQL como base de datos, pgAdmin como interfaz gráfica para administrarla, y la aplicación backend en Java. Además, este archivo crea volúmenes y redes para asegurar la persistencia de datos y la comunicación entre contenedores.

Se diseñó también un Dockerfile con configuración multi-stage, lo cual permitió compilar el proyecto y generar una imagen más optimizada y ligera, separando la fase de construcción de la de ejecución. Finalmente, se creó el archivo application.yml dentro de src/main/resources, que permite que la aplicación Spring Boot se conecte a la base de datos utilizando las variables del entorno. Con estos pasos, se logró levantar un entorno completo, automatizado y funcional desde cero.


## 9. Resultados esperados
Acceso a pgAdmin desde: http://localhost:8081

 ![Texto alternativo](https://github.com/Edissonfierro/30mayo/blob/main/pgadmin.jpg)
Backend funcionando desde: http://localhost:8080

 ![Texto alternativo](https://github.com/Edissonfierro/30mayo/blob/main/controller.jpg)
 ![Texto alternativo](https://github.com/Edissonfierro/30mayo/blob/main/consultaendpoint.jpg)
Conexión activa entre backend y PostgreSQL.

Contenedores en estado "Up".
 ![Texto alternativo](https://github.com/Edissonfierro/30mayo/blob/main/contenedores.jpg)
Migraciones exitosas desde Flyway.

## 10 Bibliografía

Docker. (s.f.). Docker documentation. https://docs.docker.com/

PostgreSQL Global Development Group. (s.f.). PostgreSQL documentation. https://www.postgresql.org/docs/

pgAdmin Team. (s.f.). pgAdmin documentation. https://www.pgadmin.org/docs/

Spring.io. (s.f.). Spring Boot Reference Documentation. https://docs.spring.io/spring-boot/docs/current/reference/html/

Baeldung. (2021). Guide to Dockerizing Spring Boot Applications. https://www.baeldung.com/dockerizing-spring-boot-application

Red Hat. (s.f.). ¿Qué es Docker?. https://www.redhat.com/es/topics/containers/what-is-docker



