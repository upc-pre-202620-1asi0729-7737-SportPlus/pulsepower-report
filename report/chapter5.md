# Capítulo V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management
Con el objetivo de garantizar un desarrollo fluido, estandarizado y compatible entre todos los miembros del equipo PulsePower, se ha definido el siguiente entorno de desarrollo para el ecosistema PulsePower
### 5.1.1. Software Development Environment Configuration
Se listan a continuación las herramientas utilizadas a lo largo de todo el ciclo de vida del proyecto, cubriendo desde la gestión hasta el despliegue:

**Project & Requirements Management:**
- Trello: Herramienta SaaS para la gestión ágil del Product Backlog y Sprints. Referencia: trello.com
- UXPressia: Herramienta SaaS para la gestión de requerimientos (Journey Maps, User Personas). Referencia: uxpressia.com
- Product UX/UI Design:
  - Figma: Herramienta SaaS para la elaboración de Wireframes, Mock-ups y Prototipos. Referencia: figma.com
- Herramientas de Desarrollo (IDEs y Editores):
  - WebStorm: IDE para el desarrollo de Frontend & Web App (Extensiones: Angular Language Service, Prettier, ESLint). Descarga: jetbrains.com/webstorm
  - IntelliJ IDEA: IDE optimizado para el desarrollo del Backend con Spring Boot. Descarga: jetbrains.com/idea
- Stack Tecnológico y Entorno de Ejecución:
  - Node.js (LTS v20+): Entorno de ejecución para Angular y la Landing Page. Descarga: nodejs.org
  - Java Development Kit (JDK 17): Entorno base para Spring Boot. Descarga: oracle.com/java
- Herramientas de Pruebas y Documentación:
  - Postman: Testeo y validación de los endpoints del backend. Descarga: postman.com
### 5.1.2. Source Code Management
El código fuente del proyecto se gestionará utilizando Git como sistema de control de versiones y GitHub como plataforma colaborativa, bajo una organización pública que favorece la modularidad y el despliegue independiente de cada componente.

**Estrategia de Ramas (GitFlow)**

Se implementará un flujo de trabajo basado en GitFlow con el objetivo de garantizar la estabilidad y trazabilidad del desarrollo:
- main: Rama principal. Contiene únicamente código estable, probado y desplegado en producción. Cada versión liberada estará debidamente etiquetada.
- develop: Rama de integración continua. Aquí se fusionan todas las nuevas características antes del pase a producción.
- feature/US[ID]-[nombre]: Ramas de desarrollo temporales, creadas a partir de develop para trabajar una User Story específica (ej. feature/US07-user-profile-registration). Una vez finalizadas, se integran nuevamente a develop mediante un Pull Request (PR).
- hotfix/[nombre]: Ramas destinadas a la corrección de errores críticos detectados en producción (main), que requieren una solución inmediata.

**Convenciones de Versionado y Commits**

- Semantic Versioning (SemVer 2.0.0): Los lanzamientos oficiales en la rama main se etiquetarán bajo el formato vMAJOR.MINOR.PATCH (ej. v1.0.0).
- Conventional Commits 1.0.0: Todos los commits seguirán una estructura semántica (tipo(alcance): descripción breve) para generar un historial legible por máquinas y humanos.

- **Tipos permitidos**

- feat: Nueva funcionalidad (ej. feat(auth): add login endpoint)
- fix: Corrección de errores (ej. fix(map): resolve overlap issue)
- docs: Cambios en documentación (ej. docs: update readme)
- style: Cambios de formato que no afectan la lógica del código (espacios, indentación, etc.)

### 5.1.3. Source Code Style Guide & Conventions

Para mantener la legibilidad y calidad del código, todo el equipo aplicará nomenclatura estrictamente en inglés para clases, variables, métodos y bases de datos. Además, se adoptan las siguientes guías de estilo oficiales:
- HTML & CSS: Se seguirán las directrices de la HTML Style Guide and Coding Conventions de W3C y la Google HTML/CSS Style Guide.
- Frontend (Angular / TypeScript): Se respetará la Angular Coding Style Guide. Las clases usarán PascalCase, variables y métodos camelCase, y los archivos kebab-case. Se utilizará Prettier y ESLint para automatizar el formato en cada commit.
- Backend (Spring Boot / Java): Se aplicará la Google Java Style Guide. La arquitectura se dividirá en capas estrictas (Controllers, Services, Repositories, Entities), respetando los seis bounded contexts definidos en el diseño orientado a objetos (Training Management, Sleep Management, Wellness Management, Physiological Analysis & Recommendations, Reporting y Community). Los endpoints RESTful usarán sustantivos en plural (ej. GET /api/v1/training-sessions).
- Requerimientos: Se emplearán las Gherkin Conventions para la redacción estructurada de los criterios de aceptación (Given/When/Then).

