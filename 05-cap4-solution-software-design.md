# Capítulo IV: Solution Software Design

## 4.1. Strategic-Level Domain-Driven Design

### 4.1.1. Event Storming

Para la construccion del Event Storming, se coordinó obtener una primera versión del modelo de dominio del proyecto. Para ello, se siguió un proceso estructurado de 9 etapas.

**Paso 1:** Lluvia de ideas de los eventos del dominio relacionados con el dominio empresarial que se está explorando.

<img src="assets/images/cap4/event_storming/event_storming_1.jpg" alt=“DDD” height="300px">

**Paso 2:** Ordenar los eventos de dominio (definiendo timelines).

<img src="assets/images/cap4/event_storming/event_storming_2.jpg" alt=“DDD” height="300px">

**Paso 3:** Identificar puntos problemáticos (paint points) en el proceso.

<img src="assets/images/cap4/event_storming/event_storming_3.jpg" alt=“DDD” height="300px">

**Paso 4:** Identificar eventos comerciales importantes (pivotal points) que indiquen un cambio en el contexto o fase del negocio.

<img src="assets/images/cap4/event_storming/event_storming_4.jpg" alt=“DDD” height="300px">

**Paso 5:** Definir comandos que desencadenan eventos.

<img src="assets/images/cap4/event_storming/event_storming_5.jpg" alt=“DDD” height="300px">

**Paso 6:**  Definir políticas que desencadenan la ejecución de comandos.

<img src="assets/images/cap4/event_storming/event_storming_6.jpg" alt=“DDD” height="300px">

**Paso 7:**  Identificar read models, los cuales son modelos de lectura o vistas que los usuarios necesitan para tomar.

<img src="assets/images/cap4/event_storming/event_storming_7.jpg" alt=“DDD” height="300px">

**Paso 8:** Identificar sistemas externos que se conectan con el dominio.

<img src="assets/images/cap4/event_storming/event_storming_8.jpg" alt=“DDD” height="300px">

**Paso 9:** Definir aggregates agrupando comandos y eventos relacionados en unidades lógicas.

<img src="assets/images/cap4/event_storming/event_storming_9.jpg" alt=“DDD” height="300px">

#### 4.1.1.1. Candidate Context Discovery

A partir del modelo de Event Storming realizado en Miro, se llevó a cabo una sesión de Candidate Context
Discovery para identificar los bounded contexts de la solución. Se utilizó principalmente la técnica
look-for-pivotal-events durante la sesión.

Primero, se buscaron eventos clave que indiquen cambios de estado entre diferentes partes del proceso del negocio:

<img src="assets/images/cap4/event_storming/event_storming_bc_paso1.jpg" alt=“DDD” height="300px">

Luego, se agruparon los eventos de acuerdo a los principales cambios de contexto.

<img src="assets/images/cap4/event_storming/event_storming_bc_paso2.jpg" alt=“DDD” height="300px">

Se trazaron fronteras alrededor de los grupos identificados, estableciendo los límites iniciales de los bounded contexts.

<img src="assets/images/cap4/event_storming/event_storming_bc_paso3.jpg" alt=“DDD” height="300px">

Finalmente, se seleccionaron nombres para los bounded context. Dando como resultado la definición de 6 bounded contexts y la **versión final del Event Storming**:

<img src="assets/images/cap4/event_storming/event_storming_general.jpg" alt=“DDD”>

A continuación, se explicará en qué consiste cada bounded context:

**Identity and Access Management:** También llamado "IAM", este bounded context contiene el proceso de ingreso del usuario a la plataforma, ya sea iniciando sesión o registrandose.

<img src="assets/images/cap4/event_storming/event_storming_bc_iam.png" alt=“DDD” height="300px">

**Subscriptions and Payments:** También llamado "Subscription", este bounded context contiene el proceso de suscribirse a uno de los planes en la plataforma y pagar por dicho plan.

<img src="assets/images/cap4/event_storming/event_storming_bc_subscription.png" alt=“DDD” height="300px">

**Profiles and Preferences:** También llamado "Profile", este bounded context contiene el proceso de configuración de datos personales en el perfil.

<img src="assets/images/cap4/event_storming/event_storming_bc_profile.png" alt=“DDD” height="300px">

**Asset and Resource Management:** También llamado "Resource", este bounded context contiene el proceso de gestionar los insumos en el inventario y realizar pedidos a un proveedor.

<img src="assets/images/cap4/event_storming/event_storming_bc_resource.png" alt=“DDD” height="300px">

**Service Design and Planning:** También llamado "Planning", este bounded context contiene el proceso de diseñar/crear una nueva receta en base a los insumos registrados en el inventario.

<img src="assets/images/cap4/event_storming/event_storming_bc_planning.png" alt=“DDD” height="300px">

**Service Operation and Monitoring:** También llamado "Monitoring", este bounded context contiene el proceso de registrar una nueva venta del administrador de restaurante y el proceso de gestionar las órdenes que recibe un proveedor.

<img src="assets/images/cap4/event_storming/event_storming_bc_monitoring.png" alt=“DDD” height="300px">

#### 4.1.1.2. Domain Message Flows Modeling

