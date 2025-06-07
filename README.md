# contenedor-frontend
TAS8 - Contenerización de aplicación Frontend con React y comunicación con API REST
## 1. Título
Contenerización de una Aplicación Frontend con React y Backend con API REST utilizando Docker

## 2. Tiempo de duración
El tiempo estimado para completar el despliegue fue de 200 minutos.

## 3. Fundamentos
Dockerfile
Un Dockerfile define los pasos para construir una imagen Docker. Este archivo contiene una serie de instrucciones que permiten transformar una imagen base en una imagen personalizada para la aplicación frontend con React y el backend con API REST.

La construcción de una imagen se realiza con docker build, agregando capas progresivamente. Para optimizar este proceso, se utiliza multi-stage build, lo que permite generar imágenes más ligeras y seguras.

Multi-stage Build
Las compilaciones multietapa permiten separar el entorno de desarrollo del entorno de ejecución final, reduciendo el tamaño de la imagen y minimizando vulnerabilidades.

En este método:

Se descargan dependencias y se compila el código en una primera etapa.

Luego, se copia la aplicación final en una imagen más ligera sin dependencias innecesarias.

Este enfoque es ideal para aplicaciones frontend en React y backend en Node.js, reduciendo el consumo de recursos.

## 4. Conocimientos previos
Para realizar el despliegue, es necesario conocer:

Fundamentos de React para el desarrollo frontend.

Fundamentos de API REST con Node.js y Express.

Comandos básicos de Docker.

Escritura y lectura de archivos Dockerfile.

Uso de .env para definir variables de configuración.

Fundamentos de bases de datos relacionales y PostgreSQL.

## 5. Objetivos a alcanzar
Contenerizar la aplicación frontend con React mediante Docker.

Contenerizar la API REST con Node.js y Express utilizando Docker.

Implementar multi-stage build para optimizar las imágenes de ambos contenedores.

Configurar servicios de base de datos y administración con Docker Compose.

Gestionar variables de entorno con un archivo .env.

Verificar la conectividad entre el frontend y la API REST.

Validar la comunicación entre la API REST y PostgreSQL.

## 6. Equipo necesario
Computador con Docker instalado.

Navegador web para acceder al frontend en React.

Conexión a internet para obtener imágenes y documentación.

## 7. Material de apoyo
Documentación oficial de Docker.

Guía de Docker Cheatsheet.

Repositorio del proyecto backend y frontend.

Videos tutoriales para referencia.

## 8. Procedimiento
Pasos
Clonar el repositorio del proyecto backend y frontend.

Crear archivo .env con las variables necesarias para ambos proyectos.

Configurar la base de datos PostgreSQL y pgAdmin.

Definir el archivo Dockerfile para el backend utilizando multi-stage build.

Definir el archivo Dockerfile para el frontend utilizando multi-stage build.

Construir y ejecutar los contenedores del backend y frontend con Docker.

Verificar si la construcción de las imágenes y los contenedores es correcta.

Validar la conexión entre el backend y la base de datos.

Crear el endpoint API REST en el backend para la entidad específica.

Configurar el frontend para consumir los datos del endpoint API REST.

Ejecutar sudo docker ps para comprobar los contenedores en ejecución.

Implementar Docker Compose para los contenedores del backend, frontend y base de datos.

Verificar el acceso al frontend en localhost y la correcta visualización de los datos.

## 9. Resultados esperados
La aplicación frontend ha sido contenerizada con éxito usando Dockerfile y multi-stage build.

La API REST del backend ha sido contenerizada con éxito.

Se generaron imágenes ligeras y optimizadas para el frontend y backend.

Se ejecutó Docker Compose para levantar los servicios frontend, backend, PostgreSQL y pgAdmin.

Se verificó la correcta comunicación entre la aplicación frontend y la API REST del backend.

Capturas de pantalla evidencian el proceso desde la clonación hasta el despliegue exitoso.

## 10. Bibliografía
Multi-stage | Docker Docs

Docker para React: cómo contenerizar tu frontend

Construcción multietapa Docker - Josef Jebavý's blog

¿Qué es el Dockerfile? - IONOS

Docker Compose para proyectos full-stack: backend y frontend