### 5.1.4. Software Deployment Configuration

- El despliegue del ecosistema PulsePower combinará métodos de publicación ágil para el Frontend y prácticas de Integración/Despliegue Continuo (CI/CD) para el Backend:
- Landing Page (Sitio Estático): Se desplegará utilizando la infraestructura gratuita de GitHub Pages, configurada para publicar automáticamente cada PR fusionado en main desde el repositorio del Landing Page.
- Frontend (Angular Web App): Se desplegará en la plataforma PaaS Vercel, utilizando su integración nativa con GitHub para publicar automáticamente cada PR fusionado en main.

## 5.2 Landing Page, Services & Applications Implementation

En esta sección se describe el proceso de implementación del producto PulsePower, incluyendo el desarrollo, pruebas, documentación y despliegue de la Landing Page. Para este avance se implementó la primera versión del Landing Page, orientada a presentar la propuesta de valor del sistema: "No puedes rendir más sin recuperarte mejor. Conócete primero."	

### 5.2.1 Sprint 1

En esta sección se describen los principales acuerdos y definiciones realizadas durante el Sprint Planning del Sprint 1, enfocado en la implementación del Landing Page de PulsePower.

#### 5.2.1.1 Sprint Planning 1

**Sprint Planning Background**

| Campo | Detalle |
| :--- | :--- |
| **Sprint #** | Sprint 1 |
| **Date** | 13-09-2025 |
| **Time** | 17:30 |
| **Location** | Reunion Virtual |
| **Prepared By** | Viza Quispe, Marlon Packard |
| **Attendees** | Evangelista Ygnacio, Sergio Joaquin<br>Martin Farro, Alexis Sebastian<br>Carbajal Santivañez, Sebastian Aaron<br>Osorio Ramírez, Eduardo Jesús |
| **Sprint 1 Review Summary** | Durante el Sprint 1 se logró implementar correctamente el Landing Page responsive de PulsePower, incluyendo navegación entre secciones, adaptación móvil y soporte multilenguaje. Además, el equipo consolidó la estructura base del frontend y definió estándares iniciales de trabajo colaborativo utilizando GitFlow y Trello para la gestión de tareas. |
| **Sprint 1 Restrospective Summary** | El equipo identificó como principal fortaleza la capacidad tecnica y la comunicación constante durante el desarrollo del Sprint 1. Sin embargo, se detectaron pequeños retrasos en la delegacion de tareas, por lo que para este sprint se acordó mejorar la coordinación en estas fases y aumentar la frecuencia de revisiones entre integrantes. |

<br>

**Sprint Goal & User Stories**

| Campo | Detalle |
| :--- | :--- |
| **Sprint 1 Goal** | Our focus is on delivering a fast, static Landing Page (HTML/CSS/JS) with language support to attract clients and validate our value proposition. This will be confirmed when the Landing Page is deployed and fully navigable by users. |
| **Sprint 1 Velocity** | 16 Story Points |
| **Sum of Story Points** | 16 |

#### 5.2.1.2 Aspect Leaders and Collaborators

A continuación se detalla la matriz de liderazgo y colaboración (LACX) para brindar claridad en la comunicación del equipo durante el desarrollo de las tareas de este Sprint.

| Team Member (Last Name, First Name) | GitHub Username | Landing Page UI/UX | Landing Page Structure | Basic Funcs | Special Funcs |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Osorio Ramírez, Eduardo Jesús | @[Iron819] | C | C | L | L |
| Carbajal Santivañez, Sebastian Aaron | @[usuario] | L | C | C | C |
| Martín Farro, Alexis Sebastián | @axismf | C | L | C | C |
| Viza Quispe, Marlon Packard | @[usuario] | C | C | L | C |
| Evangelista Ygnacio, Sergio Joaquin | @[usuario] | C | C | C | L |

*(L = Leader, C = Collaborator)*

#### 5.2.1.3 Sprint Backlog 1

Se detalla el Sprint Backlogk 1, con su respectivo tablero en Trello: https://trello.com/invite/b/6aaede0bb47af502ba9eb29d/ATTI6002400c8c79f6ddabb88999b2168b7a7AB82763/pulsepower

**Sprint #**: Sprint 1

**Sprint #**: Sprint 1