Los Domain Message Flows modelan las interacciones entre los diferentes bounded contexts, mostrando cómo se comunican entre sí mediante comandos, eventos y consultas. A continuación, se muestran los flujos de mensaje para los escenarios clave del negocio:

* **Acceso a la plataforma:** En este flujo se muestra la interacción entre el bounded context IAM y el bounded context Profile al momento en que un usuario accede a la plataforma.

  <img src="assets/images/cap4/message_flows/message_flow_access.jpg" alt=“DDD” height="500px">
* **Registrar una receta:** En este flujo se muestra la interacción entre el bounded context Planning y el bounded context Resource al momento en que un administrador de restaurante registra una receta.

  <img src="assets/images/cap4/message_flows/message_flow_recipe.jpg" alt=“DDD” height="500px">
* **Realizar un pedido a un proveedor:** En este flujo se muestra la interacción entre el bounded context Resource y el bounded context Monitoring al momento en que un administrador de restaurante solicita un pedido a un proveedor.

  <img src="assets/images/cap4/message_flows/message_flow_order.jpg" alt=“DDD” height="500px">
* **Registrar una venta y actualizar el inventario:** En este flujo se muestra la interacción entre el bounded context Monitoring y el bounded context Resource al momento en que un administrador de restaurante registra una nueva venta y actualiza su inventario.

  <img src="assets/images/cap4/message_flows/message_flow_sale.jpg" alt=“DDD” height="500px">

Adicionalmente, se presentan flujos de escenarios relevantes para los usuarios, pero en los que no se produce interacción entre distintos bounded contexts:

* **Suscripción a un plan:** En este flujo se muestra el proceso mediante el cual un usuario se suscribe a un plan, modelado en el bounded context Subscription and Payments.

  <img src="assets/images/cap4/message_flows/message_flow_subscribe.jpg" alt=“DDD” height="500px">
* **Registrar un insumo en el inventario:** En este flujo se modela el proceso mediante el cual un usuario registra un insumo en su inventario, modelado en el bounded context Asset and Resource Management.

  <img src="assets/images/cap4/message_flows/message_flow_supply.jpg" alt=“DDD” height="500px">

#### 4.1.1.3. Bounded Context Canvases

### 4.1.2. Context Mapping

En esta sección se explica el proceso de elaboración de los contexts maps. Asimismo, se permite la visualizacón de las relaciones estructurales entre vounded contexts, junto a los patrones de relaciones entre Bounded contexts establecidos en Domain Driven Design, como Anti-corruption Layer, Conformist, Customer/Supplier ó Shared Kernel.

Posterior al debate grupal para la contextualización del proyecto, nos hemos proyectado los siguientes Bounded context:

- Profiles and Preferences (PAP)
- Identity and Access Management (IAM)
- Subscriptions and Payments (SAP)
- Assets and Resource Management (ARM)
- Service Design and Planning (SDP)
- Service Operation and Monitoring (SOM)

### *Profiles and Preferences(PAP) - Identity and Access Management (IAM)*

![pap-iam](assets/images/cap4/context_mapping/pap-iam.png)
En la presente imagen se puede identificar la relación entre Profiles and preferences(PAP) e Identity and Access Management (IAM), los cuales están enfocados en lógicas similares y comparten un subconjunto del modelo de dominio común para evitar la duplicación de código y lógica.
***Profiles and Preferences (PAP)***:
Está enfocada en el listado de accesos y la segmentación de usuarios, ya que nuestro producto está en un contexto de cliente - administrador. De esta manera, se reutiliza (Shared kernel) el modelo de "usuario", el cual comparte logica con cliente y adminsitrador.
***Identity and Access Management (IAM)***:
Está enfocada en la administración y validación de acceso al sistema. Asimismo, comprende la verificacion de usuario con user y contraseña. De esta manera, también se reutiliza (Shared Kernel) la lógica de un usuario.

### *Identity and Access Management (IAM) - Subscriptions and Payments (SAP)*

![iam-sap](assets/images/cap4/context_mapping/iam-sap.png)
En la presente imagen se puede identificar la relación entre Identity and Access Management (IAM) y subscriptions and payments (SAP), los cuales está enfocada en la comunicación por medio de un acl hacia subscriptions and payment por el uso Stripe como servicio externo que se comunica por medio de OSH y Pl el cual permite la comunicacion entre contextos y la definición de servicios.

***Identity and Access Management (IAM)***:
Está enfocada en la administración, validación y actualización de datos en el acceso al sistema. Asimismo, comprende la verificacion de usuario con user, contraseña y pago por medio de stripe.

***Subscriptions and Payments (SAP)***
Está enfocada en la validación y proceso de pagos, a través de las subscripciones existentes. De esta manera, por medio de Stripe, se puede validar e influenciar en otros bounded contexts.

### *Subscriptions and Payments (SAP) - Assets and Resource Management (ARM)*

![sap-asm](assets/images/cap4/context_mapping/sap-arm.png)
En la presente imagen se puede identificar la relación entre Subscriptions and Payments (SAP) y Assets and Resource Management (ASM) por medio del patrón Customer / Supplier. Ya que el bounded context ASM actúa o se activa bajo influencia de subscripcions and payments, el cual genera una dependecia enntre estos dos bounded contexts.

