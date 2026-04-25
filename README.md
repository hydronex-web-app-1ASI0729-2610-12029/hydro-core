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

El proyecto TankIQ se desarrolla bajo un enfoque profesional que prioriza las buenas prácticas
de control de versiones, la colaboración estructurada en equipo y la trazabilidad del código
fuente a lo largo de cada sprint. La gestión del código se realiza mediante **GitHub**, dentro
de la organización
[hydronex-web-app-1ASI0729-2610-12029](https://github.com/hydronex-web-app-1ASI0729-2610-12029),
donde se alojan los repositorios correspondientes a cada artefacto del sistema: el backend
desarrollado en Spring Boot, la Web Application en Angular y la Landing Page estática.

Para la gestión de ramas, el equipo adoptó **Git Flow** como modelo de ramificación. La rama
**`main`** contiene únicamente el código estable desplegado en producción y solo recibe merges
al cierre de cada sprint tras revisión grupal. La rama **`develop`** funciona como rama de
integración continua, donde todos los integrantes consolidan sus avances mediante Pull Requests
antes de pasar a producción. Las ramas **`feature/<nombre>`** se crean desde `develop` para el
desarrollo de cada funcionalidad de forma aislada y se integran mediante Pull Request con revisión
mínima de un compañero, como `feature/tank-monitoring`, `feature/alert-system` o
`feature/jwt-auth`. Las ramas **`fix/<nombre>`** se utilizan para la corrección de errores,
como `fix/estimated-days-formula`, y las ramas **`release/<versión>`** se crean al cierre de
cada sprint para preparar la entrega antes del merge a `main`.

Para la redacción de los mensajes de commit, el equipo siguió la convención
**Conventional Commits**, lo que permitió mantener un historial claro y semánticamente
significativo. Los prefijos utilizados fueron: `feat:` para nuevas funcionalidades, `fix:`
para corrección de errores, `chore:` para tareas de mantenimiento, `docs:` para documentación,
`refactor:` para reestructuración de código y `test:` para adición de pruebas. Ejemplos de
commits del proyecto incluyen: `feat: add cistern water level monitoring endpoint`,
`feat: implement JWT authentication for admin users` y
`fix: correct estimated days calculation formula`.
![repo.png](assets/repo.png)

### 5.1.3. Source Code Style Guide & Conventions.

El uso de un estilo de código unificado es clave para asegurar la consistencia, legibilidad y
colaboración efectiva durante el desarrollo de TankIQ. Para la entrega del Sprint 1, el trabajo
se centró en la implementación de la Landing Page estática, por lo que las convenciones
establecidas en esta sección corresponden a las tecnologías utilizadas: HTML, CSS y JavaScript.

**HTML**

La estructura del HTML sigue las convenciones del Google HTML/CSS Style Guide. Se utiliza
sangría de 2 espacios, todos los atributos se escriben en minúsculas y entre comillas dobles,
y todos los elementos de imagen incluyen el atributo `alt` para garantizar accesibilidad. Los
identificadores y clases se nombran en inglés y de forma descriptiva, reflejando el propósito
del elemento. Se utilizan atributos personalizados `data-lang` para gestionar el sistema de
internacionalización y `data-placeholder-es` para los inputs con soporte bilingüe.

**CSS**

Las clases CSS se nombran siguiendo la convención kebab-case (`.hero-section`, `.plan-card`,
`.navbar-fixed`, `.problema-card`), en concordancia con las recomendaciones del Google
HTML/CSS Style Guide. El diseño sigue un enfoque **Mobile First**, definiendo primero los
estilos base para dispositivos móviles y luego aplicando media queries para pantallas más
grandes. La paleta de colores, tipografía y espaciado respetan el Design System definido en
el Capítulo IV: color principal celeste `#29ABE2`, gris oscuro `#2D2D2D`, tipografía Inter
y espaciado en múltiplos de 8px. Las animaciones de entrada se gestionan mediante las clases
`.fade-in` y `.visible`, controladas por JavaScript al detectar visibilidad en el viewport.

**JavaScript**

El código JavaScript sigue las convenciones del Google JavaScript Style Guide y se organiza
en módulos funcionales claramente delimitados mediante comentarios de sección. Las funciones
se nombran en camelCase con nombres descriptivos que reflejan su responsabilidad:
`initLanguageSystem()`, `initMobileMenu()`, `initScrollAnimations()`, `initContactForm()`.
Se utiliza `const` y `let` en lugar de `var`, y cada función tiene una única responsabilidad
definida. El sistema de idiomas gestiona inglés y español mediante la clase `lang-es` sobre
el `body`, persistiendo la preferencia del usuario en `localStorage`. Para optimizar el
rendimiento, los eventos de scroll utilizan una función `throttle()` que limita la frecuencia
de ejecución. El código se escribe en inglés para todos los identificadores y comentarios
técnicos, a excepción de los textos visibles al usuario que forman parte del sistema bilingüe.

### 5.1.4. Software Deployment Configuration.

Para el despliegue de la Landing Page de TankIQ, el equipo HydroTeam utilizó **GitHub Pages**
como plataforma de publicación, aprovechando su integración directa con el repositorio de
GitHub. Esta decisión permite que cada actualización consolidada en la rama `main` se refleje
de forma automática en el entorno público, sin necesidad de configuración adicional de
infraestructura.

El proceso de configuración seguido fue el siguiente: en primer lugar, se accedió a la
configuración del repositorio de la Landing Page desde GitHub. Posteriormente, en la sección
**Pages**, se seleccionó la rama `main` como fuente de despliegue y se indicó la carpeta raíz
(`/root`) como directorio de publicación. GitHub Pages procesó automáticamente los archivos
estáticos (`index.html`, `styles.css`, `script.js`) y habilitó HTTPS por defecto mediante
sus certificados propios.


El entorno de producción de la Landing Page de TankIQ está accesible públicamente en la
siguiente URL: https://hydronex-web-app-1asi0729-2610-12029.github.io/Landing-Page/

## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1. Sprint 1

Durante el Sprint 1, el equipo HydroTeam centró sus esfuerzos en establecer la presencia
inicial del producto TankIQ mediante la implementación de la Landing Page. El trabajo incluyó
la estructuración de las secciones principales, el diseño visual alineado con el Design System
definido en el Capítulo IV, la responsividad Mobile First y la integración de los
call-to-action diferenciados por segmento objetivo. A continuación se detallan la planificación
del Sprint, el backlog trabajado, las evidencias de desarrollo y los aspectos de colaboración
del equipo.

#### 5.2.1.1. Sprint Planning 1.

| **Sprint #** | Sprint 1 |
|---|---|
| **Sprint Planning Background** | |
| **Fecha** | 23/04/2026 |
| **Hora** | 20:00 pm (GMT-5) |
| **Ubicación** | Reunión virtual por Google Meet |
| **Preparado por** | HydroTeam |
| **Participantes (reunión de planificación)** | - Espinar Martínez, Gabriel Ferran <br> - Guevara Serrano, Diego Ismael <br> - Montalvan Palomino, Bruno Rodolfo <br> - Orosco Ttamiña, Juan Carlos <br> - Razuri Alvarez, Matias Francesco |
| **Sprint Goal & User Stories** | Nuestro enfoque está en entregar la Landing Page de TankIQ con diseño completo, responsivo y alineado con la identidad visual del producto. Creemos que esto establecerá la presencia pública del producto y comunicará la propuesta de valor a ambos segmentos objetivo. Esto se confirmará cuando los visitantes puedan navegar todas las secciones, identificar los beneficios por segmento y acceder al formulario de contacto desde cualquier dispositivo. |
| **Velocidad del Sprint 1** | 25 |
| **Suma de Story Points** | 25 |

#### 5.2.1.2. Aspect Leaders and Collaborators.

En este apartado se describen los aspectos funcionales trabajados durante el Sprint 1 del
proyecto TankIQ. Cada aspecto representa una sección clave de la Landing Page, desde la
estructura de navegación y el hero hasta el footer y la responsividad. Para cada aspecto se
designó un **Líder (L)**, responsable de la dirección técnica y la implementación principal,
y **Colaboradores (C)**, encargados de apoyar en el desarrollo, revisión e integración.

La **Matriz LACX** (Leadership and Collaboration Matrix) permite visualizar de manera clara
la distribución de responsabilidades del equipo durante el Sprint 1.

| Team Member | GitHub Username    | Navbar & Hero | Problema & Cómo funciona | Beneficios & Ahorro | Planes & Integrantes | Contacto & Footer | Responsividad |
|---|--------------------|---|---|---|---|---|---|
| Espinar Martínez, Gabriel Ferran | zzZero14           | C | C | C | L | C | C |
| Guevara Serrano, Diego Ismael | digetto            | L | C | C | C | C | C |
| Montalvan Palomino, Bruno Rodolfo | br1rodolfo         | C | L | C | C | C | C |
| Orosco Ttamiña, Juan Carlos | juancarlosorosco59 | C | C | C | C | L | C |
| Razuri Alvarez, Matias Francesco | u202410772         | C | C | L | C | C | L |

#### 5.2.1.2. Aspect Leaders and Collaborators.

En este apartado se describen los aspectos funcionales más relevantes trabajados durante el
Sprint 1 en el desarrollo de la Landing Page de TankIQ. Cada uno de ellos representa un
bloque significativo dentro del alcance funcional de la solución, abarcando la estructura de
navegación, las secciones de contenido, el sistema de contacto y la responsividad del diseño.

Para cada aspecto se asignó un responsable principal, denominado **Líder (L)**, encargado de
la dirección técnica y la implementación principal. De igual manera, se identificaron
**Colaboradores (C)**, miembros del equipo que participaron activamente en el desarrollo,
validación o soporte de cada aspecto.

La **Matriz LACX** (Leadership and Collaboration Matrix) ofrece una representación clara y
organizada de la distribución de responsabilidades, favoreciendo la trazabilidad y visibilidad
del trabajo colaborativo desarrollado a lo largo del Sprint.

| Team Member | GitHub Username | Navbar & Hero | Problema & Cómo funciona | Beneficios & Ahorro | Planes & Integrantes | Contacto & Footer | Responsividad |
|---|---|---|---|---|---|---|---|
| Espinar Martínez, Gabriel Ferran | zzZero14   | C | C | C | L | C | C |
| Guevara Serrano, Diego Ismael |  digetto    | L | C | C | C | C | C |
| Montalvan Palomino, Bruno Rodolfo | br1rodolfo  | C | L | C | C | C | C |
| Orosco Ttamiña, Juan Carlos | juancarlosorosco59| C | C | C | C | L | C |
| Razuri Alvarez, Matias Francesco | u202410772   | C | C | L | C | C | L |

#### 5.2.1.3. Sprint Backlog 1.

El Sprint Backlog 1 se orienta a implementar la Landing Page completa de TankIQ, garantizando
que comunique la propuesta de valor de forma clara y diferenciada para los segmentos de
administradores de edificios y propietarios/inquilinos. El objetivo es que la primera versión
publicada sea responsive, visualmente alineada con el Design System definido en el Capítulo IV
y funcional en todos los navegadores modernos.

![img.png](assets/img.png)

| **Sprint 1** | | | | | | | |
|---|---|---|---|---|---|---|---|
| **User Story** | | **Work-Item / Task** | | | | | |
| **User Story ID** | **Título** | **Task ID** | **Task Title** | **Description** | **Estimation (Hours)** | **Assigned To** | **Status** |
| US46 | Navegar por secciones del landing | T01 | Implementar navbar con navegación por anclas | Desarrollar la barra de navegación fija con enlaces a todas las secciones de la Landing Page y menú hamburguesa para mobile. | 3 | Guevara Serrano, Diego | Done |
| US47 | Visualizar propuesta de valor | T02 | Implementar sección Hero con CTAs | Diseñar e implementar el hero con titular principal, descripción, botones diferenciados por segmento y dashboard preview animado. | 4 | Guevara Serrano, Diego | Done |
| US48 | Identificar problemas del sistema | T03 | Implementar sección Problema | Desarrollar la sección con tres tarjetas que presentan los problemas principales del suministro de agua irregular en Lima. | 3 | Montalvan Palomino, Bruno | Done |
| US49 | Comprender funcionamiento | T04 | Implementar sección Cómo funciona | Crear la sección con tres pasos numerados (sensor → plataforma → alertas) con íconos y conectores visuales. | 3 | Montalvan Palomino, Bruno | Done |
| US50 | Visualizar beneficios | T05 | Implementar sección Beneficios y Ahorro | Desarrollar la sección con dos columnas diferenciadas por segmento y el bloque de métricas de ahorro estimado. | 4 | Razuri Alvarez, Matias | Done |
| US51 | Consultar planes | T06 | Implementar sección Planes | Diseñar las tarjetas de plan Básico y Premium con características, precios y botones de contratación. | 3 | Espinar Martínez, Gabriel | Done |
| US52 | Enviar contacto | T07 | Implementar formulario de contacto | Desarrollar el formulario con validación de campos, integración de toast notifications y soporte bilingüe. | 5 | Orosco Ttamiña, Juan Carlos | Done |
| US53 | Acceder a contacto desde botones | T08 | Implementar CTAs con scroll suave | Conectar todos los botones de la Landing Page al formulario de contacto mediante scroll suave con JavaScript. | 2 | Orosco Ttamiña, Juan Carlos | Done |

#### 5.2.1.4. Development Evidence for Sprint Review.

A continuación se presenta el registro de commits realizados en el repositorio de la Landing
Page de TankIQ durante el Sprint 1. Cada entrada incluye el identificador del commit, su
mensaje descriptivo y la fecha de consolidación, reflejando la evolución del proyecto desde
la estructura base hasta la versión publicada. Los commits siguen la convención Conventional
Commits y evidencian cómo la Landing Page fue construida sección por sección mediante un
flujo de trabajo basado en ramas por feature, Pull Requests y revisión entre compañeros.

| Repository | Branch | Commit Id | Commit Message | Committed on (Date) |
|---|---|---|---|---|
| hydronex-web-app.../Landing-Page | feature/navbar | f10e69c | feat: add navbar with logo, navigation links and language toggle | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/hero | c4faaf8 | feat: add hero section with dual CTA buttons for admin and resident | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | 5807bc3 | feat: add primary, secondary and size button styles | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | fdd7b62 | feat: add section headers and highlight styles | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | cf2c61c | feat: add footer layout, newsletter and social links styles | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | efffc37 | feat: implement bilingual language system with localStorage persistence | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | b8f70be | feat: add mobile hamburger menu toggle functionality | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/problema | 0e9e646 | feat: add problema section in index.html | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/problema | d2898de | feat: add problema css section to landing page | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/como-funciona | 2fd502b | feat: add Como Funciona section in index.html | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/como-funciona | 2a8d052 | feat: add como funciona css section to landing page | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/beneficios | 8591d3f | feat: update benefits section in landing page | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/beneficios | ac015b6 | feat: add beneficios section in styles.css | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/ahorro | 5c708db | feat: add "ahorro" section to landing page | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/ahorro | 7e0e8c9 | feat: add ahorro css section to landing page | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | f67cdc5 | feat: add NAVBAR section in styles.css | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | 9d1d091 | feat: add HERO section in styles.css | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/beneficios | bc2b4b7 | feat: add animaciones fade-in al hacer scroll section to script.js | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/beneficios | 35fbbb2 | feat: add efecto 3D en tarjetas section to script.js | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | feature/navbar | 53f921a | feat: add scroll suave, efecto navbar al hacer scroll, inicialización in script.js | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | 88dad8a | Merge pull request #1 from feature/equipo | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | 42cadec | Merge pull request #2 from feature/contacto | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | c1eb79a | Merge pull request #3 from feature/planes | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | 5c4102d | Merge pull request #4 from feature/footer | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | 62bd1df | Merge pull request #5 from feature/problema | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | a6ec12f | Merge pull request #6 from feature/como-funciona | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | e415003 | Merge pull request #7 from feature/ahorro | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | f1e3595 | Merge pull request #8 from feature/beneficios | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | 6305494 | Merge pull request #9 from feature/hero | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | develop | 2502c74 | Merge pull request #10 from feature/navbar | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | main | fea1002 | fix: add missing sections | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | main | 062f041 | fix: logo path | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | main | dfdf8e2 | fix: repeated section | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | main | f1c4264 | docs: add new logo | Apr 25, 2026 |
| hydronex-web-app.../Landing-Page | main | 2a1e28f | update | Apr 25, 2026 |.

#### 5.2.1.5. Execution Evidence for Sprint Review.

Durante el Sprint 1, el equipo HydroTeam implementó la Landing Page completa de TankIQ.
El desarrollo priorizó la experiencia visual, la responsividad Mobile First y la coherencia
con el Design System definido en el Capítulo IV. Se implementó además un sistema de
internacionalización (i18n) que permite alternar entre inglés y español, persistiendo la
preferencia del usuario en localStorage.

![navhero.png](assets/navhero.png)

![problems.png](assets/problems.png)
![problems2.png](assets/problems2.png)
![planes.png](assets/planes.png)
![about.png](assets/about.png)
![contact&footer.png](assets/contact%26footer.png)
### 5.2.1.6. Services Documentation Evidence for Sprint Review.
    
### 5.2.1.7. Software Deployment Evidence for Sprint Review.
    
### 5.2.1.8. Team Collaboration Insights during Sprint.

## Conclusiones

## Bibliografía

## Anexos
