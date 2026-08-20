# Aplication the monitoring with Nodejs

Repositorio aplicación de monitoreo y logging en tiempo real desarrollada con Node.js, TypeScript y Express.js, basada en Clean Architecture. Permite supervisar la disponibilidad de servicios web mediante tareas CRON, registrar y almacenar logs en MongoDB y PostgreSQL usando Prisma ORM, clasificar eventos por niveles de severidad (Low, Medium y Error) y enviar reportes automáticos por correo electrónico con archivos adjuntos a múltiples destinatarios. Incluye pruebas automatizadas con Jest para garantizar la calidad y confiabilidad del sistema.

## 🎯 Características Principales

- **Monitoreo de Servicios**: Verifica periódicamente la disponibilidad de URLs/servicios web
- **Sistema de Logging Multicapa**: Almacena logs en múltiples bases de datos simultáneamente:
  - Sistema de archivos (logs locales)
  - MongoDB (base de datos NoSQL)
  - PostgreSQL (base de datos relacional)
- **Notificaciones por Email**: Envía reportes automáticos con logs adjuntos a múltiples destinatarios
- **Tareas Programadas**: Ejecuta verificaciones de servicios en intervalos configurables usando CRON
- **Clasificación de Logs**: Organiza eventos por niveles de severidad

## 🛠️ Tecnologías Utilizadas

### Backend
- **Node.js** - Runtime de JavaScript
- **TypeScript** - Lenguaje tipado para mayor robustez
- **Express.js** - Framework web (implícito en la estructura)

### Bases de Datos
- **MongoDB** - Base de datos NoSQL para almacenamiento flexible de logs
- **PostgreSQL** - Base de datos relacional para logs estructurados
- **Prisma** - ORM para interacción con PostgreSQL

### Servicios y Utilidades
- **Nodemailer** - Envío de correos electrónicos
- **Cron** - Programación de tareas automatizadas
- **Jest** - Framework de testing unitario

### Infraestructura
- **HTML, CSS, JavaScript** - Interfaz web (componentes frontend)

## 🏗️ Arquitectura

La aplicación sigue un patrón de arquitectura limpia con separación clara de responsabilidades:

- **Domain**: Lógica de negocio (casos de uso, entidades)
- **Infrastructure**: Implementación de datasources y repositorios
- **Presentation**: Capa de presentación (servidor, servicios de email y CRON)
- **Config**: Configuración de variables de entorno

## 💡 Casos de Uso Principales

1. Verificar disponibilidad de servicios en intervalos regulares
2. Persistir logs en múltiples bases de datos
3. Generar y enviar reportes por correo con logs adjuntos
4. Ejecutar trabajos programados de forma automática

---


# dev
1. Duplicar el archivo .env.template y renombrar a .env
2. Configurar las Variables de entorno en .env
3. Insatalar las dependencias con el comando
    ```
    npm install

    ```
4. Levantar las bases de datos con el comando
    ```
    docker compose up -d

    ```
5. Ejecutar el comando para crear las migraciones i egeneral Prisma Client
    ````
    npx prisma migrate dev

    ```
6. Levantar el servidor con el comando 
    ```
    npm run dev
    
    ```
7. Ejecutar las pruebas 

    ````
        npm run test:watch

    ````

## Obtener Gmail Key
[Google AppPasswords](https://myaccount.google.com/u/0/apppasswords)