***Subscriptions and Payments (SAP)***:
Está enfocada en la validación y proceso de pagos, a través de las subscripciones existentes. De esta manera, por medio de Stripe, se puede validar e influenciar en otros bounded contexts.

***Assets and Resource Management (ARM)***
Está enfocada en la gestión y permisos de inventario, de manera que depende de una subscripción para poder ser usado.

### *Assets and Resource Management (ARM) - Service Design and Planning (SDP)*

![arm-sdp](assets/images/cap4/context_mapping/arm-sdp.png)
En la presente imagen se puede identificar el patrón partnership porque existe un trabajo coordinado entre estos dos boundeds contexts.
***Assets and Resource Management (ARM)***
Está enfocada en la gestión y permisos de inventario.

***Service Design and Planning (SDP)***
Está enfocado en la creación de recetas, y trabaja junto a Assets and Resource Management por el inventario que se actualiza constantemente

### *Service Design and Planning (SDP) - Service Operation and Monitoring (SOM)*

![sdp-som](assets/images/cap4/context_mapping/sdp-som.png)
En la presente imagen se puede identificar el patron conformista de manera que el downstream adopta el modelo del upstream tal cual. Y las ventas son dependientes a las recetgas.

***Service Design and Planning (SDP)***
Está enfocado en la creación de recetas, y trabaja junto a Assets and Resource Management.

***Service Operation and Monitoring(SDM)***
Es un bounded context con relación conformista. Ya que el bounded context Service Operation and Monitoring(SDM) solo recibe parte de las recetas, y de esta manera es influenciado por SDP.

### *Final Context Map*

![main-context-map](assets/images/cap4/context_mapping/main_context_map.png)

### 4.1.3. Software Architecture

Esta sección aplica el *C4 Model* en dos niveles: **Context** (visión externa / de alto nivel) y **Container** (visión interna / de alto nivel técnico). Se explica cada diagrama y se justifican las decisiones tecnológicas principales.

#### 4.1.3.1. Software Architecture Context Level Diagrams

![Figura 4.1 - Context Diagram](assets/images/cap4/software_architecture/context.png)

El Context Diagram muestra **Restock** como un recuadro central con dos actores (Administrador y Proveedor) y los servicios externos principales alrededor (Stripe, SendGrid, Push, Cloudinary). Su propósito es dejar claro el alcance del sistema: todo lo que está dentro del recuadro es responsabilidad del equipo; pagos, email, push y media se delegan a terceros.

#### 4.1.3.2. Software Architecture Container Level Diagrams

![Figura 4.2 - Container Diagram](assets/images/cap4/software_architecture/container.png)

El Container Diagram descompone Restock en: apps móviles (Android para administradores, Flutter para proveedores), y los containers backend por bounded context (IAM, Subscription, Profile, Resource, Planning, Monitoring). También muestra la persistencia (MongoDB) y las integraciones externas.

**Decisiones tecnológicas principales (bullet points, muy breves)**

- **Mobile first**: Android nativo (Kotlin) para administradores; Flutter (Dart) para proveedores.
- **Backend**: microservicios por bounded context con **Java + Spring Boot** (REST).
- **Persistencia**: **MongoDB** (schema flexible para insumos/recetas).
- **Integraciones**: **Stripe** (pagos), **SendGrid** (emails), **OneSignal/FCM** (push), **Cloudinary** (medios).
- **Autenticación**: IAM emite JWT; los servicios validan tokens para evitar consultas síncronas constantes.

#### 4.1.3.3. Software Architecture Deployment Diagrams

A continuación se presentan los diagramas de despliegue para el sistema a implementar, los cuales muestran cómo se distribuirán los diferentes componentes del sistema en la infraestructura y otros entornos. Este diagrama visualiza la interacción entre los diferentes servicios y bases de datos, así como su implementación en contenedores y máquinas virtuales. El principal objetivo de estos diagramas es proporcionar una visión clara de la arquitectura del sistema y facilitar su implementación y mantenimiento.

<img src="assets/uml/software-deployment-diagram.png" alt=“DDD” height="400px">

## 4.2. Tactical-Level Domain-Driven Design

### 4.2.1. Bounded Context: Identity and Access Management

### 4.2.1.1. Domain Layer

### 4.2.1.2. Interface Layer

### 4.2.1.3. Application Layer

### 4.2.1.4. Infrastructure Layer

### 4.2.1.5. Bounded Context Software Architecture Component Level Diagrams

### 4.2.1.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.1.6.1. Bounded Context Domain Layer Class Diagrams

##### 2.6.1.6.2. Bounded Context Database Design Diagram

### 4.2.2. Bounded Context: Subscriptions and Payments

#### 4.2.2.1. Domain Layer

#### 4.2.2.2. Interface Layer

#### 4.2.2.3. Application Layer

#### 4.2.2.4. Infrastructure Layer

#### 4.2.2.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.2.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.2.6.1. Bounded Context Domain Layer Class Diagrams

##### 2.6.2.6.2. Bounded Context Database Design Diagram

#### 4.2.3. Bounded Context: Profiles and Preferences

#### 4.2.3.1. Domain Layer

#### 4.2.3.2. Interface Layer

#### 4.2.3.3. Application Layer

#### 4.2.3.4. Infrastructure Layer

#### 4.2.3.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.3.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.3.6.1. Bounded Context Domain Layer Class Diagrams

