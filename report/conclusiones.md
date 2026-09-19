# Conclusiones

Al finalizar la primera etapa de investigación, especificación de requerimientos, diseño del producto e implementación de la presencia digital de **PulsePower**, el equipo **SportPlus** ha establecido una serie de conclusiones relacionadas con la problemática identificada, los supuestos formulados bajo el enfoque **Lean UX** y los avances alcanzados mediante el desarrollo ágil basado en **Sprints**.

### 1. Contrastación de Problem Statements y supuestos (Assumptions)

Inicialmente, se identificó como problemática la dificultad que presentan los deportistas y las personas interesadas en mejorar su bienestar para interpretar conjuntamente los indicadores de esfuerzo, sueño y recuperación. Esta situación puede llevarlos a organizar sus actividades y descansos principalmente mediante percepciones subjetivas, sin comprender completamente la información proporcionada por sus dispositivos.

A partir del **Needfinding** y las entrevistas realizadas a representantes de ambos segmentos objetivo, se identificó la necesidad de contar con explicaciones claras y contextualizadas que permitan relacionar los datos fisiológicos con las rutinas diarias. Los hallazgos respaldan el problema que **PulsePower** busca abordar y orientan su propuesta hacia la interpretación personalizada de la información, en lugar de limitarse a presentar métricas aisladas.

Asimismo, se reconoció que los dos segmentos tienen necesidades diferentes: los deportistas priorizan la planificación del esfuerzo y la recuperación, mientras que los usuarios enfocados en el bienestar buscan comprender sus hábitos de descanso y su estado cotidiano. Por ello, la personalización constituye un elemento central de la solución.

### 2. Contrastación de hipótesis (Hypothesis Statements)

- **Hipótesis de comprensión fisiológica:** Se planteó que presentar indicadores de sueño, esfuerzo y recuperación de manera centralizada y comprensible permitirá reducir la incertidumbre del usuario sobre su estado físico. La investigación inicial respalda la necesidad de esta funcionalidad, aunque su efectividad deberá comprobarse mediante pruebas de comprensión con usuarios.

- **Hipótesis de personalización:** Se estableció que incorporar los objetivos, hábitos y preferencias durante la configuración inicial permitirá generar recomendaciones más contextualizadas. Esta hipótesis orientó el diseño de los perfiles y las funcionalidades de entrenamiento y bienestar, quedando pendiente su validación mediante el uso real de la plataforma.

- **Hipótesis de integración y seguimiento:** Se consideró que la sincronización de una pulsera compatible, junto con la visualización de tendencias y reportes, facilitará el seguimiento continuo del usuario. Para contrastarla, será necesario evaluar la confiabilidad de la sincronización, la frecuencia de consulta y la utilidad percibida de las recomendaciones durante futuras pruebas.

### 3. Cumplimiento de los objetivos de diseño y avances de implementación

Durante el desarrollo del proyecto, se definió la identidad visual de **PulsePower** y se elaboraron la arquitectura de información, los wireframes, los mock-ups y los diagramas de navegación de la **Landing Page** y la aplicación web. Estos entregables permitieron representar la experiencia propuesta para ambos segmentos y mantener coherencia entre las principales funcionalidades.

Desde la perspectiva técnica, se estableció una arquitectura basada en **Angular y TypeScript** para la aplicación web, **Java y Spring Boot** para la API, y **PostgreSQL** para la persistencia de datos. El dominio se organizó en seis *bounded contexts*, complementados por módulos de soporte para identidad, perfiles y suscripciones. Los diagramas de arquitectura, clases y base de datos proporcionan una referencia para continuar la implementación de manera modular.

En el **Sprint 1**, el equipo avanzó en la implementación de la **Landing Page responsive** de PulsePower, orientada a presentar la propuesta de valor, los beneficios y las principales funcionalidades del producto. Asimismo, se establecieron herramientas y convenciones de trabajo colaborativo para gestionar el código fuente y organizar los siguientes incrementos del sistema.