| Story ID | Story Title                | Task ID | Task Title                    | Task Description                                                                                                      | Estimation (Hours) | Assigned To                          | Status      |
|:---------|:---------------------------|:--------|:------------------------------|:----------------------------------------------------------------------------------------------------------------------|:-------------------|:-------------------------------------|:------------|
| US-00    | Landing Page de Validación | TS00.1  | Setup Static Proj             | Inicializar el repositorio del Landing Page con la estructura base HTML5/CSS y configurar el tablero de Trello.       | 3                  | Evangelista Ygnacio, Sergio Joaquín  | Done        |
| US-00    | Landing Page de Validación | TS00.2  | Implement Hero Section        | Desarrollar la sección principal (Hero) responsiva con Flexbox/Grid, incluyendo la propuesta de valor de PulsePower.  | 5                  | Evangelista Ygnacio, Sergio Joaquín  | Done        |
| US-00    | Landing Page de Validación | TS00.3  | Maquetar sección "Beneficios" | Crear contenedor y tarjetas informativas sobre los beneficios de la pulsera para deportistas y usuarios de bienestar. | 4                  | Martín Farro, Alexis Sebastián       | Done        |
| US-00    | Landing Page de Validación | TS00.7  | Header / Navbar               | Implementar la barra de navegación superior con enlaces a cada sección y al selector de idioma.                       | 4                  | Martín Farro, Alexis Sebastián       | Done        |
| US-00    | Landing Page de Validación | TS00.4  | Grid de funcionalidades       | Implementar una cuadrícula responsiva con las funcionalidades principales (indicadores, recomendaciones, reportes).   | 4                  | Viza Quispe, Marlon Packard          | Done        |
| US-00    | Landing Page de Validación | TS00.5  | Selector de idioma            | Implementar el mecanismo de cambio de idioma (Español/Inglés) reutilizable en todas las secciones del Landing.        | 4                  | Viza Quispe, Marlon Packard          | In Progress |
| US-00    | Landing Page de Validación | TS00.9  | Segmentos y Testimonios       | Maquetar las secciones de segmentos objetivo ("Para quién es") y los testimonios de usuarios.                         | 4                  | Osorio Ramírez, Eduardo Jesús        | Done        |
| US-00    | Landing Page de Validación | TS00.10 | FAQ y Contacto                | Implementar la sección de preguntas frecuentes y el formulario estático de contacto.                                  | 4                  | Osorio Ramírez, Eduardo Jesús        | Done        |
| US-00    | Landing Page de Validación | TS00.6  | Maquetar sección "Planes"     | Desarrollar el layout de la sección de planes de suscripción.                                                         | 4                  | Carbajal Santivañez, Sebastian Aaron | Done        |
| US-00    | Landing Page de Validación | TS00.8  | Maquetar Footer               | Añadir información de contacto, redes sociales y datos de la organización SportPlus.                                  | 2                  | Carbajal Santivañez, Sebastian Aaron | Done        |
| US-00    | Landing Page de Validación | TS00.11 | Despliegue en GitHub Pages    | Configurar la rama main y publicar el sitio estático mediante GitHub Pages.                                           | 2                  | Carbajal Santivañez, Sebastian Aaron | Done        |

Tablero de Trello:

![Tablero Trello.png](../assets/images/Tablero%20Trello.png)

#### 5.2.1.4 Development Evidence for Sprint Review

Durante el Sprint 1, el equipo avanzó en la implementación del Landing Page, desarrollado en HTML5, CSS3 y JavaScript vanilla, y desplegado en GitHub Pages. Los principales avances incluyeron la estructura base de todas las secciones de la landing (Hero, Funcionalidades, Segmentos, Planes, Testimonios, FAQ, Contacto y Footer), la implementación del diseño responsive con media queries para móvil y tablet, y la habilitación del scroll suave y menú de navegación. A continuación se presentan los commits representativos del repositorio de Landing Page durante este Sprint.  