##### 2.6.3.6.2. Bounded Context Database Design Diagram

#### 4.2.4. Bounded Context: Asset and Resource Management

#### 4.2.4.1. Domain Layer

#### 4.2.4.2. Interface Layer

En esta capa se definen los puntos de entrada/salida del sistema y cómo se exponen los casos de uso a clientes externos (front-end, integraciones en la app móvil). Aquí se transforman solicitudes HTTP (o mensajes) en comandos/consultas hacia la *Application Layer* y mapear las respuestas del dominio a objetos aptos para transporte (DTOs).

Controllers (REST):

* `BatchController`: Administra las operaciones relacionadas con los  batches de inventario. Endpoints trabajados:

  * **GET** `/api/v1/batches` → listar batches.
  * **GET** `/api/v1/batches/{id}` → obtener detalle de un batch.
  * **POST** `/api/v1/batches` → registrar un nuevo batch.
  * **PUT/PATCH** `/api/v1/batches/{id}` → actualizar información de un batch.
  * **DELETE** `/api/v1/batches/{id}` → eliminar un batch.
* `CustomSupplyController`: Gestiona los insumos personalizados que un usuario puede registrar como suyos fuera del catálogo general.

  * **GET** `/api/v1/custom-supplies` → listar insumos personalizados.
  * **GET** `/api/v1/custom-supplies/{id}` → detalle de un insumo personalizado.
  * **POST** `/api/v1/custom-supplies` → crear un nuevo insumo personalizado.
  * **PUT/PATCH** `/api/v1/custom-supplies/{id}` → actualizar datos del insumo.
  * **DELETE** `/api/v1/custom-supplies/{id}` → eliminar insumo.
* `OrderController`: Expone los casos de uso vinculados a las órdenes de pedido y a los  batches asociados a una orden. Endpoints trabajados:

  * **GET** `/api/v1/orders/{orderId}` → obtener orden por Id.
  * **GET** `/api/v1/orders` → listar todas las órdenes
  * **GET** `/api/v1/orders/{orderId}/batches` → listar batches asociados a la orden.
  * **GET** `/api/v1/orders/{orderId}/custom-supplies` → listar insumos personalizados asociados a la orden.
  * **GET** `/api/v1/orders/{orderId}/requested-batches` → listar requested batches de la orden.
  * **GET** `/api/v1/orders/{orderId}/supplies` → listar supplies relacionados a la orden.
  * **POST** `/api/v1/orders` → crear una nueva orden.
  * **PUT** `/api/v1/orders/{orderId}` → actualizar datos de la orden.
  * **DELETE** `/api/v1/orders/{orderId}` → eliminar una orden.
  * **PUT** `/api/v1/orders/{orderId}/requested-batches/{batchId}` → actualizar un requested batch de la orden.
  * **POST** `/api/v1/orders/{orderId}/requested-batches` → agregar requested batches a la orden.
  * **POST** `/api/v1/orders/{orderId}/approvals` → aprobar una orden.
  * **POST** `/api/v1/orders/{orderId}/declines` → rechazar una orden.
  * **POST** `/api/v1/orders/{orderId}/cancellations` → cancelar una orden.
  * **POST** `/api/v1/orders/{orderId}/preparing` → marcar orden como “Preparing.
  * **POST** `/api/v1/orders/{orderId}/on-the-way` → marcar orden como “On The Way.
  * **POST** `/api/v1/orders/{orderId}/delivered` → marcar orden como “Delivered.
* `SupplyController`: Se encarga de las consultas y operaciones sobre el  catálogo general de insumos. Endpoints trabajados:

  * **GET** `/api/v1/supplies` → listar insumos del catálogo.
  * **GET** `/api/v1/supplies/{id}` → obtener detalle de un insumo.
  * **POST** `/api/v1/supplies` → registrar un nuevo insumo en el catálogo.
  * **PUT/PATCH** `/api/v1/supplies/{id}` → actualizar un insumo.
  * **DELETE** `/api/v1/supplies/{id}` → eliminar insumo.
  * **GET** `/api/v1/supplies/categories` → listar categorías únicas de insumos.

Todos estos controller trabajan con Resources (DTOs / Request & Response Models) y Assemblers/Mappers para el procesamiento de datos, los cuales son:

* **Resources (DTOs / Request & Response Models)**

  * **AddOrderToSupplierBatchResource** → request para agregar requested batches a una orden.
  * **BatchResource** → response con datos de un batch.
  * **CreateBatchResource** → request para crear un batch.
  * **CreateCustomSupplyResource** → request para crear un insumo personalizado.
  * **CreateOrderResource** → request para crear una orden.
  * **CustomSupplyResource** → response con datos de un insumo personalizado.
  * **OrderResource** → response con datos de una orden.
  * **OrderToSupplierBatchResource** → response de un *requested batch* en la orden.
  * **SupplyResource** → response con datos de un insumo del catálogo.
  * **UpdateBatchResource** → request para actualizar un batch.
  * **UpdateCustomSupplyResource** → request para actualizar un insumo personalizado.
  * **UpdateOrderResource** → request para actualizar datos de una orden.
  * **UpdateOrderToSupplierBatchResource** → request para actualizar un requested batch en la orden.
  * 
