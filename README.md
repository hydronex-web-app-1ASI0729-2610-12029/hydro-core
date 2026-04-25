<div align ="center">

![Logo Banner](assets/Banner-UPC.png)

### Universidad Peruana de Ciencias Aplicadas
### Inegeneria de Software
### 2026-1

### NRC: 12029
### Docente: Hugo Allan Mori Paiva
### Informe de Trabajo Final

###  HydroTeam
###  TankIQ



<div align = "center">
   
|**Code**|**Member**|
|---------------------|--------------------|
|U202310436 |Espinar Martínez Gabriel Ferran|
|U202410772 |Razuri Alvarez Matias Francesco| 
|U202411282 |Montalvan Palomino Bruno Rodolfo| 
|U202414840 |Oroscco Ttamiña Juan Carlos| 
|U202318951 |Guevara Serrano Diego Ismael| 

</div>

### Abril 2026

<div style="page-break-after: always;"></div>

<div align = "left">

# **Registro de Versiones del Informe**

| Versión | Fecha | Autor | Descripción de modificación |
|-----------|-----------|-----------|-----------|
|-----------|-----------|-----------|-----------|
|-----------|-----------|-----------|-----------|


# **Project Report Collaboration Insights**

**URL del Repositorio**: [https://github.com/hydronex-web-app-1ASI0729-2610-12029/hydro-core](https://github.com/hydronex-web-app-1ASI0729-2610-12029/hydro-core)

<div align = "left">

# ABET – EAC - Student Outcome 5

**Criterio:** La capacidad de funcionar efectivamente en un equipo cuyos miembros juntos proporcionan liderazgo, crean un entorno de colaboración e inclusivo, establecen objetivos, planifican tareas y cumplen objetivos.

En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro del ABET – EAC – Student Outcome 5.

| Criterio específico | Acciones realizadas | Conclusiones |
| :--- | :--- | :--- |
| **Trabaja en equipo para proporcionar liderazgo en forma conjunta** | | |
| **Crea un entorno colaborativo e inclusivo, establece metas, planifica tareas y cumple objetivos.** | | |



## Contenido

- [Capítulo V: Product Implementation, Validation \& Deployment](#capítulo-v-product-implementation-validation--deployment)
    - [5.1. Software Configuration Management](#51-software-configuration-management)
    - [5.1.1. Software Development Environment Configuration](#511-software-development-environment-configuration)
    - [5.1.2. Source Code Management](#512-source-code-management)
    - [5.1.3. Source Code Style Guide \& Conventions](#513-source-code-style-guide--conventions)
    - [5.1.4. Software Deployment Configuration](#514-software-deployment-configuration)
    - [5.2. Landing Page, Service \& Applications Implementation](#52-landing-page-service--applications-implementation)
    - [5.2.1. Sprint](#52x-sprint)
    -  [5.2.1.1. Sprint Planning 1](#5211-Sprint-Planning1)
    -  [5.2.1.2. Aspect Leaders and Collaborators](#5212-Aspect-Leaders-and-Collaborators)
    -  [5.2.1.3. Sprint Backlog 1](#5213-Sprint-Backlog-1)
    -  [5.2.1.4. Development Evidence for Sprint Review](#5214-Development-Evidence-for-Sprint-Review)
    -  [5.2.1.5. Execution Evidence for Sprint Review](#5215-Execution-Evidence-for-Sprint-Review)
    -  [5.2.1.6. Services Documentation Evidence for Sprint Review](#5216-Services-Documentation-Evidence-for-Sprint-Review)
    -  [5.2.1.7. Software Deployment Evidence for Sprint Review](#5217-Software-Deployment-Evidence-for-Sprint-Review)
    -  [5.2.1.8. Team Collaboration Insights during Sprint](#5218-Team-Collaboration-Insights-during-Sprint)
    -  [Conclusiones](#Conclusiones)
    -  [Bibliografía](#Bibliografía)
    -  [Anexos](#Anexos)



# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

### 5.1.1. Software Development Environment Configuration.

En esta sección se describen todas las herramientas utilizadas por el equipo HydroTeam para el desarrollo, diseño, documentación y despliegue de la solución TankIQ, incluyendo la categoría a la que pertenece cada una, su propósito dentro del proyecto y el enlace de acceso o descarga.

| Producto | Propósito en el proyecto | Categoría | Ruta de descarga / acceso | Descripción |
|---|---|---|---|---|
| **IntelliJ IDEA Ultimate** | IDE principal para el desarrollo del backend en Spring Boot (Java). Ofrece soporte nativo para JPA, Spring y herramientas de depuración integradas. | Software Development | https://www.jetbrains.com/idea/ | IDE de JetBrains especializado en Java y Kotlin, con integración nativa para Spring Boot, JPA y herramientas de refactorización avanzada. |
| **Visual Studio Code** | Editor de código utilizado para el desarrollo del frontend en Angular (TypeScript). Integra extensiones de Angular Language Service, ESLint y Prettier. | Software Development | https://code.visualstudio.com/ | Editor de código ligero y extensible de Microsoft, ampliamente usado para desarrollo web con soporte para TypeScript, Angular y control de versiones integrado. |
| **Angular CLI** | Framework frontend principal del proyecto. Permite generar componentes, servicios y módulos con estructura modular y tipado estático mediante TypeScript. | Software Development | https://angular.io/cli | Herramienta de línea de comandos oficial de Angular para crear, generar y gestionar proyectos Angular con buenas prácticas incorporadas. |
| **Spring Boot** | Framework backend basado en Java que implementa la API REST de TankIQ. Gestiona los seis Bounded Contexts del dominio mediante JPA/Hibernate y MySQL. | Software Development | https://spring.io/projects/spring-boot | Framework de Java que simplifica la creación de aplicaciones backend production-ready con configuración mínima y soporte para REST, JPA y seguridad. |
| **MySQL Workbench** | Herramienta visual para diseñar, gestionar y consultar la base de datos relacional del sistema. Permite ejecutar scripts SQL y administrar el esquema de TankIQ. | Software Development | https://dev.mysql.com/downloads/workbench/ | Aplicación visual para diseñar esquemas, ejecutar consultas SQL, gestionar usuarios y administrar servidores MySQL de manera integrada. |
| **Figma** | Plataforma de diseño colaborativo utilizada para crear wireframes, mockups y el prototipo interactivo de la Web Application y la Landing Page de TankIQ. | Product UX/UI Design | https://www.figma.com/ | Herramienta de diseño vectorial basada en la nube que permite la colaboración en tiempo real para prototipos, wireframes y sistemas de diseño. |
| **Structurizr** | Utilizado para modelar la arquitectura de software de TankIQ bajo el C4 Model (Context, Container, Component), generando diagramas a partir de código DSL. | Product UX/UI Design | https://structurizr.com/ | Aplicación especializada en la creación de modelos de arquitectura de software con base en el modelo C4, ideal para documentar y comunicar sistemas complejos. |
| **Lucidchart** | Utilizado para elaborar diagramas de clases, EventStorming y diagramas de flujo de usuario durante las etapas de análisis y diseño del sistema. | Product UX/UI Design | https://www.lucidchart.com/ | Herramienta de diagramación en línea que permite crear diagramas UML, flujos de procesos y arquitecturas de sistemas de forma colaborativa. |
| **Swagger UI / OpenAPI** | Herramienta para documentar y probar los endpoints de la API REST de TankIQ de forma interactiva. Se integra con Spring Boot mediante SpringDoc. | API Documentation | https://swagger.io/tools/swagger-ui/ | Interfaz que genera documentación dinámica de APIs REST, permitiendo visualizar rutas, parámetros y probar los endpoints directamente desde el navegador. |
| **Git CLI** | Sistema de control de versiones distribuido utilizado localmente por todos los integrantes para gestionar ramas, commits y sincronización con el repositorio remoto. | Version Control | https://git-scm.com/ | Sistema de control de versiones distribuido que permite gestionar cambios, trabajar con ramas y sincronizar código con repositorios remotos como GitHub. |
| **GitHub** | Plataforma remota de hospedaje de repositorios. Centraliza el código fuente de TankIQ y gestiona Pull Requests, Issues y flujos de revisión de código. | Collaboration & Version Control | https://github.com/ | Plataforma de desarrollo colaborativo para alojar, revisar y gestionar proyectos de software con integración a herramientas de CI/CD. |
| **Vercel** | Plataforma de despliegue utilizada para publicar la Landing Page estática de TankIQ con integración directa al repositorio de GitHub y HTTPS automático. | Deployment | https://vercel.com/ | Plataforma de despliegue en la nube optimizada para frontends estáticos y aplicaciones web, con despliegue automático desde GitHub. |
| **Railway** | Plataforma de despliegue en la nube utilizada para publicar el backend Spring Boot y la base de datos MySQL de TankIQ en entorno de producción. | Deployment | https://railway.app/ | Plataforma PaaS que permite desplegar aplicaciones backend y bases de datos con configuración simplificada y variables de entorno gestionadas desde el dashboard. |
| **UXPressia** | Utilizada para elaborar User Personas, User Journey Maps y Empathy Maps durante el proceso de Needfinding del proyecto. | Product UX/UI Design | https://uxpressia.com/ | Plataforma orientada a la elaboración de journey maps y perfiles de usuario que permite representar y analizar visualmente la experiencia dentro del sistema. |
| **Trello** | Herramienta de gestión ágil utilizada para organizar el Product Backlog y el Sprint Backlog del equipo, con columnas por estado de avance de las tareas. | Project Management | https://trello.com/ | Herramienta de tableros Kanban que facilita la organización visual de tareas, el seguimiento del progreso y la colaboración del equipo en sprints ágiles. |

    
### 5.1.2. Source Code Management.
    
### 5.1.3. Source Code Style Guide & Conventions.
    
### 5.1.4. Software Deployment Configuration.
    
## 5.2. Landing Page, Services & Applications Implementation.
    
## 5.2.1. Sprint n
    
### 5.2.1.1. Sprint Planning n.
    
### 5.2.1.2. Aspect Leaders and Collaborators.
    
### 5.2.1.3. Sprint Backlog n.
    
### 5.2.1.4. Development Evidence for Sprint Review.
    
### 5.2.1.5. Execution Evidence for Sprint Review.
    
### 5.2.1.6. Services Documentation Evidence for Sprint Review.
    
### 5.2.1.7. Software Deployment Evidence for Sprint Review.
    
### 5.2.1.8. Team Collaboration Insights during Sprint.

## Conclusiones

## Bibliografía

## Anexos
