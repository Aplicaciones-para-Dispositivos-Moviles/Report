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
    <td>dsadsadasdasdasdasd</td>
    <td>feat: add representative testimonials section</td>
    <td>04/10/2025</td>
  </tr>
  <tr>
    <td>sergioJM05/restock-landing-page</td>
    <td>feature/questions</td>
    <td>dsadsadasdasdasdasd</td>
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
    <td>dsadsadasdasdasdasd</td>
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

### 4.3.2. Registro de Entrevistas

### 4.3.3. Evaluaciones según heurísticas