* **Assemblers / Transform**

  Encapsulan la conversión entre el mundo externo (Resources/DTOs) y el interno (Commands/Queries/Domain). Reducen acoplamiento y duplicación.

  * **AddOrderToSupplierBatchFromResourceAssembler** → resource → command para agregar  *requested batches* .
  * **BatchResourceFromEntityAssembler** → entity → resource para batch.
  * **CreateBatchCommandFromResourceAssembler** → resource → command para crear un batch.
  * **CreateCustomSupplyCommandFromResourceAssembler** → resource → command para crear un insumo personalizado.
  * **CreateOrderCommandFromResourceAssembler** → resource → command para crear una orden.
  * **CustomSupplyResourceFromEntityAssembler** → entity → resource para insumo personalizado.
  * **OrderResourceFromEntityAssembler** → entity → resource para orden.
  * **OrderToSupplierBatchResourceFromEntityAssembler** → entity → resource para  *requested batch* .
  * **SupplyResourceFromEntityAssembler** → entity → resource para insumo del catálogo.
  * **UpdateBatchCommandFromResourceAssembler** → resource → command para actualizar un batch.
  * **UpdateCustomSupplyCommandFromResourceAssembler** → resource → command para actualizar un insumo personalizado.
  * **UpdateOrderCommandFromResourceAssembler** → resource → command para actualizar una orden.
  * **UpdateOrderToSupplierBatchCommandFromResourceAssembler** → resource → command para actualizar un  *requested batch* .

### 4.2.4.3. Application Layer

En esta capa se coordinan las interacciones entre las capas de dominio y la infraestructura, asegurando que el comportamiento del sistema sea correcto y eficiente en función de los requerimientos del negocio.

Se dividen principalmente en 3 tipos de clases:

**1. Command Handlers**

Se encargan de procesar comandos y actúan sobre el dominio. Tenemos:

- **`BatchCommandHandler`**: Maneja los comandos relacionados con la operación de insumos registrados en el inventario (batch). Permite validar, agregar, eliminar y actualizar la información de un batch.
- **`CustomSupplyCommandHandler`**: Aquí se gestionan los comandos específicos para el abastecimiento personalizado de insumos. Permite validar, agregar, eliminar y actualizar la información de un insumo propio.
- **`OrderBatchCommandHandler`**: Esta clase se ocupa de gestionar los comandos relacionados a un batch solicitado en una orden, tales como su creación, actualización y eliminación.
- **`OrderCommandHandler`**: Esta clase se ocupa de gestionar los comandos de órdenes, asegurando que los pedidos sean procesados correctamente dentro del sistema. Permite crear una orden, actualizarla y eliminarla, así como aprobarla, cancelarla o rechazarla. También, agregar un batch a la orden, actualizar el valor de un batch y cambiar el estado de una orden.
- **`SupplyCommandHandler`**: Esta clase se ocupa de gestionar los comandos relacionados a un insumo del catalogo de insumos que se maneja en la aplicación. Permite cargar la data inicial del catálogo de insumos mediante un comando seed.

**2. Event Handlers**

Se encargan de escuchar y reaccionar a eventos generados por el sistema, ejecutando acciones específicas sobre el dominio. En este caso contamos con:

* **`ResourceApplicationReadyEventHandler`** : Esta clase se encarga de escuchar el evento **`ApplicationReadyEvent`** (disparado cuando la aplicación inicia correctamente). Su función es inicializar el catálogo de insumos llamando al servicio de comandos de insumos ( **`SupplyCommandService`** ) mediante el comando  **`SeedSuppliesCommand`** . De esta forma, asegura que al inicio de la aplicación se realice automáticamente la carga inicial de datos en el sistema.

**3. Query Handlers**

Se encargan de resolver consultas del sistema. Tenemos:

* **`BatchQueryHandler`**: Gestiona consultas relacionadas con los batches registrados en el inventario. Permite obtener información detallada de los batches disponibles, sus atributos y estado actual.
* **`CustomSupplyQueryHandler`** : Maneja las consultas sobre insumos personalizados registrados por los usuarios. Permite listar, buscar y detallar la información de un insumo propio dentro del sistema.
* **`OrderBatchQueryHandler`** : Atiende las consultas vinculadas a los batches asociados a una orden. Proporciona información como los batches agregados, sus cantidades y valores en el contexto de la orden.
* **`OrderQueryHandler`** : Responde a las consultas sobre órdenes en general. Permite obtener una orden por su identificador, listar todas las órdenes, consultar su estado y los datos asociados a cada pedido.
* **`SupplyQueryHandler`** : Gestiona las consultas sobre el catálogo de insumos del sistema. Permite acceder a la lista completa de insumos, buscar por criterios y obtener categorías únicas, facilitando la navegación y filtrado en la aplicación.

### 4.2.4.4. Infrastructure Layer

#### 4.2.4.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.4.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.4.6.1. Bounded Context Domain Layer Class Diagrams

##### 2.6.4.6.2. Bounded Context Database Design Diagram

### 4.2.5. Bounded Context: Service Design and Planning

Este BC diseña y planifica el catálogo de recetas (platos del menú) y su composición de insumos; exponer una grilla de menús para operación y ventas.

**Relaciones con otros BCs:**

