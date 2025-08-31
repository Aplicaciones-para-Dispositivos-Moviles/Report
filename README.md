<div id="cover-page">

---

# **Informe de Trabajo Final**

---

<img src="assets/images/logo-upc.png" alt="Logo UPC" style="width: 150px; height: auto;" />


_Universidad Peruana de Ciencias Aplicadas_

_Ingeniería de Software_

_2025-20_

**Curso:** _Aplicaciones para Dispositivos Móviles - 12617_

_Sección 12617_

_Prof. Jorge Luis, Mayta Guillermo_

## Nombre del Startup

**Nombre:** _UI-Topic_

## Nombre del Producto

**Producto:** _Restock_

## Relación de Integrantes

|   Código   |       Apellidos y Nombres        |
| :--------: | :------------------------------: |
| u202021885 |       Castro Alejos, Julio       |
|            |    Elescano Leon, Piero Hugo     |
| u202319831 |   Guerra Perez, José Jahaziel    |
| u202318274 |    Julca Minaya, Sergio Gino     |
| u202319448 | Shapiama Rivera, Gabriela Nicole |

---

**Mes y Año**
_Agosto 2025_

</div>

## Registro de Versiones

| *Versión* | *Fecha* | *Autor*         | *Descripción de modificación*                                                                                                                                        |
| :----------: | :-------: | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     1.1     | 14/09/25 | Julio Castro      | Se adjuntó segmentos objetivos, diseño de entrevistas, registro de entrevistas, User Stories, Software Architecture y Bounded Context Resource.                        |
|     1.2     | 15/09/25 | Piero Elescano    | Se elaboró Lean UX Hypothesis Statements, User personas, Empathy Mapping, User Stories, Bounded Context IAM y Profiles, y Bounded Context Canvases.                    |
|     1.3     | 15/09/25 | Jahaziel Guerra   | Se redactó analisis competitivo, User Stories, Ubiquitous Language, Product Backlog, Software Architecture Deployment Diagrams y Bounded Context Planning y Monitoring. |
|     1.4     | 16/09/25 | Sergio Julca      | Se redactó Lean UX Problem Statements y Assumptions, User Stories, Context Mappin, As-Is y To-Be Scenario Mapping y Bounded Context Analytics y Subscriptions.          |
|     1.5     | 16/09/25 | Gabriela Shapiama | Se adjuntó Lean UX Canvas, competidores, registro de entrevistas, Impact Mapping, User Stories, Event Storming y Bounded Context Resource.                             |

# Project Report Collaboration Insights

Esta sección detalla cómo el equipo colaboró para construir el **Final Project Documentation Report** del sistema Restock, mostrando evidencia de trabajo conjunto mediante commits, revisiones, herramientas de organización y resultados integrados en el informe final. Se refleja la contribución de cada integrante en la planificación, desarrollo, documentación y presentación de la solución.

