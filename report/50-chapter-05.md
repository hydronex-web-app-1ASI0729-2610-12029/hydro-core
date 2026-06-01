# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

### 5.1.1. Software Development Environment Configuration.

En este punto detallaremos todas las herramientas de software usadas para el desarrollo
del proyecto TankIQ:

**Gestión del proyecto**

- **WhatsApp**: [LINK WhatsApp](https://www.whatsapp.com/)  
  Usamos WhatsApp como nuestro principal canal para comunicarnos, la coordinación de
  tareas, los tiempos de entrega, las nuevas ideas y brindar soporte a otros miembros
  que tengan dificultades.

- **Google Meet**: [LINK Google Meet](https://meet.google.com/)  
  Utilizado para las reuniones virtuales de planificación de sprints y coordinación
  general del equipo.

- **Jira**: [LINK Jira](https://hydroteam12.atlassian.net/jira/software/projects/SCRUM/boards/1)  
  Usamos Jira para seguir y evaluar el progreso y flujo de las actividades del proyecto
  entre todos los miembros durante todo el proceso del trabajo.

**Diseño UX/UI del Producto**

- **Figma**: [LINK Figma](https://www.figma.com/es-es/)  
  Plataforma para crear nuestros diseños, principalmente los wireframes, mockups y
  prototipo interactivo de la Landing Page.

- **UXPressia**: [LINK UXPressia](https://uxpressia.com/)  
  Se utilizó esta herramienta para la creación del Impact Mapping, Empathy Mapping y
  el User Journey Mapping.

**Software Development**



- **IntelliJ IDEA**: [LINK IntelliJ IDEA](https://www.jetbrains.com/idea/)  
  IDE principal para el desarrollo del backend en Spring Boot (Java).

- **HTML**: [Más información sobre HTML](https://developer.mozilla.org/es/docs/Web/HTML)  
  Lenguaje de marcado estándar utilizado para estructurar el contenido de la Landing
  Page, compatible con todos los navegadores modernos.

- **CSS**: [Más información sobre CSS](https://developer.mozilla.org/es/docs/Web/CSS)  
  Lenguaje de hojas de estilo que define la apariencia visual de la Landing Page,
  permitiendo controlar diseño, colores y tipografías.

- **JavaScript**: [Más información sobre JavaScript](https://developer.mozilla.org/es/docs/Web/JavaScript)  
  Lenguaje de programación que añade interactividad y lógica a la Landing Page,
  incluyendo el sistema de idiomas y las animaciones de scroll.

**Despliegue del software**

- **Git**: [LINK Git](https://git-scm.com/)  
  Sistema de control de versiones distribuido que permite gestionar cambios en el
  código, colaborar en equipo y mantener un historial completo del proyecto.

**Documentación del proyecto**

- **GitHub**: [LINK GitHub](https://github.com/)  
  Plataforma para alojar repositorios, colaborar y revisar contribuciones del equipo
  mediante Pull Requests y el flujo Git Flow.

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

<img src="assets/repo.png" alt="repo" style="width: 700px;"/></div>

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

### 5.2.1.1. Sprint Planning 1.

<table border="1" cellpadding="8" cellspacing="0" style="border-collapse: collapse; width: 100%; font-family: sans-serif; font-size: 14px;">
  <thead>
    <tr style="text-align: left;">
      <th style="width: 30%;">Sprint # / Campo</th>
      <th>Sprint 1 / Detalle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Sprint Planning Background</strong></td>
      <td></td>
    </tr>
    <tr>
      <td><strong>Fecha</strong></td>
      <td>23/04/2026</td>
    </tr>
    <tr>
      <td><strong>Hora</strong></td>
      <td>20:00 pm (GMT-5)</td>
    </tr>
    <tr>
      <td><strong>Ubicación</strong></td>
      <td>Reunión virtual por Google Meet</td>
    </tr>
    <tr>
      <td><strong>Preparado por</strong></td>
      <td>HydroTeam</td>
    </tr>
    <tr>
      <td><strong>Participantes</strong></td>
      <td>
        • Espinar Martínez, Gabriel Ferran<br>
        • Guevara Serrano, Diego Ismael<br>
        • Montalvan Palomino, Bruno Rodolfo<br>
        • Orosco Ttamiña, Juan Carlos<br>
        • Razuri Alvarez, Matias Francesco
      </td>
    </tr>
    <tr>
      <td><strong>Sprint Goal & User Stories</strong></td>
      <td style="text-align: justify;">
        Nuestro enfoque está en entregar la Landing Page de TankIQ con diseño completo, responsivo y alineado con la identidad visual del producto. Creemos que esto establecerá la presencia pública del producto y comunicará la propuesta de valor a ambos segmentos objetivo. Esto se confirmará cuando los visitantes puedan navegar todas las secciones, identificar los beneficios por segmento y acceder al formulario de contacto desde cualquier dispositivo.
      </td>
    </tr>
    <tr>
      <td><strong>Velocidad del Sprint 1</strong></td>
      <td>25</td>
    </tr>
    <tr>
      <td><strong>Suma de Story Points</strong></td>
      <td>25</td>
    </tr>
  </tbody>
</table>

### 5.2.1.2. Aspect Leaders and Collaborators.

En este apartado se describen los aspectos funcionales trabajados durante el Sprint 1 del
proyecto TankIQ. Cada aspecto representa una sección clave de la Landing Page, desde la
estructura de navegación y el hero hasta el footer y la responsividad. Para cada aspecto se
designó un **Líder (L)**, responsable de la dirección técnica y la implementación principal,
y **Colaboradores (C)**, encargados de apoyar en el desarrollo, revisión e integración.

La **Matriz LACX** (Leadership and Collaboration Matrix) permite visualizar de manera clara
la distribución de responsabilidades del equipo durante el Sprint 1.

| Team Member                       | GitHub Username    | Navbar & Hero | Problema & Cómo funciona | Beneficios & Ahorro | Planes & Integrantes | Contacto & Footer | Responsividad |
|-----------------------------------|--------------------|---------------|--------------------------|---------------------|----------------------|-------------------|---------------|
| Espinar Martínez, Gabriel Ferran  | zzZero14           | C             | C                        | C                   | L                    | C                 | C             |
| Guevara Serrano, Diego Ismael     | digetto            | L             | C                        | C                   | C                    | C                 | C             |
| Montalvan Palomino, Bruno Rodolfo | br1rodolfo         | C             | L                        | C                   | C                    | C                 | C             |
| Orosco Ttamiña, Juan Carlos       | juancarlosorosco59 | C             | C                        | C                   | C                    | L                 | C             |
| Razuri Alvarez, Matias Francesco  | u202410772         | C             | C                        | L                   | C                    | C                 | L             |

### 5.2.1.3. Sprint Backlog 1.

El Sprint Backlog 1 se orienta a implementar la Landing Page completa de TankIQ, garantizando
que comunique la propuesta de valor de forma clara y diferenciada para los segmentos de
administradores de edificios y propietarios/inquilinos. El objetivo es que la primera versión
publicada sea responsive, visualmente alineada con el Design System definido en el Capítulo IV
y funcional en todos los navegadores modernos.

<img src="assets/img.png" alt="image" style="width: 700px;">

<table style="width: 100%; border-collapse: collapse; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif; font-size: 13px; color: #333333; background-color: #ffffff; box-shadow: 0 4px 6px rgba(0,0,0,0.05); border-radius: 8px; overflow: hidden; margin: 20px 0;">
  <thead>
    <!-- Cabecera Principal del Sprint -->
    <tr style="background-color: #1e293b; color: #ffffff;">
      <th colspan="8" style="padding: 12px 16px; font-size: 14px; font-weight: bold; letter-spacing: 0.5px; border-bottom: 1px solid #334155;">
        SPRINT 1 - BACKLOG & TASKS
      </th>
    </tr>
    <!-- Cabecera de Columnas -->
    <tr style="background-color: #334155; color: #f8fafc; text-align: left;">
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; width: 60px; text-align: center;">US ID</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; width: 160px;">User Story Título</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; width: 60px; text-align: center; color: #38bdf8;">Task ID</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; color: #38bdf8; width: 180px;">Task Title</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase;">Description</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; width: 70px; text-align: center;">Estim.</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; width: 160px;">Assigned To</th>
      <th style="padding: 10px 14px; font-weight: 600; font-size: 11px; text-transform: uppercase; width: 75px; text-align: center;">Status</th>
    </tr>
  </thead>
  <tbody>
    <!-- US46 -->
    <tr style="border-bottom: 1px solid #e2e8f0;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US46</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Navegar por secciones del landing</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T01</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar navbar con navegación por anclas</td>
      <td style="padding: 12px 14px; color: #475569;">Desarrollar la barra de navegación fija con enlaces a todas las secciones de la Landing Page y menú hamburguesa para mobile.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">3h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Guevara Serrano, Diego</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US47 -->
    <tr style="border-bottom: 1px solid #e2e8f0; background-color: #fcfcfc;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US47</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Visualizar propuesta de valor</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T02</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar sección Hero con CTAs</td>
      <td style="padding: 12px 14px; color: #475569;">Diseñar e implementar el hero con titular principal, descripción, botones diferenciados por segmento y dashboard preview animado.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">4h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Guevara Serrano, Diego</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US48 -->
    <tr style="border-bottom: 1px solid #e2e8f0;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US48</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Identificar problemas del sistema</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T03</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar sección Problema</td>
      <td style="padding: 12px 14px; color: #475569;">Desarrollar la sección con tres tarjetas que presentan los problemas principales del suministro de agua irregular en Lima.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">3h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Montalvan Palomino, Bruno</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US49 -->
    <tr style="border-bottom: 1px solid #e2e8f0; background-color: #fcfcfc;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US49</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Comprender funcionamiento</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T04</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar sección Cómo funciona</td>
      <td style="padding: 12px 14px; color: #475569;">Crear la sección con tres pasos numerados (sensor → plataforma → alertas) con íconos y conectores visuales.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">3h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Montalvan Palomino, Bruno</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US50 -->
    <tr style="border-bottom: 1px solid #e2e8f0;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US50</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Visualizar beneficios</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T05</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar sección Beneficios y Ahorro</td>
      <td style="padding: 12px 14px; color: #475569;">Desarrollar la sección con dos columnas diferenciadas por segmento y el bloque de métricas de ahorro estimado.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">4h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Razuri Alvarez, Matias</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US51 -->
    <tr style="border-bottom: 1px solid #e2e8f0; background-color: #fcfcfc;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US51</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Consultar planes</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T06</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar sección Planes</td>
      <td style="padding: 12px 14px; color: #475569;">Diseñar las tarjetas de plan Básico y Premium con características, precios y botones de contratación.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">3h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Espinar Martínez, Gabriel</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US52 -->
    <tr style="border-bottom: 1px solid #e2e8f0;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US52</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Enviar contacto</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T07</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar formulario de contacto</td>
      <td style="padding: 12px 14px; color: #475569;">Desarrollar el formulario con validación de campos, integración de toast notifications y soporte bilingüe.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">5h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Orosco Ttamiña, Juan Carlos</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
    <!-- US53 -->
    <tr style="border-bottom: 1px solid #e2e8f0; background-color: #fcfcfc;">
      <td style="padding: 12px 14px; text-align: center; font-weight: bold; color: #475569; background-color: #f8fafc;">US53</td>
      <td style="padding: 12px 14px; font-weight: 500; color: #1e293b;">Acceder a contacto desde botones</td>
      <td style="padding: 12px 14px; text-align: center; font-family: monospace; font-weight: bold; color: #0284c7;">T08</td>
      <td style="padding: 12px 14px; font-weight: 600; color: #0f172a;">Implementar CTAs con scroll suave</td>
      <td style="padding: 12px 14px; color: #475569;">Conectar todos los botones de la Landing Page al formulario de contacto mediante scroll suave con JavaScript.</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #f1f5f9; color: #334155; padding: 3px 8px; border-radius: 12px; font-weight: 600;">2h</span></td>
      <td style="padding: 12px 14px; color: #334155;">Orosco Ttamiña, Juan Carlos</td>
      <td style="padding: 12px 14px; text-align: center;"><span style="background: #dcfce7; color: #15803d; padding: 4px 8px; border-radius: 4px; font-weight: bold; font-size: 11px;">DONE</span></td>
    </tr>
  </tbody>
</table>

### 5.2.1.4. Development Evidence for Sprint Review.

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

### 5.2.1.5. Execution Evidence for Sprint Review.

Durante el Sprint 1, el equipo HydroTeam implementó la Landing Page completa de TankIQ.
El desarrollo priorizó la experiencia visual, la responsividad Mobile First y la coherencia
con el Design System definido en el Capítulo IV. Se implementó además un sistema de
internacionalización (i18n) que permite alternar entre inglés y español, persistiendo la
preferencia del usuario en localStorage.

<img src="assets/navhero.png" alt="image" style="width: 700px">

<img src="assets/problems.png" alt="image" style="width: 700px">

<img src="assets/problems2.png" alt="image" style="width: 700px">

<img src="assets/planes.png" alt="image" style="width: 700px">

<img src="assets/about.png" alt="image" style="width: 700px">

<img src="assets/contact&footer.png" alt="image" style="width: 700px">

### 5.2.1.6. Services Documentation Evidence for Sprint Review.

El repositorio del Landing Page contiene una documentación exhaustiva que detalla la estructura del proyecto, las tecnologías empleadas, los requisitos de instalación y las directrices para el despliegue. En el archivo README.md del repositorio, se puede acceder a esta documentación.

<img src="assets/github.png" alt="image" style="width: 700px">

### 5.2.1.7. Software Deployment Evidence for Sprint Review.

En esta sección se presentan las evidencias del proceso de despliegue de la Landing Page
desarrollado durante el Sprint 1. El despliegue se realizó utilizando **GitHub Pages**, una
plataforma de hosting gratuita y confiable para sitios web estáticos, que permite la
publicación automática desde el repositorio de GitHub.

**Información del Despliegue**

| Aspecto | Detalle |
|---|---|
| Plataforma de Despliegue | GitHub Pages |
| Repositorio | [Landing-Page](https://github.com/hydronex-web-app-1ASI0729-2610-12029/Landing-Page) |
| URL del Landing Page | [https://hydronex-web-app-1ASI0729-2610-12029.github.io/Landing-Page/](https://hydronex-web-app-1ASI0729-2610-12029.github.io/Landing-Page/) |
| Rama de Despliegue | main |
| Fecha de Despliegue | 25/04/2026 |
| Estado Actual | Desplegado y Funcional |
| Tipo de Sitio | Sitio Web Estático (HTML, CSS, JavaScript) |
| HTTPS | Habilitado (Certificado SSL automático) |

**Proceso de Despliegue Detallado**

**Paso 1: Preparación del Repositorio**
- Se configuró el repositorio `Landing-Page` en GitHub con la estructura completa de archivos.
- Se organizaron los archivos HTML, CSS, JavaScript e imágenes en carpetas apropiadas.
- Se aseguró que todos los archivos estuvieran consolidados en la rama `main`.

**Paso 2: Configuración de GitHub Pages**
- Se accedió a la configuración del repositorio en GitHub.
- Se habilitó GitHub Pages en la sección **Settings → Pages**.
- Se seleccionó la rama `main` como fuente del sitio.
- Se configuró la carpeta raíz (`/root`) como directorio de publicación.

Configuración de GitHub Pages

<img src="assets/landing-page/github-pages.png" alt="image" style="width: 700px">

**Paso 3: Generación de la URL**
- GitHub Pages generó automáticamente la URL pública del sitio.
- La URL sigue el formato: `https://[organizacion].github.io/[repositorio]/`

**Paso 4: Verificación del Despliegue**
- Se verificó que el sitio estuviera accesible en la URL proporcionada.
- Se comprobó que el certificado SSL estuviera activo (HTTPS).
- Se validó que todos los recursos se cargaran correctamente.

Confirmación de despliegue exitoso

<img src="assets/landing-page/landing-page-deployment.png" alt="image" style="width: 700px">

**Paso 5: Validación de Funcionalidad**

Se realizaron pruebas para verificar que todas las funcionalidades del Landing Page
funcionaran correctamente:

- **Navegación entre secciones:** Todos los enlaces del menú funcionan con scroll suave.
- **Diseño responsive:** El sitio se adapta correctamente a mobile, tablet y desktop.
- **Sistema de idiomas:** El toggle EN/ES funciona correctamente y persiste en localStorage.
- **Formulario de contacto:** La validación de campos y los toast notifications operan sin errores.
- **Carga de assets:** Todas las imágenes y recursos se cargan sin errores.
- **Compatibilidad:** Se probó en Chrome, Firefox, Safari y Edge.

*(Insertar captura: Landing Page desplegada en producción)*

### 5.2.1.8. Team Collaboration Insights during Sprint.

Durante el Sprint 1, las actividades de implementación del Landing Page de TankIQ se
desarrollaron de forma colaborativa mediante **GitHub**, aplicando el flujo de trabajo
basado en ramas por feature, commits con la convención Conventional Commits y Pull
Requests con revisión mínima de un compañero antes del merge a `main`. Este proceso
garantizó trazabilidad, calidad de código y un historial claro de las contribuciones de
cada integrante.

Cada miembro del equipo asumió la responsabilidad de una o más secciones de la Landing
Page según la distribución establecida en la Matriz LACX, asegurando una participación
activa y balanceada. Las coordinaciones técnicas se realizaron mediante reuniones virtuales
por Google Meet y comunicación por WhatsApp.

A continuación se presentan las evidencias de colaboración del equipo durante el Sprint 1:

Network Graph del repositorio Landing-Page en GitHub

<img src="assets/git-hub/insights.png" alt="General insights" style="margin-bottom: 5px; width: 600px">

Contributors — commits por integrante

<img src="assets/git-hub/contributors.png" alt="Historial de commits por in" style="margin-bottom: 5px; width: 600px">


Historial de Pull Requests mergeados

<img src="assets/git-hub/insights-pulse.png" alt="Historial de insights" style="margin-bottom: 5px; width: 600px">

### 5.2.2. Sprint 2

Durante el Sprint 2, el equipo HydroTeam centró sus esfuerzos en el desarrollo de la primera
versión de la Web Application de TankIQ utilizando Angular como framework principal. En esta
etapa se trabajó en la configuración de la arquitectura base del proyecto, la implementación
de navegación mediante rutas, la organización modular utilizando bounded contexts y el
desarrollo de las primeras vistas funcionales del sistema. Asimismo, se realizaron mejoras
sobre los artefactos desarrollados durante el Sprint 1, corrigiendo aspectos visuales,
tipográficos y estructurales para mantener coherencia con el Design System definido
previamente.

### 5.2.2.1. Sprint Planning 2.

### 5.2.2.1. Sprint Planning 2.

| **Sprint #** | Sprint 2 |
|---|---|
| **Sprint Planning Background** | |
| **Date** | 2026-05-06 |
| **Time** | 08:00 PM |
| **Location** | Reunión virtual mediante Google Meet |
| **Prepared By** | HydroTeam |
| **Attendees (to planning meeting)** | Espinar Martínez, Gabriel Ferran / Guevara Serrano, Diego Ismael / Montalvan Palomino, Bruno Rodolfo / Orosco Ttamiña, Juan Carlos / Razuri Alvarez, Matias Francesco |
| **Sprint 1 – Review Summary** | Durante el Sprint 1 se completó el desarrollo inicial del Landing Page y los principales artefactos UX/UI del proyecto. Asimismo, durante la revisión se identificaron observaciones relacionadas con enlaces faltantes, visibilidad de algunas imágenes del informe y pequeños ajustes visuales de la interfaz. |
| **Sprint 1 – Retrospective Summary** | Durante la retrospectiva del Sprint 1, el equipo identificó la necesidad de mejorar la organización del trabajo colaborativo y la estructura del frontend para facilitar el desarrollo de nuevas funcionalidades. Además, se concluyó que era necesario utilizar una arquitectura más escalable y una mejor estrategia de manejo de ramas para reducir conflictos durante la integración del proyecto. |
| **Sprint Goal & User Stories** | |
| **Sprint 2 Goal** | Nuestro enfoque está en desarrollar la primera versión funcional de la Web Application de TankIQ utilizando Angular y una arquitectura modular organizada por bounded contexts. Creemos que esto permitirá integrar los primeros módulos frontend del sistema y facilitar el trabajo paralelo del equipo. Esto se confirmará cuando los usuarios puedan navegar entre las principales vistas de la aplicación y visualizar la integración inicial del dashboard y módulos base del sistema. |
| **Sprint 2 Velocity** | 40 |
| **Sum of Story Points** | 40 |

### 5.2.2.2. Aspect Leaders and Collaborators.

Durante el Sprint 2, el equipo trabajó utilizando una estrategia basada en ramas feature para
desarrollar de manera paralela los diferentes módulos frontend de la Web Application. Cada
integrante asumió la responsabilidad principal de un bounded context específico, permitiendo
mantener una mejor organización del proyecto y facilitar la integración de funcionalidades
hacia las ramas develop y main.

La siguiente Matriz LACX muestra la distribución de responsabilidades del equipo durante el
Sprint 2.

| Team Member | GitHub Username | Landing Angular | IAM Module | Dashboard Overview | Water Monitoring | Alerts & Notifications |
|---|---|---|---|---|---|---|
| Espinar Martínez, Gabriel Ferran | zzZero14 | C | C | C | L | C |
| Guevara Serrano, Diego Ismael | digetto | L | C | C | C | C |
| Montalvan Palomino, Bruno Rodolfo | br1rodolfo | C | L | C | C | C |
| Orosco Ttamiña, Juan Carlos | juancarlosorosco59 | C | C | L | C | C |
| Razuri Alvarez, Matias Francesco | u202410772 | C | C | C | C | L |

### 5.2.2.3. Sprint Backlog 2.

El Sprint Backlog 2 estuvo orientado al desarrollo de la primera versión de la Frontend Web
Application de TankIQ utilizando Angular. El trabajo incluyó la implementación de la
arquitectura modular del sistema, layouts reutilizables, navegación mediante Angular Router y
la estructura inicial de los diferentes módulos definidos en el Product Backlog. Además, se
realizaron mejoras visuales y técnicas sobre el Landing Page desarrollado durante el Sprint 1.

| **Sprint 2** | | | | | | | |
|---|---|---|---|---|---|---|---|
| **User Story** | | **Work-Item / Task** | | | | | |
| **User Story ID** | **Título** | **Task ID** | **Task Title** | **Description** | **Estimation (Hours)** | **Assigned To** | **Status** |
| US54 | Acceder a la Web Application | T09 | Configurar arquitectura Angular | Inicializar el proyecto Angular y organizar la estructura modular mediante bounded contexts, standalone components y lazy loading. | 4 | Orosco Ttamiña, Juan Carlos | Done |
| US55 | Navegar entre módulos del sistema | T10 | Implementar sistema de routing | Configurar rutas principales, layouts y navegación entre Landing, Dashboard, IAM, Monitoring y Alerts. | 4 | Orosco Ttamiña, Juan Carlos | Done |
| US56 | Visualizar métricas principales del sistema | T11 | Implementar Dashboard Overview | Desarrollar la primera vista del dashboard incluyendo métricas, sidebar y componentes base del panel principal. | 5 | Orosco Ttamiña, Juan Carlos | Done |
| US57 | Acceder al Landing Page desde Angular | T12 | Migrar Landing Page | Adaptar el Landing Page desarrollado en el Sprint 1 hacia una arquitectura basada en componentes Angular reutilizables. | 4 | Guevara Serrano, Diego | Done |
| US58 | Gestionar el acceso de usuarios | T13 | Implementar módulo IAM | Crear la estructura inicial del módulo IAM incluyendo vistas de login, autenticación y navegación base. | 4 | Montalvan Palomino, Bruno | Done |
| US59 | Consultar información de monitoreo | T14 | Implementar módulo Water Monitoring | Desarrollar la estructura inicial y rutas del módulo de monitoreo de agua utilizando componentes placeholder y navegación integrada. | 3 | Espinar Martínez, Gabriel | Done |
| US60 | Visualizar alertas y notificaciones | T15 | Implementar módulo Alerts & Notifications | Crear la estructura inicial del módulo de alertas y notificaciones utilizando vistas placeholder y navegación interna. | 3 | Razuri Alvarez, Matias | Done |
| US61 | Mantener una estructura escalable del sistema | T16 | Organizar proyecto por feature branches | Configurar el flujo de trabajo basado en ramas feature y bounded contexts para permitir el desarrollo paralelo e integración del sistema. | 2 | HydroTeam | Done |
| US62 | Mantener coherencia visual en la aplicación | T17 | Ajustar estilos y layouts | Corregir tipografía, tamaños, espaciados y estilos generales para mantener consistencia visual entre Landing y Web Application. | 3 | HydroTeam | Done |

### 5.2.2.4. Development Evidence for Sprint Review.

A continuación se presenta el registro de commits realizados en el repositorio
HydroTeam-Frontend durante el Sprint 2. Los commits reflejan el trabajo realizado por el
equipo para implementar la arquitectura Angular, organizar el proyecto mediante ramas feature
y desarrollar los diferentes módulos frontend definidos para esta primera versión de la Web
Application.

  <h1>
    HydroTeam Frontend - Commit History Evidence
  </h1>

| Repository | Branch | Commit Id | Commit Message | Committed on (Date) |
|---|---|---|---|---|
| HydroTeam-Frontend | develop | f3f7102 | update | May 14, 2026 |
| HydroTeam-Frontend | develop | 32b1b83 | Update | May 14, 2026 |
| HydroTeam-Frontend | develop | 4b5ec38 | Fix import path for AlertsApiEndpoint | May 14, 2026 |
| HydroTeam-Frontend | develop | c40abdd | Delete | May 14, 2026 |
| HydroTeam-Frontend | develop | 14d48bf | feat: add model and entity | May 14, 2026 |
| HydroTeam-Frontend | develop | 981e216 | fix: remove unnecessary closing braces in alerts.store.ts | May 14, 2026 |
| HydroTeam-Frontend | develop | 4b52499 | fix: refactor monitoring component to use signals | May 14, 2026 |
| HydroTeam-Frontend | develop | d33b86b | fix: html section | May 14, 2026 |
| HydroTeam-Frontend | develop | 13d0cca | fix: refactor CSS for monitoring page layout and styles | May 14, 2026 |
| HydroTeam-Frontend | develop | 03393bf | Merge pull request #2 from hydronex-web-app-1ASI0729-2610-12029/feature/tb1-alerts-notifications | May 14, 2026 |
| HydroTeam-Frontend | develop | 21ba2c1 | Merge pull request #1 from hydronex-web-app-1ASI0729-2610-12029/feature/tb1-water-monitoring | May 14, 2026 |
| HydroTeam-Frontend | develop | d6b94ac | Merge branch 'feature/tb1-dashboard-overview' into develop | May 14, 2026 |
| HydroTeam-Frontend | develop | 5d09c3e | Merge branch 'feature/tb1-iam' into develop | May 14, 2026 |
| HydroTeam-Frontend | develop | 202936a | Fix IAM routing and CommonModule imports | May 14, 2026 |
| HydroTeam-Frontend | develop | e224ed3 | feat: fix style | May 14, 2026 |
| HydroTeam-Frontend | develop | cc5097a | feat: add water monitoring modules | May 14, 2026 |
| HydroTeam-Frontend | develop | d777343 | feat(landing): improve public landing page | May 14, 2026 |
| HydroTeam-Frontend | develop | 8652f14 | fix(iam): remove auth guard from app routes | May 14, 2026 |
| HydroTeam-Frontend | develop | b024a91 | feat(iam): protect dashboard routes with auth guard | May 14, 2026 |
| HydroTeam-Frontend | develop | 50702de | feat(iam): add sign-up route | May 14, 2026 |
| HydroTeam-Frontend | develop | f33c39f | feat(iam): update login component | May 14, 2026 |
| HydroTeam-Frontend | develop | af5e51d | feat(iam): update login template | May 14, 2026 |
| HydroTeam-Frontend | develop | 342e579 | feat(iam): update login styles | May 14, 2026 |
| HydroTeam-Frontend | develop | e4aab9a | feat(iam): add sign-up view | May 14, 2026 |
| HydroTeam-Frontend | develop | 82ebb82 | docs(iam): update authentication store | May 14, 2026 |
| HydroTeam-Frontend | develop | fb830d1 | docs(iam): update login component | May 14, 2026 |
| HydroTeam-Frontend | develop | 0f2f990 | feat(iam): add authentication store | May 14, 2026 |
| HydroTeam-Frontend | develop | 383a1d5 | feat(iam): add auth guard | May 14, 2026 |
| HydroTeam-Frontend | develop | 4e6a7e2 | feat(iam): add infrastructure layer | May 14, 2026 |
| HydroTeam-Frontend | develop | 4a9e67a | feat(iam): add user entity | May 14, 2026 |
| HydroTeam-Frontend | develop | a3b3f19 | feat(iam): add i18n keys for login, sign-up and validation in Spanish | May 14, 2026 |
| HydroTeam-Frontend | develop | 2dfcdf3 | feat(iam): add i18n keys for login, sign-up and validation in English | May 14, 2026 |
| HydroTeam-Frontend | develop | 34504c2 | feat: add matt-icon | May 14, 2026 |
| HydroTeam-Frontend | develop | 9631ba7 | feat: add component | May 14, 2026 |
| HydroTeam-Frontend | develop | 81d5173 | feat: add component | May 14, 2026 |
| HydroTeam-Frontend | develop | c49c987 | feat: add component | May 14, 2026 |
| HydroTeam-Frontend | develop | 4703329 | feat: add infrastructure | May 14, 2026 |
| HydroTeam-Frontend | develop | 864a764 | feat: add entities | May 14, 2026 |
| HydroTeam-Frontend | develop | e9fca61 | feat: create alerts-response.ts and define Alert DTOs and API response interfaces | May 13, 2026 |
| HydroTeam-Frontend | develop | cc9a028 | feat: create alerts-api.ts with CRUD operations | May 13, 2026 |
| HydroTeam-Frontend | develop | 380f1a3 | feat: create alerts-api-endpoints.ts | May 13, 2026 |
| HydroTeam-Frontend | develop | f8f1220 | feat: create alert-assembler.ts for data mapping between layers | May 13, 2026 |
| HydroTeam-Frontend | develop | b59bba7 | feat: create alert.entity.ts and define Alert domain entity and types | May 13, 2026 |
| HydroTeam-Frontend | develop | 5750144 | feat: create alerts.store.ts | May 13, 2026 |
| HydroTeam-Frontend | develop | 84f9895 | feat: add MatIcon to alerts css | May 13, 2026 |
| HydroTeam-Frontend | develop | b767c65 | feat: implement layout and control flow for alerts view | May 13, 2026 |
| HydroTeam-Frontend | develop | e4512bd | feat: add background color to alert card icons | May 13, 2026 |
| HydroTeam-Frontend | develop | 7944895 | merge: resolve README conflict | May 13, 2026 |
| HydroTeam-Frontend | develop | 1c7c294 | feat: initialize frontend base project | May 13, 2026 |
| HydroTeam-Frontend | develop | ccc907a | Initial commit | Apr 11, 2026 |

### 5.2.2.5. Execution Evidence for Sprint Review.

Durante el Sprint 2, el equipo HydroTeam implementó la primera versión de la Frontend Web
Application de TankIQ utilizando Angular. El desarrollo se enfocó en establecer una
arquitectura modular y escalable, integrando navegación mediante Angular Router, layouts
reutilizables y componentes standalone para facilitar futuras integraciones del sistema.

Asimismo, se desarrollaron las primeras vistas correspondientes a los módulos Dashboard
Overview, IAM, Water Monitoring y Alerts & Notifications, manteniendo coherencia visual con
el Landing Page trabajado durante el Sprint 1.

Landing Page integrado en Angular

<img src="assets/tb1/landing-tb1.png" alt="Landing Angular" style="margin-bottom: 5px; width: 600px">

Dashboard Overview implementado en Angular

<img src="assets/tb1/dashboard-tb1.png" alt="Dashboard Overview" style="margin-bottom: 5px; width: 600px">

Módulo Alerts & Notifications

<img src="assets/tb1/alerts-tb1.png" alt="Alerts Module" style="margin-bottom: 5px; width: 600px">

Módulo Water Monitoring

<img src="assets/tb1/water-monitoring-tb1.png" alt="Water Monitoring" style="margin-bottom: 5px; width: 600px">

Módulo IAM y vistas de autenticación

<img src="assets/tb1/iam-tb1.png" alt="IAM Module" style="margin-bottom: 5px; width: 600px">

### 5.2.2.6. Services Documentation Evidence for Sprint Review.

El repositorio HydroTeam-Frontend contiene documentación relacionada con la instalación del
proyecto, ejecución de la aplicación y estructura modular implementada durante el Sprint 2.
Asimismo, el archivo README.md incluye instrucciones para configurar Angular, ejecutar builds
y trabajar colaborativamente utilizando ramas feature y flujo GitHub Flow.

Repositorio y documentación del proyecto frontend

### 5.2.2.7. Software Deployment Evidence for Sprint Review.

En esta sección se detallan las evidencias correspondientes al despliegue 
de la primera versión de la aplicación web frontend de TankIQ. La arquitectura 
de la solución contempla una Single Page Application (SPA) desarrollada sobre el 
framework Angular, optimizada para el alojamiento en Firebase Hosting con soporte
integral para enrutamiento interno y navegación fluida.

Cabe precisar que, debido a priorizaciones en el cronograma del Sprint 2, la fase 
de deployment final no fue concluida en el periodo actual. No obstante, se ha 
establecido como un entregable crítico y de alta prioridad para el Sprint 3, asegurando 
así la disponibilidad de la plataforma en el próximo ciclo de desarrollo.

### 5.2.2.8. Team Collaboration Insights during Sprint.

Durante el Sprint 2, el equipo HydroTeam trabajó utilizando GitHub y una estrategia basada
en ramas feature para desarrollar de manera paralela los diferentes módulos frontend de la
aplicación. Cada integrante trabajó sobre un bounded context específico, permitiendo una
mejor organización del proyecto y facilitando la integración de funcionalidades mediante Pull
Requests hacia las ramas `develop` y `main`.

Además, el equipo realizó coordinaciones constantes relacionadas con arquitectura Angular,
routing, layouts y diseño visual de la aplicación, manteniendo una comunicación continua para
resolver observaciones y unificar criterios técnicos durante el desarrollo.

Network Graph del repositorio HydroTeam-Frontend

<img src="assets/git-hub/insights-tb1.png" alt="Network Graph" style="margin-bottom: 5px; width: 600px">

Contributors — commits realizados por integrante

<img src="assets/git-hub/contributors-tb1.png" alt="Contributors" style="margin-bottom: 5px; width: 600px">
