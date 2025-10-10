# Capítulo IV: Product Implementation & Validation

## 4.1. Software Configuration Management

### 4.1.1. Software Development Environment Configuration

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

## 4.2. Landing Page & Mobile Application Implementation

### 4.2.1. Sprint 1

#### 4.2.1.1. Sprint Planning 1

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

A continuación se presentan los materiales de evidencia correspondientes a los tres productos desarrollados durante el Sprint 1: Landing Page, Backend y Aplicación Móvil. Cada sección incluye una breve descripción del alcance entregado en este sprint, lo que se demuestra en el material audiovisual.

#### Landing Page

**Alcance entregado (Sprint 1)**  
- Landing Page desplegada y accesible públicamente.  
- Contenido explicativo sobre la propuesta de valor de RESTOCK: gestión de supplies para administradores de restaurantes y proveedores.  
- Secciones principales implementadas: Hero / Valor diferencial, Funcionalidades clave, CTA para registro/inicio de sesión, y contacto.  
- Diseño responsivo básico (desktop ↔ mobile) y coherencia visual con la identidad del producto.

**Qué se demuestra en el video**  
- Navegación entre secciones de la página.  
- Comportamiento responsivo en distintas resoluciones.  
- Enlaces hacia la zona de acceso (login/signup) y descripciones de las funcionalidades que conectan con la app móvil y el backend.

**Video de Landing Page:**  https://shorturl.at/NOzSq

![Execution Landing Page](assets/images/cap4/sprint1/execution/exec1.png)

#### Backend (API) — Estado: ~70%

**Alcance entregado (Sprint 1)**  
- Implementación de los endpoints core para soportar la lógica básica de la plataforma: autenticación, users/profiles, supplies, custom-supplies, recipes, batches, orders, business-categories y roles.  
- Documentación mínima de endpoints (endpoints listos para pruebas con Postman/Swagger).  
- Pruebas funcionales de endpoints principales (autenticación, listado/consulta de supplies, creación/consulta de orders y CRUD básico de recipes y custom supplies).

**Endpoints destacados implementados**  
- **Autenticación**  
  - `POST /api/v1/authentication/sign-up`  
  - `POST /api/v1/authentication/sign-in`  
- **Supplies (plataforma)**  
  - `GET /api/v1/supplies`  
  - `GET /api/v1/supplies/{supplyId}`  
  - `GET /api/v1/supplies/categories`  
- **Custom Supplies (usuario)**  
  - `GET /api/v1/custom-supplies`  
  - `POST /api/v1/custom-supplies`  
  - `PUT /api/v1/custom-supplies/{id}`  
  - `DELETE /api/v1/custom-supplies/{id}`  
  - `GET /api/v1/custom-supplies/user/{userId}`  
- **Recipes**  
  - `GET /api/v1/recipes` / `GET /api/v1/recipes/{id}`  
  - `POST /api/v1/recipes` / `PUT /api/v1/recipes/{id}` / `DELETE /api/v1/recipes/{id}`  
  - `GET /api/v1/recipes/{id}/supplies` / `POST /api/v1/recipes/{id}/supplies`  
  - `PUT /api/v1/recipes/{recipeId}/supplies/{supplyId}` / `DELETE /api/v1/recipes/{recipeId}/supplies/{supplyId}`  
- **Orders & Batches**  
  - `POST /api/v1/orders` / `GET /api/v1/orders` / `GET /api/v1/orders/{id}` / `DELETE /api/v1/orders/{id}`  
  - `POST /api/v1/orders/{orderId}/batches` / `GET /api/v1/orders/{orderId}/batches`  
  - `PUT /api/v1/orders/{id}/state`  
  - Batches: `GET /api/v1/batches` / `GET /api/v1/batches/{id}` / `POST /api/v1/batches` / `PUT /api/v1/batches/{id}` / `DELETE /api/v1/batches/{id}` / `GET /api/v1/batches/user/{userId}`  
- **Perfiles / Usuarios / Roles / Categorías**  
  - `GET /api/v1/users` / `GET /api/v1/users/{userId}`  
  - `PUT /api/v1/profiles/{userId}/personal` / `PUT /api/v1/profiles/{userId}/password` / `PUT /api/v1/profiles/{userId}/business` / `GET /api/v1/profiles/{userId}` / `DELETE /api/v1/profiles/{userId}`  
  - `GET /api/v1/roles` / `GET /api/v1/business-categories`

**Qué se demuestra en el video**  
- Ejecución de requests sobre los endpoints principales con Postman/Swagger.  
- Flujo de autenticación (sign-up / sign-in) y consumo de un endpoint protegido.  
- Creación y consulta de resources claves: supplies, custom-supplies, recipes, orders.  
- Pruebas de cambio de estado en orders y creación de batches.

**Video del Backend (demostración / pruebas):** https://shorturl.at/CZzk9 