**Repositorio del informe del proyecto:**
[https://shorturl.at/i6Ps8](https://shorturl.at/i6Ps8)

![Evidencia de commits del repositorio](assets/images/presentation/ci-overview.png)

- **Total de commits:** 507
- **Autores contribuyentes:**
  - Piero Elescano (`PieroHugo`)
  - Sergio Julca (`sergioJM05`)
  - Julio Castro (`JulioXC4`)
  - Gabriela Shapiama (`GabrielaShapiama28`)
  - Jahaziel Guerra (`jahazielgg`)

Todas las entregas se desarrollaron sobre ramas específicas con _pull requests_ revisados en equipo. Se utilizaron issues de GitHub y tableros Trello para distribuir tareas, y herramientas como Figma, Draw.io, PlantUML y Structurizr para la elaboración de diagramas incluidos en el informe.

## TB1 – Informe inicial y Landing Page

*Periodo:* 27 de agosto – 18 de setiembre de 2025

Se redactaron las secciones base del informe: Introducción, Justificación, Objetivos, Guias de estilo, Usuarios y Flujo de Valor. Se construyó una **Landing Page estática** con HTML5, CSS3 y JS. Las decisiones se documentaron en Trello, y se utilizó Figma para el primer prototipo visual. Cada sección del informe fue escrita en ramas separadas y luego unificada en `develop`.

![Colaboraciones TB1](assets/images/presentation/ci-tb1.png)

- **Contribuciones destacadas del informe:**

  - Definición de problema y objetivos.
  - Análisis de herramientas similares.
  - Diseño de flujo de valor y tipos de usuario.
  - Prototipo inicial en Figma.
  - Página informativa y formulario de contacto en Landing.

- **Commits por integrante:**

TO-DO

## Herramientas colaborativas utilizadas

- **GitHub Projects & Branching:** Para control de versiones y revisiones.
- **Trello:** Organización de tareas por entregas y responsables.
- **Discord y Google Meet:** Reuniones periódicas para coordinación.
- **Figma:** Bocetos y prototipos de interfaz.
- **PlantUML & Draw.io:** Diagramas de arquitectura y flujo.
- **Structurizr DSL:** Modelado de arquitectura de software (C4 Model).
- **Swagger/OpenAPI:** Documentación interactiva de endpoints REST.
- **Markdown Preview & VSCode:** Redacción técnica en equipo del informe.

# Tabla de contenidos

## [Capítulo I: Introducción](cap1-introduction.md)

- [1.1 Startup Profile](cap1-introduction.md#11-startup-profile)
  - [1.1.1 Descripción de la Startup](cap1-introduction.md#111-descripción-de-la-startup)
  - [1.1.2 Perfiles de integrantes del equipo](cap1-introduction.md#112-perfiles-de-integrantes-del-equipo)
- [1.2 Solution Profile](cap1-introduction.md#12-solution-profile)
  - [1.2.1 Antecedentes y problemática](cap1-introduction.md#121-antecedentes-y-problemática)
  - [1.2.2 Lean UX](cap1-introduction.md#122-lean-ux)
    - [1.2.2.1 Problem Statement](cap1-introduction.md#1221-lean-ux-problem-statement)
    - [1.2.2.2 Assumptions](cap1-introduction.md#1222-lean-ux-assumptions)
    - [1.2.2.3 Hypothesis](cap1-introduction.md#1223-lean-ux-hypothesis-statements)
    - [1.2.2.4 Lean UX Canvas](cap1-introduction.md#1224-lean-ux-canvas)
- [1.3 Segmentos Objetivos](cap1-introduction.md#13-segmentos-objetivos)

## [Capítulo II: Requirements Elicitation &amp; Analysis](cap2-requirements-elicitation-and-analysis.md)

- [2.1 Competidores](cap2-requirements-elicitation-and-analysis.md#21-competidores)
  - [2.1.1 Análisis competitivo](cap2-requirements-elicitation-and-analysis.md#211-análisis-competitivo)
  - [2.1.2 Estrategias y tácticas frente a competidores](cap2-requirements-elicitation-and-analysis.md#212-estrategias-y-tácticas-frente-a-competidores)
- [2.2 Entrevistas](cap2-requirements-elicitation-and-analysis.md#22-entrevistas)
  - [2.2.1 Diseño de entrevistas](cap2-requirements-elicitation-and-analysis.md#221-diseño-de-entrevistas)
  - [2.2.2 Registro de entrevistas](cap2-requirements-elicitation-and-analysis.md#222-registro-de-entrevistas)
  - [2.2.3 Análisis de entrevistas](cap2-requirements-elicitation-and-analysis.md#223-análisis-de-entrevistas)
- [2.3 Needfinding](cap2-requirements-elicitation-and-analysis.md#23-needfinding)
  - [2.3.1 User Personas](cap2-requirements-elicitation-and-analysis.md#231-user-personas)
  - [2.3.2 User Task Matrix](cap2-requirements-elicitation-and-analysis.md#232-user-task-matrix)
  - [2.3.3 User Journey Mapping](cap2-requirements-elicitation-and-analysis.md#233-user-journey-mapping)
  - [2.3.4 Empathy Mapping](cap2-requirements-elicitation-and-analysis.md#234-empathy-mapping)
  - [2.3.5 As-is Scenario Mapping](cap2-requirements-elicitation-and-analysis.md#235-as-is-scenario-mapping)
- [2.4 Ubiquitous Language](cap2-requirements-elicitation-and-analysis.md#24-ubiquitous-language)

## [Capítulo III: Requirements Specification](cap3-requirements-specification.md)

- [3.1 To-Be Scenario Mapping](cap3-requirements-specification.md#31-to-be-scenario-mapping)
- [3.2 User Stories](cap3-requirements-specification.md#32-user-stories)
- [3.3 Impact Mapping](cap3-requirements-specification.md#33-impact-mapping)
- [3.4 Product Backlog](cap3-requirements-specification.md#34-product-backlog)

## [Capítulo IV: Product Design](cap4-product-design.md)

- [4.1. Strategic-Level Domain-Driven Design](cap4-product-design.md#41-strategic-level-domain-driven-design)
  - [4.1.1. EventStorming](cap4-product-design.md#411-eventstorming)
    - [4.1.1.1. Candidate Context Discovery](cap4-product-design.md#4111-candidate-context-discovery)
    - [4.1.1.2. Domain Message Flows Modeling](cap4-product-design.md#4112-domain-message-flows-modeling)
    - [4.1.1.3. Bounded Context Canvases](cap4-product-design.md#4113-bounded-context-canvases)
  - [4.1.2. Context Mapping](cap4-product-design.md#412-context-mapping)
  - [4.1.3. Software Architecture](cap4-product-design.md#413-software-architecture)
    - [4.1.3.1. Software Architecture Context Level Diagrams](cap4-product-design.md#4131-software-architecture-context-level-diagrams)
    - [4.1.3.2. Software Architecture Container Level Diagrams](cap4-product-design.md#4132-software-architecture-container-level-diagrams)
    - [4.1.3.3. Software Architecture Deployment Diagrams](cap4-product-design.md#4133-software-architecture-deployment-diagrams)
- [4.2. Tactical-Level Domain-Driven Design](cap4-product-design.md#42-tactical-level-domain-driven-design)
  - [4.2.1. Bounded Context: `<Resource>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.1.1. Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.1.2. Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.1.3. Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.1.4. Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.1.5. Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.1.6. Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.1.6.1. Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)
    - [4.2.1.6.2. Bounded Context Database Design Diagram](cap4-product-design.md#42x62-bounded-context-database-design-diagram)
  - [4.2.2. Bounded Context: `<Subscriptions>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.2.1. Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.2.2. Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.2.3. Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.2.4. Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.2.5. Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.2.6. Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.2.6.1. Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)
  - [4.2.3. Bounded Context: `<Analytics>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.3.1. Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.3.2. Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.3.3. Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.3.4. Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.3.5. Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.3.6. Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.3.6.1. Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)
  - [4.2.4. Bounded Context: `<Identity and Guess Managements>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.4.1. Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.4.2. Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.4.3. Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.4.4. Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.4.5. Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.4.6. Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.4.6.1. Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)
  - [4.2.5. Bounded Context: `<Monitoring>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.5.1. Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.5.2. Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.5.3. Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.5.4. Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.5.5. Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.5.6. Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.5.6.1. Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)
  - [4.2.6. Bounded Context: `<Profiles>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.6.1. Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.6.2. Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.6.3. Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.6.4. Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.6.5. Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.6.6. Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.6.6.1. Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)
  - [4.2.7. Bounded Context: `<Planning>`](cap4-product-design.md#42x-bounded-context)
    - [4.2.7.1 Domain Layer](cap4-product-design.md#42x1-domain-layer)
    - [4.2.7.2 Interface Layer](cap4-product-design.md#42x2-interface-layer)
    - [4.2.7.3 Application Layer](cap4-product-design.md#42x3-application-layer)
    - [4.2.7.4 Infrastructure Layer](cap4-product-design.md#42x4-infrastructure-layer)
    - [4.2.7.5 Bounded Context Software Architecture Component Level Diagrams](cap4-product-design.md#42x5-bounded-context-software-architecture-component-level-diagrams)
    - [4.2.7.6 Bounded Context Software Architecture Code Level Diagrams](cap4-product-design.md#42x6-bounded-context-software-architecture-code-level-diagrams)
    - [4.2.7.6.1 Bounded Context Domain Layer Class Diagrams](cap4-product-design.md#42x61-bounded-context-domain-layer-class-diagrams)

## [Capítulo V: Product Implementation, Validation &amp; Deployment](cap5-prod-implementation-validation-deployment.md)

- [5.1 Software Configuration Management](cap5-prod-implementation-validation-deployment.md#51-software-configuration-management)
  - [5.1.1 Software Development Environment Configuration](cap5-prod-implementation-validation-deployment.md#511-software-development-environment-configuration)
  - [5.1.2 Source Code Management](cap5-prod-implementation-validation-deployment.md#512-source-code-management)
  - [5.1.3 Source Code Style Guide &amp; Conventions](cap5-prod-implementation-validation-deployment.md#513-source-code-style-guide--conventions)
  - [5.1.4 Software Deployment Configuration](cap5-prod-implementation-validation-deployment.md#514-software-deployment-configuration)
- [5.2 Landing Page, Services &amp; Applications Implementation](cap5-prod-implementation-validation-deployment.md#52-landing-page-services--applications-implementation)
  - [5.2.X Sprint n](cap5-prod-implementation-validation-deployment.md#521-sprint-1)
    - [5.2.X.1 Sprint Planning n](cap5-prod-implementation-validation-deployment.md#5211-sprint-planning-1)
    - [5.2.X.2 Aspect Leaders and Collaborators](cap5-prod-implementation-validation-deployment.md#5212-aspect-leaders-and-collaborators)
    - [5.2.X.3 Sprint Backlog n](cap5-prod-implementation-validation-deployment.md#5213-sprint-backlog-1)
    - [5.2.X.4 Development Evidence for Sprint Review](cap5-prod-implementation-validation-deployment.md#5214-development-evidence-for-sprint-review)
    - [5.2.X.5 Execution Evidence for Sprint Review](cap5-prod-implementation-validation-deployment.md#5215-execution-evidence-for-sprint-review)
    - [5.2.X.6 Services Documentation Evidence for Sprint Review](cap5-prod-implementation-validation-deployment.md#5216-services-documentation-evidence-for-sprint-review)
    - [5.2.X.7 Software Deployment Evidence for Sprint Review](cap5-prod-implementation-validation-deployment.md#5217-software-deployment-evidence-for-sprint-review)
    - [5.2.X.8 Team Collaboration Insights during Sprint](cap5-prod-implementation-validation-deployment.md#5218-team-collaboration-insights-during-sprint)

## [Conclusiones](conclusiones.md)

- [Conclusiones y recomendaciones](conclusiones.md#conclusiones-y-recomendaciones)
- [Video About-the-Team](conclusiones.md#video-about-the-team)

## [Bibliografía](bibliography.md)
Cross, D. (2024). Innovating Restaurant Inventory Management Application Enhancing Quality And Efficiency Through Extreme Pro-gramming Approach. _JURNAL EKONOMI, 13_(2), 696-698. [https://ejournal.seaninstitute.or.id/index.php/Ekonomi/article/view/4476](https://ejournal.seaninstitute.or.id/index.php/Ekonomi/article/view/4476)

Valenzuela, A., Vera, B., Castillo, L., Valenzuela, J. (2024). Industry 4.0 in Logistics Management in Latin America: A Bibliometric Review. _Journal of Indutrial Ingineering and Management, 18_(1), 115-129. [https://www.jiem.org/index.php/jiem/article/view/8147/1117](https://www.jiem.org/index.php/jiem/article/view/8147/1117)

Lévesque, J., Godin, L., Perreault, V., & Mikhaylin, S. (2024). Identifying the factors affecting the implementation of food waste reduction strategies in independent restaurants: Moving towards eco-efficiency. _Journal of Cleaner Production, 440_, 140765. https://doi.org/10.1016/j.jclepro.2024.140765

Tan, Y., Hai, F., Popp, J., & Oláh, J. (2022). Minimizing Waste in the Food Supply Chain: Role of Information System, Supply Chain Strategy, and Network Design. _Sustainability, 14_(18), 11515. https://doi.org/10.3390/su141811515

## [Anexos](anexos.md)

# ABET – EAC - Student Outcome 7

**Criterio:** La capacidad de adquirir y aplicar nuevos conocimientos según sea
necesario, utilizando estrategias de aprendizaje apropiadas.

En el siguiente cuadro se describe las acciones realizadas y enunciados de conclusiones por parte del grupo, que permiten sustentar el haber alcanzado el logro del ABET – EAC - Student Outcome 7.

| Criterio específico | Acciones realizadas | Conclusiones |
|---------------------|---------------------|--------------|
| **Actualiza conceptos y conocimientos necesarios para su desarrollo profesional y en especial para su proyecto en soluciones de software.** | **Julio Castro Alejos** <br />TB1: Segmentos objetivo: Aplicó métodos de identificación de usuarios y mercados relevantes.<br />Diseño y registro de entrevistas : Aprendió técnicas de levantamiento de información cualitativa.<br />User Journey Mapping : Desarrolló habilidades de representación de experiencias de usuario para mejorar el diseño de soluciones.<br /><br />**Piero Hugo Elescano Leon** <br />TB1: Descripción de la Startup : Estudió la estructura de negocio digital como base del proyecto.<br />Lean UX Hypothesis Statements : Aplicó nuevas técnicas para plantear hipótesis y validar supuestos.<br />Estrategias frente a competidores : Adquirió nociones de benchmarking estratégico.<br />User Personas y Empathy Mapping : Profundizó en metodologías de caracterización de usuarios.<br /><br />**José Jahaziel Guerra Perez** <br />TB1: Antecedentes y problemática : Investigó conceptos clave del sector gastronómico y tecnológico.<br />Análisis competitivo : Aprendió a comparar fortalezas y debilidades frente al mercado.<br />Ubiquitous Language : Incorporó conocimientos de DDD para uniformizar términos del proyecto.<br />Product Backlog : Aplicó prácticas de gestión ágil en el levantamiento de requerimientos.<br /><br />**Julca Minaya, Sergio Gino** <br />TB1: Lean UX Problem Statements y Assumptions : Practicó la definición de problemas y supuestos.<br />Análisis de entrevistas : Adquirió experiencia en síntesis de datos cualitativos.<br />Context Mapping : Incorporó técnicas para identificar relaciones entre actores y procesos.<br />User Task Matrix : Estructuró las tareas de usuarios en función de objetivos de negocio.<br /><br />**Gabriela Nicole Shapiama Rivera** <br />TB1: Lean UX Canvas : Aprendió a integrar problemas, hipótesis y métricas en un marco visual.<br />Competidores : Desarrolló habilidades de análisis comparativo.<br />Registro de entrevistas : Practicó técnicas de documentación y organización de hallazgos.<br />Impact Mapping : Profundizó en la representación de impactos y objetivos estratégicos. | **TB1:**<br />Cada integrante incorporó nuevos conceptos y metodologías (Lean UX, entrevistas, análisis competitivo, mapeos, backlog ágil). Esto fortaleció su capacidad de adquirir conocimientos aplicables en la construcción del proyecto, alineando investigación, diseño estratégico y gestión de software. |
| **Reconoce la necesidad del aprendizaje permanente para el desempeño profesional y el desarrollo de proyectos en soluciones de software.** | **Julio Castro Alejos** <br />TB1: Detectó la importancia del aprendizaje continuo al aplicar entrevistas y journey mapping para identificar nuevas necesidades de usuarios.<br /><br />**Piero Hugo Elescano Leon** <br />TB1: Comprendió que el aprendizaje permanente es clave al generar hipótesis Lean UX y analizar competidores de manera iterativa.<br /><br />**José Jahaziel Guerra Perez** <br />TB1: Reconoció que debe actualizarse constantemente al investigar antecedentes, problemáticas y aplicar backlog en metodologías ágiles.<br /><br />**Julca Minaya, Sergio Gino** <br />TB1: Entendió la importancia del aprendizaje continuo al analizar entrevistas y usar context mapping para representar dinámicas cambiantes.<br /><br />**Gabriela Nicole Shapiama Rivera** <br />TB1: Reafirmó la necesidad del aprendizaje permanente mediante el uso de herramientas de diseño estratégico (Lean UX Canvas, Impact Mapping) y el registro de entrevistas. | **TB1:**<br />El equipo evidenció que el aprendizaje permanente es indispensable. La investigación constante, la validación de supuestos y la aplicación de metodologías ágiles y de diseño estratégico muestran cómo el conocimiento debe renovarse y ampliarse de manera continua para el éxito de un proyecto de software. |

# Objetivos SMART

A continuación, se presentarán los objetivos SMART (Specific, Measurable, Achievable, Relevant y Time-bound) relacionados al desarrollo profesional de cada integrante del equipo una vez finalizada su carrera.

**-- Julio Castro --**

* En los primeros 6 meses posteriores a mi graduación, desarrollaré y publicaré en GitHub al menos 3 proyectos profesionales (uno en desarrollo web, uno en móvil y uno con enfoque en ciberseguridad básica). Cada proyecto deberá incluir documentación técnica y pruebas de funcionamiento. Esto me permitirá explorar las tres áreas con resultados tangibles para mi portafolio y decidir en cuál especializarme.

* En un plazo de 24 meses, obtendré un puesto de trabajo en el área que haya elegido (web, móvil o ciberseguridad) y habré alcanzado al menos una certificación internacional reconocida (ejemplo: AWS Certified Developer, Google Associate Android Developer o CompTIA Security+). Además, me fijaré como meta contribuir en al menos dos proyectos colaborativos open source relacionados a mi área para demostrar experiencia práctica y fortalecer mi red profesional.


**-- Piero Elescano --**

**-- Jahaziel Guerra --**

**-- Sergio Julca --**


**-- Gabriela Shapiama --**

* En los 12 meses posteriores a mi graduación, rotar por 3 áreas de software (por ejemplo, frontend, backend/API y DevOps/QA), realizando al menos 1 proyecto entregable por área y publicando una bitácora de aprendizaje por cada una. Esto me permitirá colaborar con equipos diversos, fortalecer habilidades end-to-end y, con evidencia de resultados, definir con mayor precisión mi futura especialización.
* En 18 meses ampliaré mi exposición a tecnología para entretenimiento participando en 1–2 eventos del sector (meetups, game jams o showcases académicos) para conocer prácticas y hacer networking; contribuiré con 1 o más PR(s) a un proyecto open source afín (por ejemplo, librerías de audio/gráficos, motores o tooling de streaming) y realizaré 1 entrega pública (demo técnica reproducible). Además, estableceré una mentoría con un profesional del área para revisar portafolio, priorizar habilidades y definir oportunidades concretas de siguiente paso.