| Repository | Branch | Commit Id | Commit Message | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `82efb03` | `feat(landing): add responsive styles for various sections and navigation` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `53d26c4` | `feat(landing): add styles for legal pages with responsive design.` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `7b90494` | `feat(landing): add floating language switcher with responsive design.` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `a06344a` | `feat(landing): add styles for Footer section with responsive layout and social links` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `d792b51` | `feat(landing): add styles for Overview & Secondary Video section with grid layout and responsive design` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `de5e9f5` | `feat(landing): add styles for Plans & Pricing section with toggle and responsive cards` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `ceb849f` | `feat(team): add styles for Our Team section with responsive cards and hover effects` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `600dd3b` | `feat(video): add styles for interactive video section with tabs and player` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `ec96c5c` | `feat(landing): add styles for mid CTA banner section` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `2fffd30` | `feat(landing): add styles for How PulsePower Works section with 5-step arched cards` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `9553c2c` | `feat(landing): add styles for coaching services section and accordion components` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `fa5c120` | `feat(landing): add styles for science-backed coaching section` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `3a41450` | `feat(landing): add styles for marquee banner and ticker items` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `c42ccd0` | `feat(landing): add styles for hero section, including layout, watermark, and call-to-action button` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `7e8d84c` | `feat(landing): add language toggle switch and auth button styles` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `b7b5db3` | `feat(landing): add implement fixed header and navigation styles` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `7dac399` | `feat(landing): add SVG assets for PulsePower landing page and styles` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `main` | `16057ef` | `First Commit.` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `a745c4b` | `feat(landing): add implement function to apply translations based on selected language` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `b3d8e7a` | `feat(landing): add function to flatten nested translation objects` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `17b17c3` | `feat(landing): add Interactive Scripts & i18n` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `616c78d` | `feat(landing): add Spanish translations for overview and footer sections` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `0122e01` | `feat(landing): add Spanish translations for team and plans sections` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `34a43ca` | `feat(landing): add Spanish translations for CTA banner and video section` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `020e79f` | `feat(landing): add Spanish translations for coaching services and process steps` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `887f36d` | `feat(landing): add Spanish translations for navigation, hero, marquee, and science sections` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `9ba1dfb` | `feat(landing): fix names of i18n.` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `573634c` | `feat(landing): add Spanish translations for overview and footer sections` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `db2765a` | `feat(landing): add Spanish translations for video section, team members, and plans` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `9acf111` | `feat(landing): add Spanish translations for coaching services and process steps` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `82d5e88` | `feat(landing): add Spanish translations for marquee and science sections` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `517b628` | `feat(landing): add English translations for navigation and hero sections` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `2ea4dc7` | `feat(landing): add YouTube video placeholder styles with hover effects` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `06646a6` | `feat(package): initialize package-lock.json for PulsePower website` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `3780523` | `feat (landing): add main HTML structure for PulsePower website` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `419b0c4` | `feat (landing): add tos main` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `9c1bb99` | `feat (landing): add tos header` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `6ac16c0` | `feat (landing): add tos` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `e664249` | `feat(landing): add toggle functionality for pricing plans with active state management` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `f5f3437` | `feat(landing): add implement toggle functionality for monthly and annual pricing plans` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `d99a19a` | `feat(landing): add video embed functionality with tab navigation and active state management` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `ffeac89` | `feat(landing): add accordion functionality for coaching services and initialize first active tab` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `4f1390c` | `feat(landing): add scroll event to change header background on scroll` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `58341b5` | `feat(landing): add floating language switcher and mobile menu toggle functionality` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `3b744cf` | `feat(landing): add language toggle functionality with synchronization and HTML lang update` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `3aa73ec` | `feat(landing): add synchronize language toggle with active state and thumb position` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `58ac9ca` | `feat(landing): add functionality to apply translations to placeholders and HTML elements` | `09/18/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `main` | `696bf54` | `Merge pull request #2 from upc-pre-202620-1asi0729-7737-SportPlus/feature/app-features` | `09/19/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `9d2f6cb` | `feat(landing): fix video player placeholders to use div instead of anchor tags` | `09/19/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `cde0848` | `feat(landing): fix remove hardcoded YouTube links from video player placeholders` | `09/19/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `4ae3299` | `feat(landing): fix enhance hero section and team card layout with new styles` | `09/19/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `5225ad3` | `feat(landing):add update team member details and replace logo images` | `09/19/2026` |
| `https://github.com/upc-pre-202620-1asi0729-7737-SportPlus/pulsepower-website` | `feature/app-features` | `047c046` | `feat(landing): add privacy policy page for PulsePower website` | `09/18/2026` |

### 5.2.1.5. Execution Evidence for Sprint Review.