![Execution Backend](assets/images/cap4/sprint1/execution/exec2.png)


#### Aplicación Móvil (Administrador de Restaurantes — Android) — Pantallas integradas

**Alcance entregado (Sprint 1)**  
- Desarrollo e integración de las **pantallas core** del flujo administrativo en Android: listas principales, búsquedas y vistas detalle.  
- Conexión parcial con el backend para operaciones de lectura y algunas operaciones CRUD (dependiendo del endpoint).  
- Validaciones visuales y estados básicos (loading, empty state, error).

**Pantallas incluidas (PRIMERA PARTE — ADMIN RESTAURANTES)**

1. **Supplies — Lista y tabla**  
   - Ver lista de supplies (datos desde `GET /api/v1/supplies` y `GET /api/v1/custom-supplies/user/{userId}` según contexto).  
   - Barra de búsqueda con filtros (por categoría: `GET /api/v1/supplies/categories`).  
   - Estado vacío cuando no hay supplies.

2. **Modal / Interfaz CRUD de Supplies**  
   - Modal para crear/editar supplies (consume `POST /api/v1/custom-supplies`, `PUT /api/v1/custom-supplies/{id}`, `DELETE /api/v1/custom-supplies/{id}`).  
   - Alternativa: evaluación sobre si usar modal o pantalla separada según usabilidad.

3. **Recipes — Interfaz y CRUD**  
   - Pantalla de listado `GET /api/v1/recipes`.  
   - Detalle de receta `GET /api/v1/recipes/{id}` y listado de supplies de receta `GET /api/v1/recipes/{id}/supplies`.  
   - Agregar supplies a receta `POST /api/v1/recipes/{id}/supplies`.  
   - Operaciones de creación/edición/eliminación: `POST /api/v1/recipes`, `PUT /api/v1/recipes/{id}`, `DELETE /api/v1/recipes/{id}`.

4. **Sales — Primera parte (lista y búsqueda)**  
   - Lista de sales disponibles (puede implementarse inicialmente con datos estáticos para mostrar UI).  
   - Barra de búsqueda, filtros y mensaje “no hay elementos” cuando esté vacío.  
   - Lista con botón de edición (navega a la segunda parte).

5. **Sales — Segunda parte (CRUD conectado)**  
   - Interfaz y lógica para agregar/actualizar/eliminar una sale, conectada al backend cuando los endpoints estén listos.

**Mapeo rápido: pantallas → endpoints**  
- Lista de Supplies (pantalla) → `GET /api/v1/supplies`, `GET /api/v1/custom-supplies/user/{userId}`  
- Filtros por categoría → `GET /api/v1/supplies/categories`  
- Crear/editar supply (modal) → `POST /api/v1/custom-supplies`, `PUT /api/v1/custom-supplies/{id}`, `DELETE /api/v1/custom-supplies/{id}`  
- Recipes (lista, detalle, modificar) → endpoints bajo `/api/v1/recipes` (ver sección Recipes arriba)  
- Orders / Batches (cuando se integre la gestión de compras) → endpoints bajo `/api/v1/orders` y `/api/v1/batches`  

**Qué se demuestra en el video**  
- Navegación por las pantallas core: lista de supplies, filtro/búsqueda, modal de creación/edición, listado y detalle de recipes.  
- Conexión parcial con el backend: llamadas de lectura y ejemplos de POST/PUT donde se ha integrado.  
- Comportamientos de validación y estados UI (loading / empty / success / error).

**Video de Aplicación Móvil:** https://shorturl.at/8adxX

![Execution Backend](assets/images/cap4/sprint1/execution/exec3.png)


#### 4.2.1.6. Services Documentation Evidence for Sprint Review

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

  
  <tr>
    <td>Segmento 2: Proveedores de Restaurantes</td>
    <td>
      <ul>
        <li>Claridad del valor en el Landing Page.</li>
        <li>Gestión de catálogo de productos.</li>
        <li>Eliminación de insumos no disponibles.</li>
        <li>Revisión de pedidos realizados por restaurantes.</li>
        <li>Interacción con comentarios recibidos.</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Suscripción y pago.</li>
        <li>Registro y gestión de productos en el catálogo.</li>
        <li>Eliminación de insumos.</li>
        <li>Gestión de órdenes recibidas.</li>
        <li>Panel principal del proveedor.</li>
      </ul>
    </td>
    <td>
      <ul>
        <li>Explorar el Landing Page y describir su comprensión del producto.</li>
        <li>Simular el proceso de registro y suscripción.</li>
        <li>Ingresar al sistema y registrar productos en su catálogo.</li>
        <li>Eliminar productos del catálogo.</li>
        <li>Revisar pedidos recibidos de restaurantes.</li>
        <li>Comentar sobre la utilidad de la interfaz de pedidos y feedback.</li>
      </ul>
    </td>
  </tr>
  </tbody>
