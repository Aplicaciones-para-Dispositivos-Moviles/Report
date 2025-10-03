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
    <td>jahazielgg/restock-landing-page</td>
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
    <td>jahazielgg/restock-landing-page</td>
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

#### 4.2.1.5. Execution Evidence for Sprint Review

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

### 4.3.3. Evaluaciones según heurísticas