Durante el Sprint 1, el equipo implementó y desplegó la primera versión pública del Landing Page de SportPlus, accesible en: [https://upc-pre-202620-1asi0729-7737-sportplus.github.io/pulsepower-website/](https://upc-pre-202620-1asi0729-7737-sportplus.github.io/pulsepower-website/)).

La landing page presenta un diseño moderno y responsive enfocado en la salud y el fitness. Incluye secciones clave como el Hero con llamadas a la acción, descripción de servicios de coaching, demostraciones de la aplicación, videos explicativos, presentación del equipo y planes de bienestar. A continuación se presenta la captura de la página implementada.

![PulsePower-Landing_Page_Wireframe.jpeg](../assets/images/PulsePower-Landing_Page_Wireframe.jpeg)

Esta captura de pantalla muestra el diseño completo de la página web de **PulsePower**, diseñada con un estilo dinámico que intercala secciones de fondo oscuro, blanco y tonos pastel claros. En la parte superior, el *Hero section* destaca la palabra "HEALTH" en gran tamaño junto a una atleta, con el lema *"Science-Backed, Results Driven Coaching"* y botones de registro. Descendiendo, la página expone los servicios (*Our Coaching Services*) con una imagen de entrenamiento y una lista de beneficios.

Una parte central muy visual es la sección *"How PulsePower Works"*, que utiliza coloridas maquetas de dispositivos móviles (en tonos rosa, azul, naranja y turquesa) para explicar el proceso paso a paso. Posteriormente, se integran reproductores de video incrustados para detallar características como monitoreo fisiológico y reportes de progreso. Finalmente, la página incluye una sección de presentación del equipo (*Our Team*) con fotografías y nombres de los integrantes, una demostración de la interfaz móvil de la app bajo el título *"A Plan for Your Wellbeing"*, y concluye con un pie de página (footer) oscuro que contiene enlaces de navegación y redes sociales.

### 5.2.1.6. Services Documentation Evidence for Sprint Review.

Durante el Sprint 1, el alcance de implementación estuvo enfocado exclusivamente en el desarrollo, diseño y despliegue de la primera versión del Landing Page de PulsePower/SportPlus, así como en la estructuración de la documentación técnica y las bases del sistema de diseño a nivel de interfaz de usuario.

En consecuencia, no se ha realizado en este sprint el desarrollo de Web Services ni la implementación de endpoints RESTful, por lo que no existe documentación de servicios mediante OpenAPI/Swagger que reportar en esta entrega. La documentación de servicios será incorporada a partir del Sprint 2, cuando se inicie la implementación del backend, conforme al plan de desarrollo establecido en el Product Backlog.

### 5.2.1.7. Software Deployment Evidence for Sprint Review.

Durante el Sprint 1, el equipo realizó el despliegue de la primera versión pública de la Landing Page utilizando GitHub Pages, servicio gratuito y estático integrado directamente con el repositorio de GitHub.

* **Plataforma de despliegue:** GitHub Pages — [https://pages.github.com](https://upc-pre-202620-1asi0729-7737-sportplus.github.io/pulsepower-website/)
* **URL base del repositorio:** https://github.com/upc-pre-202620-1asi0729-7737-SportPlus

**Proceso de despliegue:**
1. Se utilizó el repositorio central del equipo bajo la organización de la clase.
2. Todo el contenido estático de la landing page (HTML, CSS, JS) fue integrado mediante Pull Requests revisados por los integrantes del equipo, siguiendo el flujo GitFlow.
3. En la sección *Settings → Pages* del repositorio, se seleccionó la rama principal de producción como fuente de publicación.
4. GitHub Pages generó automáticamente la URL pública y publicó el sitio estático para su acceso global.

### 5.2.1.8. Team Collaboration Insights during Sprint.

Durante el Sprint 1, el equipo utilizó GitHub como plataforma central de colaboración y control de versiones para el repositorio `upc-pre-202620-1asi0729-7737-SportPlus`, aplicando el flujo de trabajo GitFlow junto con Conventional Commits para mantener la trazabilidad.

**Flujo de trabajo aplicado:**
* Cada integrante trabajó en ramas individuales creadas desde la rama `develop` o `main`, siguiendo la nomenclatura de funcionalidades o capítulos de documentación (ej. `feature/chapter-1`, `feature/chapter-2`, etc.).
* Los cambios se integraron mediante Pull Requests, requiriendo revisión antes del merge.
* Los mensajes de commit siguieron un estándar estructurado (`feat:`, `fix:`, `docs:`), garantizando la correcta identificación del trabajo realizado, como se evidenció en los aportes de documentación de los capítulos 1 al 5.

![Commits Report.jpg](../assets/images/Commits%20Report.jpg)

Esta captura de pantalla muestra el gráfico de actividad de GitHub del repositorio `upc-pre-202620-1asi0729-7737-SportPlus`. En él se puede observar una alta concentración de trabajo en equipo durante el mes de septiembre, con múltiples contribuciones y commits registrados durante la consolidación del Sprint 1, reflejando el trabajo concurrente de los distintos líderes de aspecto y colaboradores en sus respectivas ramas.