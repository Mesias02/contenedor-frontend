# contenedor-frontend
TAS9 - Contenerización de aplicación Frontend con React y comunicación con API REST
---
![image](https://github.com/user-attachments/assets/769ead10-fd59-4c7a-b139-87473b8966c9)
---
## 1. Título
Contenerización de una Aplicación Frontend con React y Backend con API REST utilizando Docker
---
![image](https://github.com/user-attachments/assets/14996811-426f-4d12-acb0-d15b7e4ccd04)
---
## 2. Tiempo de duración
El tiempo estimado para completar el despliegue fue de 200 minutos.

## 3. Fundamentos
Dockerfile

El Dockerfile es un archivo que define los pasos necesarios para construir una imagen Docker. En este archivo se especifica cómo configurar el entorno del contenedor, incluyendo la instalación de dependencias, la compilación del código y la preparación de archivos para producción. Este mecanismo es utilizado tanto en el frontend desarrollado con React como en el backend basado en Node.js y Express. Cada instrucción en el Dockerfile representa una capa de la imagen, y todas se ejecutan de forma secuencial al invocar el comando docker build (Docker Docs, n.d.).

---
![image](https://github.com/user-attachments/assets/5c8d61a3-ab96-43c4-aa41-099b8414a0d9)
---
La construcción de una imagen se realiza con docker build, agregando capas progresivamente. Para optimizar este proceso, se utiliza multi-stage build, lo que permite generar imágenes más ligeras y seguras.

Multi-stage Build

La técnica de multi-stage build (compilaciones multietapa) es ampliamente recomendada para separar el proceso de construcción del de ejecución. Esto permite que solo los archivos necesarios lleguen a la imagen final, eliminando herramientas de desarrollo, archivos temporales o dependencias innecesarias, lo cual optimiza el tamaño y mejora la seguridad de los contenedores (IONOS, n.d.; Docker Docs, n.d.).

"Las compilaciones multietapa en Docker mejoran la eficiencia del proceso al eliminar dependencias innecesarias en la imagen final, garantizando un entorno más liviano y seguro" (Docker Docs, n.d.).

"Las compilaciones multietapa en Docker mejoran la eficiencia del proceso al eliminar dependencias innecesarias en la imagen final, garantizando un entorno más liviano y seguro." (Docker Docs, 2025)

En este método:

Se descargan dependencias y se compila el código en una primera etapa.

Luego, se copia la aplicación final en una imagen más ligera sin dependencias innecesarias.

Este enfoque reduce el consumo de recursos y mejora la seguridad del contenedor.

---
![image](https://github.com/user-attachments/assets/3b148c61-29ef-4267-9a6e-67f579872f72)
---
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

Repositorio del proyecto backend y frontend del proyecto de titulacion.

Videos tutoriales para referencia.

## 8. Procedimiento
Pasos
Definir el archivo Dockerfile para el backend etapa 1

---
![image](https://github.com/user-attachments/assets/066ba7ed-a9d5-4aa5-a95c-d7ce7b6c3650)
---
Definir el archivo Dockerfile para el frontend etapa 2

---
![image](https://github.com/user-attachments/assets/3449e4c0-0669-4e7a-be41-38e6da162572)
---
Verificar si la construcción de las imágenes y los contenedores es correcta.

---
![image](https://github.com/user-attachments/assets/0103f9f6-21d4-4f87-a0e3-4e52dc12351e)
---
Docker compose proyecto Futbol

----
![image](https://github.com/user-attachments/assets/4f2de168-af4f-4849-a4f2-0321037048a8)
----
Configurar el frontend para consumir los datos del endpoint API REST.

---
![image](https://github.com/user-attachments/assets/53361e9d-2fe6-453d-b72c-7afc7c0faf8a)
---
Ejecutar sudo docker ps para comprobar los contenedores en ejecución.

---
![image](https://github.com/user-attachments/assets/6d0220fc-f365-47aa-9882-4bf5a0bef380)
---
Implementar Docker Compose para los contenedores del backend, frontend y base de datos.

![image](https://github.com/user-attachments/assets/3abdcaad-92f1-4ac0-b658-a06cb85a42a6)
---
![image](https://github.com/user-attachments/assets/4edcf59f-0432-4109-a78f-46d454ebdb31)
---
Verificar el acceso al frontend en localhost y la correcta visualización de los datos.

---
![image](https://github.com/user-attachments/assets/0aeb802b-7b4c-4058-8bab-6b5914682a2d)
----
![image](https://github.com/user-attachments/assets/1b310437-12d9-49bf-b8ab-aa5dc52b16d7)
---

## 9. Resultados esperados
La aplicación frontend ha sido contenerizada con éxito usando Dockerfile y multi-stage build.

La API REST del backend ha sido contenerizada con éxito.

Se generaron imágenes ligeras y optimizadas para el frontend y backend.

Se ejecutó Docker Compose para levantar los servicios frontend, backend, PostgreSQL y pgAdmin.

Se verificó la correcta comunicación entre la aplicación frontend y la API REST del backend.

Capturas de pantalla evidencian el proceso desde la clonación hasta el despliegue exitoso.

## 10. Bibliografía
Multi-stage | Docker Docs

Docker Docs. (n.d.). Use multi-stage builds. Recuperado el 15 de junio de 2025, de https://docs.docker.com/develop/develop-images/multistage-build/

IONOS. (n.d.). ¿Qué es el Dockerfile y cómo funciona?. Recuperado el 15 de junio de 2025, de https://www.ionos.es/digitalguide/servidores/know-how/dockerfile/
Docker para React: cómo contenerizar tu frontend

Construcción multietapa Docker - Josef Jebavý's blog

¿Qué es el Dockerfile? - IONOS

Docker Compose para proyectos full-stack: backend y frontend
