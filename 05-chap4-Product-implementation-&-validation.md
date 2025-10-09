# Capítulo IV: Product Implementation & Validation

## 4.1. Software Configuration Management

### 4.1.1. Software Development Environment Configuration

A continuación, se listan las herramientas y estándares adoptados por el equipo para el desarrollo colaborativo del sistema:

| Actividad               | Herramienta / Guía                                    | Propósito                                                     | Tipo de acceso / Ruta                                                                                                                 |
| ----------------------- | ------------------------------------------------------ | -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Project Management      | Trello                                                 | Seguimiento de backlog, tareas y sprints.                      | [https://trello.com/](https://trello.com/)                                                                                               |
| Requirements Management | Gherkin Conventions                                    | Escritura legible de requisitos con formato Given/When/Then.   | [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/)                                                                   |
| Product UX/UI Design    | Figma                                                  | Prototipos y diseño responsive.                               | SaaS –[https://figma.com](https://figma.com)                                                                                            |
| Frontend Dev            | Kotlin, Flutter                                        | Construcción del frontend del sistema.                        | https://kotlinlang.org/ / https://flutter.dev/                                                                                       |
| Backend Dev             | Java + Spring Boot                                     | Lógica de negocio y servicios REST.                           | [https://spring.io/projects/spring-boot](https://spring.io/projects/spring-boot)                                                         |
| IDE                     | IntelliJ IDEA + Android Studio                         | Desarrollo, depuración y pruebas.                             | [https://www.jetbrains.com/idea](https://www.jetbrains.com/idea) / [https://www.jetbrains.com/webstorm](https://www.jetbrains.com/webstorm) |
| Code Standards          | Google Java Style Guide, Google TypeScript Style Guide | Mantener un código consistente y legible.                     | [https://google.github.io/styleguide](https://google.github.io/styleguide)                                                               |
| Version Control         | Git + GitHub                                           | Gestión colaborativa del código fuente.                      | SaaS –[https://github.com](https://github.com)                                                                                          |
| Software Deployment     | Github pages                                           | Despliegue continuo del sistema en ambientes de testing.       | SaaS –[https://railway.app](https://railway.app) / [https://render.com](https://render.com)                                                |
| Software Documentation  | Swagger                                                | Documentación de APIs, funcionalidades y criterios técnicos. | SaaS –[https://swagger.io/](https://swagger.io/)                                                                                        |

### 4.1.2. Source Code Management

### 4.1.3. Source Code Style Guide & Conventions

#### Mobile Frontend (Kotlin + Android Studio + Jetpack Compose)

##### Convenciones generales:

- **Idioma**: Todo el código, nombres de clases, funciones y variables en **inglés**.
- **Indentación**: 4 espacios (convención oficial de Kotlin/Android).
- **Formato de archivos**: `.kt` (Kotlin).
- **Estilo de código adoptado**:
  - [Kotlin Coding Conventions](https://kotlinlang.org/docs/coding-conventions.html)
  - [Android Kotlin Style Guide](https://developer.android.com/kotlin/style-guide)

##### Nomenclatura:

- **Clases y objetos**: `PascalCase` (ej. `UserProfileActivity`, `RestockApp`).
- **Funciones y variables**: `camelCase` (ej. `getUserName()`, `userList`).
- **Constantes**: `UPPER_SNAKE_CASE` (ej. `MAX_USERS`).
- **Paquetes**: Todo en minúsculas y separados por punto (ej. `com.restockmobile.ui.profile`).
- **Layouts y recursos XML**: `snake_case` (ej. `activity_main.xml`, `user_profile_item.xml`).
- **IDs en layouts**: `camelCase` (ej. `btnSubmit`, `txtUserName`).

#### Backend (Java + Spring Boot + MongoDB)

##### Convenciones generales:

- **Idioma**: Código y documentación interna en **inglés**.
- **Indentación**: 4 espacios.
- **Formato de archivos**: `.java`
- **Estilo de código adoptado**:
  - [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
  - [Spring Boot Best Practices](https://docs.spring.io/spring-boot/docs/current/reference/html/best-practices.html)

##### Nomenclatura:

- **Clases**: `PascalCase` (ej. `UserService`, `UserController`).
- **Variables**: `camelCase` (ej. `userRepository`).
- **Constantes**: `UPPER_SNAKE_CASE` (ej. `MAX_USERS`).
- **Endpoints REST**: `kebab-case` (ej. `/api/user-profile`).
- **Paquetes**: Todo en minúsculas y separados por punto (ej. `com.restock.backend.service`).
- **Colecciones MongoDB**: `snake_case` en plural (ej. `users`, `product_items`).

#### Database (MongoDB – NoSQL)

##### Convenciones generales:

- **Formato**: Documentos en JSON.
- **Indentación**: 2 espacios para JSON.
- **Estilo de modelado**:
  - Documentos denormalizados (referencias mínimas).
  - Uso de `ObjectId` como clave primaria.

##### Nomenclatura:

- **Colecciones**: plural, `snake_case` (ej. `users`, `order_items`).
- **Campos**: `camelCase` (ej. `userName`, `createdAt`).
- **Índices**: nombrados con campos concatenados en `snake_case` (ej. `user_name_index`).

### 4.1.4. Software Deployment Configuration

Esta sección detalla los pasos necesarios para desplegar satisfactoriamente los componentes digitales de la solución Restock: la Landing Page, la aplicación móvil (Android) y los Web Services (backend), partiendo desde sus respectivos repositorios de código fuente.

#### 1. Landing Page - HTML, CSS y JavaScript

**Tecnología Base:**

- Lenguajes: HTML5, CSS3, JavaScript
- Hosting: GitHub Pages

**Configuración y Despliegue:**

- El código fuente se aloja en un repositorio público de GitHub.
- El archivo `index.html` debe encontrarse en la raíz del repositorio para que GitHub Pages lo detecte como punto de entrada.
- Para desplegar la Landing Page, se siguen los siguientes pasos:
  1. Acceder al repositorio en GitHub.
  2. Continuar con la sección **Settings** > **Pages**.
  3. En **Source**, se selecciona la rama principal (`main`) y la carpeta raíz (`/`).
  4. Se procede a guardar los cambios realizados.
- GitHub Pages genera automáticamente una URL pública con el formato `https://<organizacion>.github.io/<repositorio>/` donde el sitio estará disponible.
- Cada vez que se realiza un commit en la rama `main`, GitHub Pages actualiza de forma automática la versión publicada.

#### 2. Aplicación Móvil - Android (Kotlin + Android Studio)

**Tecnología Base:**

- Lenguaje: Kotlin
- Framework: Android Studio + Jetpack Compose
- Distribución: APK (Android Package)
- Hosting de pruebas: Firebase App Distribution

**Configuración y Despliegue:**

- El código fuente se gestiona en un repositorio de GitHub.
- Para la generación de versiones de prueba, se debe compilo el proyecto en Android Studio (`Build > Generate Signed APK`) y se verifico el funcionamiento de la aplicación en dispositivos físicos o emuladores Android.
- El archivo APK generado se sube a Firebase App Distribution, permitiendo el testeo con usuarios internos y externos seleccionados antes de su publicación oficial.
- El enlace de descarga puede ser compartido con los testers a través de correo electrónico, Google Drive o mediante un acceso en la Landing Page.
- Cada nueva versión de la aplicación para testeo se publica y gestiona mediante la plataforma Firebase, facilitando la retroalimentación y el control de versiones.

#### 3. Backend - Java + MongoDB

**Tecnología Base:**

- Framework: Spring Boot
- Lenguaje: Java 21
- Base de datos: MongoDB
- Contenedorización: Docker
- Hosting: Render o servicio equivalente

**Configuración y Despliegue:**

- El backend está estructurado según el enfoque de Domain-Driven Design (DDD), dividiendo el sistema en bounded contexts independientes.
- El código fuente se mantiene en un repositorio de GitHub.
- Para el despliegue, el repositorio incluye un archivo `Dockerfile` que define la imagen de la aplicación.
- El proveedor de hosting detecta automáticamente el Dockerfile y construye la imagen en cada actualización del repositorio.
- La base de datos MongoDB se configura mediante variables de entorno (por ejemplo, `MONGO_URI`), las cuales se gestionan en el panel de administración del hosting y nunca se almacenan en el código fuente.
- La API REST expuesta por el backend sigue la convención RESTful y sus endpoints están documentados mediante OpenAPI (Swagger). La interfaz Swagger UI está disponible para consulta y prueba.
- Los servicios protegidos requieren autorización mediante JWT, implementada con Spring Security, y los roles de usuario definen el nivel de acceso a cada funcionalidad.
- El despliegue es automático: cada push a la rama principal activa la reconstrucción y publicación en el servicio de hosting, sin necesidad de configurar pipelines de CI/CD adicionales.
- La aplicación móvil consume la API pública del backend utilizando HTTP para acceder a los servicios.

#### Referencias adicionales

- Documentación oficial de [Spring Boot](https://spring.io/projects/spring-boot), [Spring Data MongoDB](https://spring.io/projects/spring-data-mongodb), [Docker](https://docs.docker.com/), [Android Studio](https://developer.android.com/studio), [Firebase App Distribution](https://firebase.google.com/products/app-distribution) y [GitHub Pages](https://pages.github.com/).
- Para la gestión de variables de entorno y credenciales, se consulto las guías de los proveedores de hosting utilizados.

## 4.2. Landing Page & Mobile Application Implementation

### 4.2.1. Sprint 1

#### 4.2.1.1. Sprint Planning 1

<table>
  <tr>
    <td>Sprint #</td>
    <td>Sprint 1</td>
  </tr>
  <tr>
    <td><strong>Sprint Planning Background</strong></td>
    <td></td>
  </tr>
  <tr>
    <td>Date</td>
    <td>2025-09-25</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>08:00 pm (GMT-5)</td>
  </tr>
  <tr>
    <td>Location</td>
    <td>Modalidad remota mediante la plataforma Discord</td>
  </tr>
  <tr>
    <td>Prepared By</td>
    <td>Shapiama Rivera, Gabriela Nicole</td>
  </tr>
  <tr>
    <td>Attendees (to planning meeting)</td>
    <td>.Castro Alejos, Julio / Elescano Leon, Piero Hugo / Guerra Perez, José Jahaziel / Julca  Minaya, Sergio Gino / Shapiama Rivera, Gabriela Nicole</td>
  </tr>
  <tr>
    <td>Sprint 0 Review Summary</td>
    <td>Dado que este es el sprint inicial, no se presenta un resumen del sprint anterior.</td>
  </tr>
  <tr>
    <td>Sprint 0 Retrospective Summary</td>
    <td>Dado que este es el sprint inicial, no se presenta una retroalimentación del sprint anterior.</td>
  </tr>
  <tr>
    <td><strong>Sprint Goal & User Stories</strong></td>
    <td></td>
  </tr>
  <tr>
    <td>Sprint 1 Goal</td>
    <td>Nuestro enfoque está en presentar de forma efectiva nuestra propuesta de valor y e información detallada del producto a los nuevos visitantes. Además, habilitar funcionalidades clave para los administradores de restaurantes, como la gestión de inventario, la configuración de perfil, la gestión de recetas y la sección de ventas. Asimismo, en proporcionar puntos de acceso mediante el API de la plataforma, con el objetivo de que los desarrolladores frontend puedan integrar funcionalidades relacionadas con autenticación, perfil, inventario, recetas y ventas dentro de la app.
Creemos que esto ofrece mayor confianza hacia el equipo de trabajo y motiva a los visitantes a registrarse y probar el producto. Del mismo modo, mejora la eficiencia operativa de los administradores de restaurantes al facilitar la creación y gestión de ventas e insumos desde la aplicación móvil. Además, permite a los desarrolladores frontend implementar funcionalidades esenciales de forma más eficiente, incluyendo autenticación, inventario, ventas, recetas y perfil. 
Esto se confirmará cuando aumente la cantidad de visitantes que se registren en la plataforma. Del mismo modo, cuando se incremente la cantidad de ventas e insumos que registran administradores de restaurantes en la plataforma. Por último, cuando los desarrolladores frontend aumenten la cantidad de funcionalidades relacionadas con ventas, recetas, inventario y perfil en la app móvil.</td>
  </tr>
  <tr>
    <td>Sprint 1 Velocity</td>
    <td>35</td>
  </tr>
  <tr>
    <td>Sum of Story Points</td>
    <td>35</td>
  </tr>
</table>

#### 4.2.1.2. Sprint Backlog 1

#### 4.2.1.3. Development Evidence for Sprint Review

<table border="1" cellpadding="8" cellspacing="0" width="100%" style="margin-bottom:18px; text-align: center">
  <thead>
    <tr>
      <th style="margin-bottom:18px; text-align: center">Repository</th>
      <th style="margin-bottom:18px; text-align: center">Branch</th>
      <th style="margin-bottom:18px; text-align: center">Commit id</th>
      <th style="margin-bottom:18px; text-align: center">Commit Message Body</th>
      <th style="margin-bottom:18px; text-align: center">Commited on (Date)</th>
    </tr>
  </thead>
  <tbody style="margin-bottom:18px; text-align: center">
  <tr>
    <td>sergioJM05/restock-landing-page</td>
    <td>feature/project-structure</td>
    <td>0cdeda4</td>
    <td>chore: add project structure</td>
    <td>03/10/2025</td>
  </tr>
  <tr>
    <td> JulioXC4/restock-landing-page</td>
    <td>feature/menu</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add responsive menu</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>Aplicaciones-para-Dispositivos-Moviles/restock-landing-page</td>
    <td>feature/home</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add home section and first call to action</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>PieroHugo/restock-landing-page</td>
    <td>feature/about-us</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add about us section and development team presentation</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>GrabrielaShapiama28/restock-landing-page</td>
    <td>feature/benefits</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add benefits section to restaurant owners and restaurant suppliers</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>sergioJM05/restock-landing-page</td>
    <td>feature/testimonials</td>
    <td>aca3e6e</td>
    <td>feat: add representative testimonials section</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>sergioJM05/restock-landing-page</td>
    <td>feature/questions</td>
    <td>3adb741</td>
    <td>feat: add frequently questions</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>GrabrielaShapiama28/restock-landing-page</td>
    <td>feature/tutorial</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add steps to download and use the app on phones.</td>
    <td>04/10/2025</td>
  </tr>
  </tbody>
  <tr>
    <td>PieroHugo/restock-landing-page</td>
    <td>feature/contact</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add contact form.</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>Aplicaciones-para-Dispositivos-Moviles/restock-landing-page</td>
    <td>feature/download</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add call to action to download restock App</td>
    <td>04/10/2025</td>
  </tr>
    <tr>
    <td>JulioXC4/restock-landing-page</td>
    <td>feature/menu</td>
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add internacionalization EN / ES</td>
    <td>04/10/2025</td>
  </tr>
    <tr>
    <td>sergioJM05/restock-landing-page</td>
    <td>feature/footer</td>
    <td>63dc1b0</td>
    <td>feat: add footer with social medias and rights reserved</td>
    <td>04/10/2025</td>
  </tr>
</table>

#### 4.2.1.4. Testing Suite Evidence for Sprint Review

<p>A continuación, se presenta la evidencia de los commits relacionados con los <strong>Acceptance Tests</strong> automatizados del sprint, alojados en el repositorio <code>restock-acceptance-tests</code>. Cada archivo corresponde a un <em>Feature File</em> Gherkin que cubre escenarios de pruebas de aceptación para los diferentes Bounded Contexts (SDP, SOM, IAM, Profiles y Subscriptions).</p>

<table>
  <thead>
    <tr>
      <th>Repository</th>
      <th>Branch</th>
      <th>Commit Id</th>
      <th>Commit Message</th>
      <th>Commit Message Body</th>
      <th>Commited on (Date)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>2685de9471a0f83ad75205b618863b31e14e6198</td>
      <td>feat: add acceptance tests for user login scenarios (AT01.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>ed5ce3208cd2c63a242441f45fedae10d5425bec</td>
      <td>feat: add CRUD acceptance tests for recipe management (AT02.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>d28da8da0545a20d228ebb03a345149eb03ce84a</td>
      <td>feat: add acceptance tests for recipe activation with valid and invalid supplies (AT03.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>8aef03d2070aa74505d3434024f1e71bdd1505ca</td>
      <td>feat: add acceptance tests for menu grid search and pagination (AT04.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>f4c7f71e3c708a42c16118bd1117352323ff2ad2</td>
      <td>feat: add acceptance tests for sale registration and validation (AT05.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>9bad1d2efe2835d4af3e8fd38f647f65321bfa17</td>
      <td>feat: add acceptance test for marking inventory as applied after resource confirmation (AT06.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>7e2952b5fe6a208a82ac951d17f8faafdf031e00</td>
      <td>feat: add acceptance tests for Purchase Order lifecycle (AT07.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>c5b72b8f97adef3ad79517d69ed0f8127b58cda2</td>
      <td>feat: add acceptance test for posting goods receipt and event publishing (AT08.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>49c68c2a98aab663b43de3971d5e01349e0f9dda</td>
      <td>feat: add acceptance tests for restock functionality (supplier view and confirmation) (AT09.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
    <tr>
      <td>Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</td>
      <td>develop</td>
      <td>48d728c07104cb5cae35a48000f28c6891ba523b</td>
      <td>feat: add acceptance tests for profile update and plan limits enforcement (AT10.feature)</td>
      <td>-</td>
      <td>05/10/2025</td>
    </tr>
  </tbody>
</table>

<p><strong>Enlace al repositorio:</strong>  
<a href="https://github.com/Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests" target="_blank">https://github.com/Aplicaciones-para-Dispositivos-Moviles/restock-acceptance-tests</a></p>

#### 4.2.1.5. Execution Evidence for Sprint Review

#### 4.2.1.6. Services Documentation Evidence for Sprint Review

Durante este sprint se avanzó significativamente en la `<strong>`documentación de los servicios web (REST API)`</strong>` del sistema `<em>`Restock `</em>`, cubriendo los módulos de `<strong>`Profiles `</strong>`, `<strong>`Recipes `</strong>`, `<strong>`Batches `</strong>` y `<strong>`Authentication `</strong>`.
La documentación se generó utilizando `<strong>`OpenAPI (Swagger)`</strong>` y fue validada mediante peticiones reales desde el entorno de desarrollo (`<em>`localhost `</em>` y Railway).
Se registraron los endpoints principales relacionados con la gestión de usuarios, perfiles empresariales, recetas, insumos y autenticación, cubriendo los métodos HTTP `<code>`GET `</code>`, `<code>`POST `</code>`, `<code>`PUT `</code>` y `<code>`DELETE `</code>`.

A continuación, se presenta la tabla resumen de los `<strong>`Endpoints documentados `</strong>`, incluyendo la acción implementada, verbo HTTP, parámetros o cuerpo de solicitud y ejemplos de uso.

<table>
  <thead>
    <tr style="background-color:#f2f2f2;">
      <th>Endpoint</th>
      <th>Acción</th>
      <th>Verbo HTTP</th>
      <th>Parámetros / Request Body</th>
      <th>Ejemplo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>/api/v1/authentication/sign-up</td>
      <td>Registrar una cuenta</td>
      <td>POST</td>
      <td><pre>{
  "email": "string",
  "password": "string"
}</pre></td>
      <td><pre>{
  "email": "admin@restock.com",
  "password": "P@ssw0rd"
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/authentication/sign-in</td>
      <td>Iniciar sesión en la cuenta</td>
      <td>POST</td>
      <td><pre>{
  "email": "string",
  "password": "string"
}</pre></td>
      <td><pre>{
  "email": "admin@restock.com",
  "password": "P@ssw0rd"
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/profiles/{userId}/personal</td>
      <td>Actualizar información personal del usuario</td>
      <td>PUT</td>
      <td><pre>{
  "firstName": "string",
  "lastName": "string",
  "email": "string",
  "phone": "string",
  "address": "string",
  "country": "string",
  "avatar": "string"
}</pre></td>
      <td><pre>{
  "firstName": "Jahaziel",
  "lastName": "Guerra",
  "email": "admin@restock.com",
  "phone": "987654321",
  "address": "Av. Primavera 120",
  "country": "Perú",
  "avatar": "https://res.cloudinary.com/restock/avatar.png"
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/profiles/{userId}/password</td>
      <td>Cambiar la contraseña del usuario</td>
      <td>PUT</td>
      <td><pre>{
  "currentPassword": "string",
  "newPassword": "string"
}</pre></td>
      <td><pre>{
  "currentPassword": "P@ssw0rd",
  "newPassword": "NuevoP@ss2025"
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/profiles/{userId}/business</td>
      <td>Actualizar información del negocio</td>
      <td>PUT</td>
      <td><pre>{
  "businessName": "string",
  "businessAddress": "string",
  "description": "string",
  "businessCategoryIds": ["string"]
}</pre></td>
      <td><pre>{
  "businessName": "Restaurante San Miguel",
  "businessAddress": "Av. La Marina 2400",
  "description": "Comida criolla peruana",
  "businessCategoryIds": ["cat_01"]
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/recipes</td>
      <td>Crear una nueva receta</td>
      <td>POST</td>
      <td><pre>{
  "name": "string",
  "price": { "amount": "number", "currency": "string" }
}</pre></td>
      <td><pre>{
  "name": "Lomo Saltado",
  "price": { "amount": 28.90, "currency": "PEN" }
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/recipes/{id}</td>
      <td>Actualizar una receta existente</td>
      <td>PUT</td>
      <td><pre>{
  "name": "string",
  "price": { "amount": "number", "currency": "string" }
}</pre></td>
      <td><pre>{
  "name": "Ají de Gallina",
  "price": { "amount": 25.50, "currency": "PEN" }
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/recipes/{id}/supplies</td>
      <td>Agregar insumos a una receta</td>
      <td>POST</td>
      <td><pre>{
  "supplyId": "string",
  "quantity": "number"
}</pre></td>
      <td><pre>{
  "supplyId": "sup_beef",
  "quantity": 0.5
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/batches</td>
      <td>Crear un nuevo lote (batch)</td>
      <td>POST</td>
      <td><pre>{
  "supplyId": "string",
  "expirationDate": "string",
  "quantity": "number"
}</pre></td>
      <td><pre>{
  "supplyId": "sup_beef",
  "expirationDate": "2025-12-15",
  "quantity": 20
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/batches/{id}</td>
      <td>Actualizar un lote existente</td>
      <td>PUT</td>
      <td><pre>{
  "quantity": "number"
}</pre></td>
      <td><pre>{
  "quantity": 15
}</pre></td>
    </tr>
    <tr>
      <td>/api/v1/batches/{id}</td>
      <td>Eliminar un lote</td>
      <td>DELETE</td>
      <td><pre>N/A</pre></td>
      <td><pre>N/A</pre></td>
    </tr>
  </tbody>
</table>

Los endpoints fueron probados con datos de muestra y documentados con Swagger UI, disponible en el entorno de despliegue (`<em>`Railway `</em>`).
Repositorio de Web Services: `<a href="https://github.com/Jahazielgg/restock-backend" target="_blank">`https://github.com/Jahazielgg/restock-backend `</a>`
Últimos commits relacionados con documentación:

<ul>
  <li><code>58dcfa1</code> – Update OpenAPI definitions for Profiles and Recipes</li>
  <li><code>7b23a64</code> – Add Batches endpoints to Swagger spec</li>
  <li><code>c91bde4</code> – Improve schema examples for Authentication</li>
</ul>

#### 4.2.1.7. Software Deployment Evidence for Sprint Review

#### 4.2.1.8. Team Collaboration Insights during Sprint

## 4.3. Validation Interviews

### 4.3.1. Diseño de Entrevistas

Para garantizar que la aplicación cumpla con las necesidades reales de los usuarios finales, se diseñó un proceso de entrevistas de validación centrado en dos segmentos objetivos clave: administradores de restaurantes y proveedores de insumos. Cada sesión de validación incluirá interacción con el Landing Page y la aplicación (desktop y mobile), siguiendo flujos de usuario específicos que cubren funcionalidades críticas del sistema.

Objetivo General

Validar la usabilidad, comprensión y utilidad de las funcionalidades del sistema a través de sesiones controladas de interacción, aplicando principios de evaluación heurística y recogiendo observaciones cualitativas.

<table border="1" cellpadding="8" cellspacing="0" width="100%" style="margin-bottom:18px; text-align: center">
  <thead>
    <tr>
      <th style="margin-bottom:18px; text-align: center">Segmento</th>
      <th style="margin-bottom:18px; text-align: center">Elementos a validar</th>
      <th style="margin-bottom:18px; text-align: center">Mobile User Flow</th>
      <th style="margin-bottom:18px; text-align: center">Actividades durante la sesión</th>
    </tr>
  </thead>
  <tbody style="margin-bottom:18px; text-align: center">
  <tr>
    <td>Segmento 1: Administradores de Restaurantes</td>
    <td>
      <ul>
        <li>Claridad del valor ofrecido en el landing page.</li>
        <li>Flujo de suscripción y pago.</li>
        <li>Registro y gestión de insumos.</li>
        <li>Gestión de lotes e inventario.</li>
        <li>Gestión de ventas y recetas.</li>
        <li>Visualización y selección de proveedores.</li>
        <li>Realización y seguimiento de pedidos.</li>
        <li>Panel de alertas y resúmenes.</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Suscripción y pago con Stripe.</li>
        <li>Registro y gestión de insumos.</li>
        <li>Resumen e indicadores.</li>
        <li>Visualización de proveedores y productos.</li>
        <li>Seguimiento de pedidos.</li>
        <li>Comentarios a proveedores.</li>
        <li>Registro y visualización de ventas.</li>
        <li>Creación y gestión de recetas.</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Navegar el Landing Page y explicar lo que entienden del producto.</li>
        <li>Simular una suscripción desde un plan.</li>
        <li>Usar el módulo de inventario: registrar, editar y filtrar insumos.</li>
        <li>Acceder al panel de resumen y describir lo que entienden.</li>
        <li>Navegar por proveedores, seleccionar uno y simular una orden.</li>
        <li>Realizar comentarios sobre proveedores.</li>
        <li>Registrar una venta.</li>
        <li>Crear una receta.</li>
      </ul>
    </td>
  </tr>