* Resource (Inventario): upstream para consultar/validar insumos y downstream para descontar inventario cuando una receta es consumida.
* Monitoring (Ventas): emite eventos de venta de platos. SDP consume esos eventos para generar la orden de consumo de insumos hacia Resource.

ACL: se implementa un Anti-Corruption Layer para traducir términos/IDs entre SDP y Resource/Monitoring (evita que modelos externos contaminen el dominio de SDP).

Lenguaje ubicuo (Ubiquitous Language): Recipe, RecipeIngredient, Supply, Quantity, Price, Menu Grid, Sale/Consumption.

**Políticas clave:**

Una Recipe no es consumible si cualquiera de sus RecipeIngredients (insumos requeridos) no existe o su Quantity ≤ 0.

La consumición de una Recipe sólo procede si Resource confirma stock suficiente (consistencia eventual con reserva/confirmación).

Una Recipe confirmada mantiene invariantes: nombre no vacío; precio ≥ 0; cada item con cantidad > 0; sin duplicados de insumo.

#### 4.2.5.1. Domain Layer

**Aggregates:**

* Recipe (Aggregate Root)

  * Atributos: RecipeId, Name, Price, Items: List`<RecipeIngredient>`, Status (Draft|Active|Archived), Audit (createdBy, createdAt, …).
  * Invariantes:

    * Name no vacío; Price >= 0.
    * Items no vacía cuando Status = Active.
    * Cada RecipeIngredient.Quantity > 0.
    * No hay dos RecipeIngredient con el mismo SupplyId.
  * Comportamientos:

    * addItem(SupplyId, Quantity) (merge quantities si ya existe).
    * updateItemQuantity(SupplyId, Quantity) (revalida invariantes).
    * removeItem(SupplyId) (no permite quedar vacía si está Active).
    * activate() / archive().

**Entities & Value Objects:**

* RecipeIngredient (VO embebido):

  * SupplyId (referencia externa a Resource), Quantity (decimal > 0, p.ej. kg, L, unid), Unit (opcional, si aplica).
  * Validación: Quantity > 0; SupplyId no nulo.
* Price (VO opcional)

  * amount (decimal >= 0), currency (ISO).
* Quantity (VO)

  * value (decimal > 0), unit (enum opcional).

**Domain Services (reglas que no encajan en una sola entidad)**

* RecipeConsumptionPolicy: Dado un Recipe y una solicitud de consumo (de Monitoring), produce el pedido de descuento a Resource (lista de {SupplyId, Quantity}), aplicando transformaciones de unidades/redondeos si fuese necesario.
* RecipeValidationService: Verifica existencia y vigencia de SupplyId en Resource (vía ACL), antes de activar una receta.

**Factories:**

* RecipeFactory:

  * create(name, price, items?) → Recipe(Draft) (permite crear en Draft incluso sin items; al activar se exige items válidos).

**Domain Events (propios de Service Design and Planning)**

* RecipeCreated {recipeId, name}
* RecipeUpdated {recipeId, changedFields}
* RecipeActivated {recipeId} / RecipeArchived {recipeId}
* RecipeConsumptionRequested {recipeId, saleId, lines: [{supplyId, qty}]} (emitido hacia Resource tras evento de venta de Monitoring, vía Application)
* RecipeConsumptionRejected {recipeId, saleId, reason} (si Resource niega stock)
* RecipeConsumptionCommitted {recipeId, saleId}

**Repositories (interfaces del dominio)**

    interface RecipeRepository {
        fun findById(id: RecipeId): Recipe?
        fun findByName(name: String): Recipe?
        fun save(recipe: Recipe): Unit
        fun delete(id: RecipeId): Unit
        fun search(filter: RecipeFilter, page: Int,
        size: Int): Paged`<Recipe>`
    }

Queries complejas para grilla (búsqueda por nombre, rango de precio, estado) se modelan con Specifications/Filters.

#### 4.2.5.2. Interface Layer

**Usuarios:** Restaurant Administrators (Android).

**Pantallas principales (Android):**

* Menu Grid (RecipeListScreen): grid de recetas con búsqueda/orden y estados (Active/Archived).
* Recipe Editor (RecipeEditorScreen): crear/editar nombre, precio e items (selector de Supply remoto con ACL a Resource).
* Recipe Details: vista de receta con lista de insumos y validaciones.
* Activation Flow: activar/archivar con confirmaciones e impactos.

**Controladores/Consumers (frontera de la app móvil):**

* Controllers (Activities/Fragments) + ViewModels (invocan casos de uso de Application).
* Consumers de notificaciones: para feedback de consumo (p.ej., cuando Resource confirma/rechaza consumo post-venta).

**Controllers:**

* RecipeController
  * Responsabilidad: frontera HTTP para CRUD y ciclo de vida de recetas.
  * Colabora con: CreateRecipeHandler, SearchRecipesHandler, GetRecipeByIdHandler, ActivateRecipeHandler, ArchiveRecipeHandler.

#### 4.2.5.3. Application Layer

**Capabilities (casos de uso):**

* Commands (mutaciones):

  * CreateRecipeCommand {name, price, currency}
  * AddRecipeIngredientCommand {recipeId, supplyId, qty, unit?}
  * UpdateRecipeIngredientQuantityCommand {recipeId, supplyId, qty}
  * RemoveRecipeIngredientCommand {recipeId, supplyId}
  * ActivateRecipeCommand {recipeId} / ArchiveRecipeCommand {recipeId}
  * (Opcional) RenameRecipeCommand, UpdateRecipePriceCommand