</table>

**Herramientas y Recursos para Validación**

Formato de Evaluación Heurística: Se aplicarán los 10 principios heurísticos de Nielsen en cada sesión.
Instrumento de observación: Lista de verificación + sección de notas abiertas.
Grabación de pantalla y voz: previa autorización, para análisis posterior.

### 4.3.2. Registro de Entrevistas

A continuación, se presenta el registro correspondiente a la entrevista realizada con un representante del segmento de **proveedores de restaurantes**, quien participó en la validación del **Landing Page** de la plataforma **Restock**. El objetivo fue evaluar la claridad del mensaje, la propuesta de valor y la percepción de utilidad del sistema desde la perspectiva de un proveedor.

#### **Entrevista 01 – Josue Ramírez**

**Datos del entrevistado:**
- **Nombre completo:** Josue Ramírez  
- **Edad:** 26 años  
- **Distrito:** Chorrillos  
- **Segmento:** Proveedor de insumos gastronómicos  
- **Fecha de entrevista:** 07 de octubre de 2025  
- **Duración:** 8 minutos y 58 segundos  
- **Registro audiovisual:**  https://shorturl.at/kaGl4
- **Captura de entrevista:**  
  ![Captura de entrevista a segmento provedores](/assets/images/cap4/sprint1/interviews/int-providers.png)

#### **Resumen descriptivo de la entrevista:**

Durante la sesión, se mostró el **Landing Page de Restock** al entrevistado con el propósito de evaluar su comprensión del producto y su percepción sobre la utilidad para proveedores. Josue Ramírez indicó que el diseño del landing le pareció **claro y profesional**, destacando el mensaje principal que resalta la **conexión directa entre proveedores y administradores de restaurantes**.

Comentó que el apartado de **“gestión de catálogo”** le resultó relevante, ya que permitiría mantener actualizados sus productos sin necesidad de depender de terceros. Asimismo, valoró positivamente la posibilidad de **recibir pedidos en tiempo real y mantener comunicación directa con los restaurantes** mediante la plataforma.

Sin embargo, sugirió que sería útil incluir una sección más visible en el landing donde se expliquen los **beneficios específicos para proveedores**, como métricas de venta o testimonios de otros usuarios. También recomendó que el formulario de registro indique con mayor claridad los **requisitos de verificación** o documentos necesarios.

En general, el entrevistado expresó una **percepción positiva sobre la propuesta de Restock**, considerando que el sistema podría optimizar su relación con los clientes y mejorar la gestión de pedidos y stock de su negocio.

**Conclusión general:**  
La entrevista permitió validar que el mensaje principal del Landing Page es claro y atractivo para el segmento de proveedores. Sin embargo, se identificó la necesidad de reforzar la comunicación de los beneficios específicos para este grupo y mejorar la guía del proceso de registro.


### 4.3.3. Evaluaciones según heurísticas

<table border="1" cellpadding="8" cellspacing="0" width="100%" style="margin-bottom:18px; text-align: center">
  <thead>
    <tr>
      <th style="text-align: center">Segmento</th>
      <th style="text-align: center">Elementos a validar</th>
      <th style="text-align: center">Mobile User Flow</th>
      <th style="text-align: center">Actividades durante la sesión</th>
    </tr>
  </thead>
  <tbody style="text-align: center">
    <tr>
      <td>Segmento 2: Proveedores de Restaurantes</td>
      <td>
        <ul>
          <li>Claridad del mensaje del landing page y valor percibido.</li>
          <li>Facilidad de registro como proveedor.</li>
          <li>Publicación de productos y gestión del catálogo.</li>
          <li>Recepción y actualización de pedidos.</li>
          <li>Comunicación con administradores de restaurantes.</li>
          <li>Visualización de historial de pedidos y métricas de venta.</li>
          <li>Comprensión de alertas y notificaciones del sistema.</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Registro como proveedor.</li>
          <li>Creación y edición de productos en catálogo.</li>
          <li>Recepción de pedidos y confirmación de entrega.</li>
          <li>Gestión de pedidos activos y completados.</li>
          <li>Mensajería con restaurantes asociados.</li>
          <li>Revisión de métricas de desempeño (ventas, entregas, reseñas).</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Explorar el landing page e indicar qué entienden del servicio ofrecido.</li>
          <li>Completar el flujo de registro como proveedor.</li>
          <li>Publicar un nuevo producto y modificar su precio o stock.</li>
          <li>Simular la recepción de un pedido y su actualización de estado.</li>
          <li>Acceder a la bandeja de mensajes y enviar una respuesta a un restaurante.</li>
          <li>Consultar las métricas de ventas y comentar su utilidad.</li>
          <li>Comentar percepciones generales sobre la facilidad de uso y claridad del sistema.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>