En conjunto, estos avances permiten concluir que **PulsePower** cuenta con una propuesta de producto y una base de diseño y arquitectura definidas. La validación de sus beneficios fisiológicos, la personalización efectiva de las recomendaciones y la integración completa de los servicios permanecen como objetivos de las siguientes etapas.

## Recomendaciones (Roadmap)

Considerando los avances alcanzados y las funcionalidades pendientes de implementación y validación, se proponen las siguientes líneas de acción para continuar el desarrollo de **PulsePower**:

- **Validación con usuarios:** realizar pruebas de comprensión, usabilidad y utilidad percibida con representantes de ambos segmentos, contrastando los resultados con los criterios de éxito establecidos en Lean UX.

- **Integración de datos fisiológicos:** definir y probar el contrato con AIoTI, considerando autorización, sincronización, calidad de los datos y prevención de registros duplicados.

- **Evolución de la Web Application:** implementar progresivamente los módulos de entrenamiento, sueño, bienestar, recomendaciones, reportes y comunidad, priorizando las historias de usuario del Product Backlog.

- # Bibliografía
<ul>
  <li>
    Brown, S. (2020). <em>The C4 model for visualising software architecture</em>. C4 Model. Recuperado de <a href="https://c4model.com/">https://c4model.com/</a>
  </li>
  <li>
    Cohn, M. (2004). <em>User Stories Applied: For Agile Software Development</em>. Addison-Wesley Professional.
  </li>
  <li>
    Evans, E. (2003). <em>Domain-Driven Design: Tackling Complexity in the Heart of Software</em>. Addison-Wesley Professional.
  </li>
  <li>
    Gothelf, J., & Seiden, J. (2021). <em>Lean UX: Designing Great Products with Agile Teams</em> (3rd ed.). O'Reilly Media.
  </li>
  <li>
    Robertson, J., Robertson, S., & Reed, A. (2023). <em>Mastering the Requirements Process: Getting Requirements Right</em> (4th ed.). Addison-Wesley Professional.
  </li>
  <li>
    Wiegers, K., & Hokanson, C. (2023). <em>Software Requirements Essentials: Core Practices for Successful Business Analysis</em>. Addison-Wesley Professional.
  </li>
  <li>
    Heath, F. (2020). <em>Managing Software Requirements the Agile Way</em>. Packt Publishing.
  </li>
  <li>
    Lee, C. (2023). <em>The Art of Crafting User Stories</em>. O'Reilly Media.
  </li>
  <li>
    Dirección General de Medicamentos, Insumos y Drogas [DIGEMID]. (2018). <em>Manual de Buenas Prácticas de Manufactura de Productos Farmacéuticos</em>. Ministerio de Salud del Perú.
  </li>

  <li>
    Mendel, J. (s.f.). <em>Seriously, what’s your startup’s problem?</em>. Recuperado de <a href="https://medium.com/@jakemendel/seriously-whats-your-startup-s-problemb3a884c54ab4">https://medium.com/@jakemendel/seriously-whats-your-startup-s-problemb3a884c54ab4</a>
  </li>
  <li>
    <em>Lean UX – Chapter 3 (Sampler)</em>. Recuperado de <a href="https://www.scribd.com/document/655516553/Leanux-Sampler">https://www.scribd.com/document/655516553/Leanux-Sampler</a>
  </li>
  <li>
    Dittrich, J. (s.f.). <em>A Beginner’s Guide to Finding User Needs</em>. Recuperado de <a href="https://jdittrich.github.io/userNeedResearchBook/">https://jdittrich.github.io/userNeedResearchBook/</a>
  </li>
  <li>
    Mountain Goat Software. (s.f.). <em>User Stories Articles</em>. Recuperado de <a href="https://www.mountaingoatsoftware.com/blog/tag/user-stories">https://www.mountaingoatsoftware.com/blog/tag/user-stories</a>
  </li>
  <li>
    Sameera, S. (s.f.). <em>How to Write a User Story for an API Product</em>. Recuperado de <a href="https://sameera17w.medium.com/how-to-write-a-user-story-for-an-api-product7af6abd4ad2e">https://sameera17w.medium.com/how-to-write-a-user-story-for-an-api-product7af6abd4ad2e</a>
  </li>

  <li>
    UXPressia. (s.f.). <em>User vs. Buyer Persona: Differences and free template</em>. Recuperado de <a href="https://uxpressia.com/blog/user-persona-vs-buyer-persona-difference">https://uxpressia.com/blog/user-persona-vs-buyer-persona-difference</a>
  </li>
  <li>
    UXPressia. (s.f.). <em>How to create an Impact Map in 4 easy steps?</em>. Recuperado de <a href="https://uxpressia.com/blog/build-impact-map-4-easy-steps">https://uxpressia.com/blog/build-impact-map-4-easy-steps</a>
  </li>
  <li>
    IBM. (s.f.). <em>As-is Scenario Map</em>. Recuperado de <a href="https://www.ibm.com/design/thinking/page/toolkit/activity/as-is-scenario-map">https://www.ibm.com/design/thinking/page/toolkit/activity/as-is-scenario-map</a>
  </li>
  <li>
    IBM. (s.f.). <em>To-be Scenario Map</em>. Recuperado de <a href="https://www.ibm.com/design/thinking/page/toolkit/activity/to-be-scenario-map">https://www.ibm.com/design/thinking/page/toolkit/activity/to-be-scenario-map</a>
  </li>
  <li>
    IBM. (s.f.). <em>Empathy Map</em>. Recuperado de <a href="https://www.ibm.com/design/thinking/page/toolkit/activity/empathy-map">https://www.ibm.com/design/thinking/page/toolkit/activity/empathy-map</a>
  </li>
  <li>
    Nielsen Norman Group. (s.f.). <em>Empathy Mapping</em>. Recuperado de <a href="https://www.nngroup.com/articles/empathy-mapping/">https://www.nngroup.com/articles/empathy-mapping/</a>
  </li>
  <li>
    Nielsen Norman Group. (s.f.). <em>Design Systems 101</em>. Recuperado de <a href="https://www.nngroup.com/articles/design-systems-101/">https://www.nngroup.com/articles/design-systems-101/</a>
  </li>
  <li>
    Nielsen Norman Group. (s.f.). <em>Front-End Style Guides</em>. Recuperado de <a href="https://www.nngroup.com/articles/front-end-style-guides/">https://www.nngroup.com/articles/front-end-style-guides/</a>
  </li>
  <li>
    Nielsen Norman Group. (s.f.). <em>The Four Dimensions of Tone of Voice</em>. Recuperado de <a href="https://www.nngroup.com/articles/tone-of-voice-dimensions/">https://www.nngroup.com/articles/tone-of-voice-dimensions/</a>
  </li>
  <li>
    CareerFoundry. (s.f.). <em>What are User Flows in UX Design?</em>. Recuperado de <a href="https://careerfoundry.com/en/blog/ux-design/what-are-user-flows/">https://careerfoundry.com/en/blog/ux-design/what-are-user-flows/</a>
  </li>

  <li>
    Progressa Lean. (s.f.). <em>5W2H – Técnica de análisis de problemas</em>. Recuperado de <a href="https://www.progressalean.com/5w2h-tecnica-de-analisis-de-problemas/">https://www.progressalean.com/5w2h-tecnica-de-analisis-de-problemas/</a>
  </li>
  <li>
    DZone. (s.f.). <em>Acceptance Criteria in Scrum</em>. Recuperado de <a href="https://dzone.com/articles/acceptance-criteria-in-software-explanation-exampl">https://dzone.com/articles/acceptance-criteria-in-software-explanation-exampl</a>
  </li>
  <li>
    Modern Requirements. (s.f.). <em>Requirements Traceability Matrix</em>. Recuperado de <a href="https://www.modernrequirements.com/blogs/using-a-requirements-traceabilitymatrix-to-improve-project-quality/">https://www.modernrequirements.com/blogs/using-a-requirements-traceabilitymatrix-to-improve-project-quality/</a>
  </li>

  <li>
    Fowler, M. (s.f.). <em>Ubiquitous Language</em>. Recuperado de <a href="https://martinfowler.com/bliki/UbiquitousLanguage.html">https://martinfowler.com/bliki/UbiquitousLanguage.html</a>
  </li>
  <li>
    Open Practice Library. (s.f.). <em>Ubiquitous Language</em>. Recuperado de <a href="https://openpracticelibrary.com/practice/ubiquitous-language/">https://openpracticelibrary.com/practice/ubiquitous-language/</a>
  </li>
  <li>
    Nick Tune. (s.f.). <em>Domain-Driven Architecture Diagrams</em>. Recuperado de <a href="https://medium.com/nick-tune-tech-strategy-blog/domain-driven-architecturediagrams-139a75acb578">https://medium.com/nick-tune-tech-strategy-blog/domain-driven-architecturediagrams-139a75acb578</a>
  </li>
  <li>
    Domain Storytelling. (s.f.). <em>Domain Storytelling and Requirements</em>. Recuperado de <a href="https://domainstorytelling.org/#dst-requirements">https://domainstorytelling.org/#dst-requirements</a>
  </li>
  <li>
    DDD Crew. (s.f.). <em>Big Picture EventStorming</em>. Recuperado de <a href="https://github.com/ddd-by-examples/library/blob/master/docs/big-picture.md">https://github.com/ddd-by-examples/library/blob/master/docs/big-picture.md</a>
  </li>
  <li>
    DDD Crew. (s.f.). <em>Design Level EventStorming</em>. Recuperado de <a href="https://github.com/ddd-by-examples/library/blob/master/docs/design-level.md">https://github.com/ddd-by-examples/library/blob/master/docs/design-level.md</a>
  </li>

  <li>
    <em>The Markdown Guide</em>. Recuperado de <a href="https://www.markdownguide.org/">https://www.markdownguide.org/</a>
  </li>
  <li>
    Noam Tamim. (s.f.). <em>How to use PlantUML with Markdown</em>. Recuperado de <a href="https://gist.github.com/noamtamim/f11982b28602bd7e604c233fbe9d910f">https://gist.github.com/noamtamim/f11982b28602bd7e604c233fbe9d910f</a>
  </li>
  <li>
    Structurizr. (s.f.). <em>Embedding diagrams</em>. Recuperado de <a href="https://docs.structurizr.com/cloud/embed">https://docs.structurizr.com/cloud/embed</a>
  </li>
  <li>
    Connect2Group. (s.f.). <em>Using PlantUML for diagrams</em>. Recuperado de <a href="https://connect2grp.medium.com/using-plantuml-for-creating-clear-and-concisediagrams-2fc621529560">https://connect2grp.medium.com/using-plantuml-for-creating-clear-and-concisediagrams-2fc621529560</a>
  </li>

  <li>
    Driessen, V. (2010). <em>A successful Git branching model</em>. Recuperado de <a href="https://nvie.com/posts/a-successful-git-branching-model/">https://nvie.com/posts/a-successful-git-branching-model/</a>
  </li>
  <li>
    <em>Semantic Versioning 2.0.0</em>. Recuperado de <a href="https://semver.org/">https://semver.org/</a>
  </li>
  <li>
    <em>Conventional Commits</em>. Recuperado de <a href="https://www.conventionalcommits.org/">https://www.conventionalcommits.org/</a>
  </li>
</ul>

<div style="page-break-after: always;"></div>
<div style="page-break-after: always;"></div>

# Anexos

## Anexo A: Videos de Exposiciones

| Entrega | Nombre del archivo | URL |
| :--- | :--- | :--- |
| AV1 | `upc-pre-202620-1asi0729-7737-pluspower-expo-av1.mp4` | [Ver exposición AV1](link) |