* Queries (lecturas):

  * GetRecipeByIdQuery {recipeId}
  * SearchRecipesQuery {text?, status?, minPrice?, maxPrice?, page, size}

**Command Handlers (ejemplos):**

* CreateRecipeHandler: valida nombre/price, crea Recipe(Draft), emite RecipeCreated.
* AddRecipeIngredientHandler: carga aggregate, agrega/merge item, revalida invariantes, save.
* ActivateRecipeHandler: llama a RecipeValidationService (consulta a Resource vía ACL para validar supplies); si ok → activate() → RecipeActivated.

**Event Handlers (integración con Monitoring/Resource):**

* OnSaleRegistered (de Monitoring, externo):

  * Verifica recipeId involucrados.
  * Usa RecipeConsumptionPolicy para construir RecipeConsumptionRequested.
  * Publica evento a Resource (MessageBroker).
* OnInventoryConsumptionConfirmed/Rejected (de Resource, externo):

  * Publica RecipeConsumptionCommitted o RecipeConsumptionRejected (para auditoría/UX).

#### 4.2.5.4. Infrastructure Layer

**Persistencia (Backend NoSQL – MongoDB):**
Colección recipes (un documento por aggregate):

```json
{
  "_id": "recipeId",
  "name": "Spaghetti Carbonara",
  "price": { "amount": 12.5, "currency": "USD" },
  "items": [
    { "supplyId": "supply1", "quantity": 0.2, "unit": "kg" },
    { "supplyId": "supply2", "quantity": 0.1, "unit": "L" }
  ],
  "status": "Active",
  "audit": { "createdBy": "...", "createdAt": "...", ... }
}
```

**Repositorios (implementación):**

* RecipeRepository (mapea Aggregate ↔ documento embebido).

**Mensajería / Integraciones:**

* MessageBroker:

  * Tópico de entrada (desde Monitoring): sales.registered.
  * Tópicos de salida (hacia Resource): inventory.consumption.requested, inventory.consumption.compensate.
  * Tópicos de confirmación (desde Resource): inventory.consumption.confirmed/rejected.

#### 4.2.5.5. Bounded Context Software Architecture Component Level Diagrams

#### 4.2.5.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.5.6.1. Bounded Context Domain Layer Class Diagrams

<img src="assets/images/cap4/class_diagram/dc-web-planning.png" alt=“DDD” height="400px">

##### 4.2.5.6.2. Bounded Context Database Design Diagram

<img src="assets/images/cap4/db_diagram/db_planning.png" alt=“DDD” height="400px">

### 4.2.6. Bounded Context: Service Operation and Monitoring (SOM)

Este BC opera y monitorea el día a día en dos frentes:

1. **Ventas** registradas por *restaurant administrators*.
2. **Órdenes de proveedor** gestionadas por *suppliers* (ciclo PO: crear→aprobar→enviar→recibir).

**Relaciones con otros BCs:**

* **SDP (Service Design & Planning):** usa `recipeId` y `price` vigentes; tras una venta SOM **publica** `SaleRegistered` y SDP deriva el consumo de insumos.
* **Resource (Inventario):** recibe `GoodsReceiptPosted` (aumentos) y confirma/alerta niveles (bajo stock); confirma/rehúsa descuentos por consumo.

**ACL:** traduce ids/unidades con SDP/Resource; todas las cantidades viajan en **unidad base** del supply.

**Lenguaje ubicuo:** *Sale, SaleLine, AdditionalSupply, Ticket, PurchaseOrder (PO), POLine, Supplier*.

**Políticas clave**

* **Sale**: cantidades > 0; totales coherentes; **snapshot** de precio/nombre de receta al momento de la venta.

#### 4.2.6.1. Domain Layer

**Aggregates**

* **Sale** *(Aggregate Root)*

  * **Atributos:** SaleId, adminRestaurantId, dinerName?, occurredAt, currency,
    recipeLines: List<RecipeLine>, additionalSupplies: List<SupplyLine>,
    totals {subtotal, tax, total}, status (Registered|Voided|Refunded),
    inventoryApplied: Boolean, audit.
  * **Invariantes:** cantidades > 0; total = Σ lineTotal; estados consistentes.
  * **Comportamientos:** register(...), void(reason), markInventoryApplied().

* **PurchaseOrder** *(Aggregate Root)*

  * **Atributos:** PurchaseOrderId, supplierId, orderedAt, expectedAt?,
    lines: List<POLine>, receipts: List<GoodsReceipt>, status, audit.
  * **Comportamientos:** addLine(...), submit(), approve(), send(), receive(lines), cancel().

**Entities & Value Objects**

* RecipeLine (VO): { recipeId, recipeName_snapshot, unitPrice_snapshot: Money, quantity: Decimal, lineTotal: Money }.
* SupplyLine (VO): { supplyId, quantity: Decimal } *(unidad base de Resource; sin unit en SOM)*.
* PurchaseOrderLine (VO): { supplyId, quantity: Decimal, unitPrice?: Money, currency }.
* GoodsReceipt (Entity): { receiptId, receivedAt, lines[{ supplyId, receivedQty: Decimal }] }.
* Money(amount: Decimal128, currency), Quantity(Decimal128).


**Domain Events (SOM)**

* SaleRegistered {saleId, occurredAt, recipeLines[], additionalSupplies[], totals}
* SaleVoided {saleId, reason}
* InventoryAppliedForSale {saleId}
* PurchaseOrderCreated|Submitted|Approved|Sent
* GoodsReceiptPosted {poId, receiptId, lines[]}

**Repositories (interfaces)**

```kotlin
interface SaleRepository {
  fun findById(id: SaleId): Sale?
  fun save(sale: Sale)
  fun search(filter: SaleFilter, page: Int, size: Int): Paged<Sale>
}
interface PurchaseOrderRepository {
  fun findById(id: PoId): PurchaseOrder?
  fun save(po: PurchaseOrder)
  fun search(filter: PoFilter, page: Int, size: Int): Paged<PurchaseOrder>
}
```

#### 4.2.6.2. Interface Layer

**Usuarios / plataformas**

* *Restaurant Admin* → **Android** (ventas, reportes, POs).
* *Supplier* → **Flutter** (inbox de PO, confirmar envío/entrega).

**Controllers (HTTP – REST)**

* **SalesController**
* **PurchaseOrdersController**

**Consumers (mensajería)**

* InventoryConfirmationsConsumer (Resource: inventory.consumption.confirmed|rejected) → marca inventoryApplied.
* InventoryAlertsConsumer (Resource: inventory.low) → crea/actualiza alertas en UI.

#### 4.2.6.3. Application Layer

**Commands**

* RegisterSaleCommand { dinerName?, adminRestaurantId, occurredAt, currency, recipeLines[{recipeId, quantity}], additionalSupplies[{supplyId, quantity}] }
* VoidSaleCommand { saleId, reason }
* CreatePoCommand { supplierId }, AddPoLineCommand { ... }, SubmitPoCommand, ApprovePoCommand, SendPoCommand, PostGoodsReceiptCommand {poId, lines[{supplyId, receivedQty}]}

**Queries**

* GetSaleByIdQuery, SearchSalesQuery, SalesSummaryQuery, TopRecipesQuery
* GetPurchaseOrderByIdQuery, SearchPurchaseOrdersQuery

**Handlers (ejemplos)**

* RegisterSaleHandler: valida líneas, calcula totales, persiste, **emite SaleRegistered** y despacha consumo (SDP/Resource).


#### 4.2.6.4. Infrastructure Layer

**Colecciones:**

* **sales** — *Aggregate = 1 documento; reemplaza “sales\_recipes” y “sales\_additionalSupplies” con arrays embebidos*:

```json
{
  "_id": "sale_01JKM...",
  "adminRestaurantId": "rest_123",
  "dinerName": "Mesa 5",
  "occurredAt": "2025-09-10T13:15:00Z",
  "currency": "PEN",
  "recipeLines": [
    { "recipeId": "rec_01HZY...", "recipeName_snapshot": "Lomo Saltado",
      "unitPrice_snapshot": { "$numberDecimal": "28.90" },
      "quantity": { "$numberDecimal": "2" },
      "lineTotal": { "$numberDecimal": "57.80" }
    }
  ],
  "additionalSupplies": [
    { "supplyId": "sup_extra_napkins", "quantity": { "$numberDecimal": "3" } }
  ],
  "totals": {
    "subtotal": { "$numberDecimal": "57.80" },
    "tax":      { "$numberDecimal": "10.40" },
    "total":    { "$numberDecimal": "68.20" }
  },
  "status": "Registered",
  "inventoryApplied": false,
  "audit": { "createdBy": "admin_1", "createdAt": "2025-09-10T13:15:01Z" }
}
```

* **purchase_orders** — *Aggregate con líneas y recepciones embebidas*:

```json
{
  "_id": "po_2025_001",
  "supplierId": "sup_ABC",
  "orderedAt": "2025-09-10T09:00:00Z",
  "expectedAt": "2025-09-12T18:00:00Z",
  "status": "Sent",
  "lines": [
    { "supplyId": "sup_beef_topside", "quantity": { "$numberDecimal": "15.0" },
      "unitPrice": { "$numberDecimal": "18.50" }, "currency": "PEN" }
  ],
  "receipts": [
    { "receiptId": "gr_01", "receivedAt": "2025-09-12T19:10:00Z",
      "lines": [{ "supplyId": "sup_beef_topside", "receivedQty": { "$numberDecimal": "15.0" } }] }
  ],
  "audit": { "createdBy": "admin_1", "createdAt": "2025-09-10T09:00:00Z" }
}
```

### 4.2.6.5. Bounded Context Software Architecture Component Level Diagrams

### 4.2.6.6. Bounded Context Software Architecture Code Level Diagrams

##### 4.2.6.6.1. Bounded Context Domain Layer Class Diagrams

<img src="assets/images/cap4/class_diagram/dc-web-monitoring.png" alt=“DDD” height="400px">

##### 4.2.6.6.2. Bounded Context Database Design Diagram

<img src="assets/images/cap4/db_diagram/db_monitoring.png" alt=“DDD” height="400px">