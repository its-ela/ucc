1. **¿Por qué es importante el levantamiento de requisitos en el desarrollo de Software?**

El levantamiento de requisitos (también llamado recolección, elicitation o análisis de requerimientos) es la fase más crítica del desarrollo de software. 

Las razones principales por las que es tan importante:

* **_Costo y Eficiencia Económica:_** Reduce costos drásticamente: un error aquí cuesta 1×, en producción puede costar 100–1000×.

* **_Definición y Alcance del Producto:_** Define exactamente qué se va a construir (evita desarrollar el producto equivocado). Controla el scope creep (evita que el alcance se infle sin control).

* **_Planificación y Estimación:_** Permite estimaciones realistas de tiempo, presupuesto y recursos.

* **_Alineación y Comunicación:_** Alinea expectativas entre clientes, usuarios y equipo.

* _**Calidad y Detección Temprana de Problemas:**_ Detecta temprano inconsistencias, ambigüedades y requisitos no funcionales (seguridad, rendimiento…).

* **_Reducción de Riesgo y Éxito del Proyecto:_** Es la causa #1 de fracaso en muchos proyectos de software.

En resumen, sin un buen levantamiento de requisitos → alto riesgo de fracaso, retrasos y desperdicio. Con él → base sólida para entregar lo que realmente se necesita.

- - - - - - - - -  - - - - - -  - - - - - - - - - - - -  - - - - - -  - -

**2. Agregue los términos que construyó con su equipo.**

- _**MVP (Producto Mínimo Viable):**_ Es la versión más ligera pero funcional de un producto que ya resuelve el problema principal para un grupo reducido de usuarios tempranos, permitiendo recoger evidencia real antes de invertir en perfeccionamiento masivo.  
    **- Origen:** El término “Minimum Viable Product” fue acuñado alrededor de 2001 por Frank Robinson (SyncDev), pero explotó en popularidad gracias a Steve Blank y sobre todo Eric Ries con “The Lean Startup” (2011). Antes se hablaba de prototipos o “smoke tests”, pero MVP enfatiza lo “viable” = capaz de generar valor y aprendizaje pagado.  
    **- Básico:** Es como sacar una tortilla de prueba con solo huevo, tortilla y sal: ves si a la gente le gusta el sabor base antes de agregar aguacate, queso y salsas caras.  
    **- Práctico:** Para un software de gestión de tareas como Asana, el MVP inicial podría enfocarse solo en crear listas y asignar deadlines, probando con early adopters antes de agregar integraciones con calendarios o IA predictiva.  
    **- Naturaleza profunda:** Expresa que la verdad de un producto no está en la idea perfecta en la cabeza del fundador, sino en el encuentro real con el uso y el pago; su ser emerge de la retroalimentación iterativa (ontología de validación empírica y aprendizaje).  
    - **Manifestación concreta:** En la práctica se ven MVPs de diferente “peso”: desde un landing page con espera (concierge MVP, como un script manual que simula automatización) hasta un producto funcional pero austero (un app web básica con backend mínimo). Esta distinción óntica separa lo que realmente genera tracción de lo que solo parece bonito en presentaciones.  
    **- Ejemplo real:** Dropbox (fundado en 2007) lanzó su MVP como un video demo simple que mostraba sincronización de archivos, atrayendo 75.000 sign-ups en una noche sin código completo, validando la demanda antes de desarrollar el full client y escalar a millones de usuarios.

- **Integración API:** Es el mecanismo estandarizado mediante el cual dos o más sistemas de software se comunican de forma automática y segura, compartiendo datos o funcionalidades como si fueran extensiones naturales uno del otro.**  
    - Origen:** “API” (Application Programming Interface) nace en los años 40–50 con los primeros lenguajes de alto nivel y se consolida en los 60–70 con sistemas operativos y bibliotecas reutilizables. El término “integración API” gana fuerza en los 2000 con la explosión de servicios web (REST, SOAP) y la economía de plataformas (Google Maps, Twilio, Stripe), convirtiéndose en el “pegamento” invisible de la nube.  
    **- Básico:** Es como enchufar el cargador del celular al enchufe: no necesitas entender la electricidad interna, solo que el estándar coincide y fluye la energía (datos).  
    **- Práctico:** En un dashboard de e-commerce como Shopify, la integración API con Stripe permite procesar pagos en tiempo real, sincronizando transacciones sin intervención manual y mejorando la experiencia del usuario.  
    **- Naturaleza profunda:** Revela que el ser de un software moderno ya no es solitario: su esencia reside en la capacidad relacional y en protocolos compartidos que trascienden el código individual (ontología de conectividad y composición).  
    **- Manifestación concreta:** En la vida real distinguimos integraciones simples (un webhook que envía notificaciones cuando un commit se mergea en GitHub) de complejas (orquestación bidireccional con autenticación OAuth, rate limiting y manejo de errores en un microservicios setup). Esta capa óntica muestra cómo una buena integración pasa desapercibida, mientras que una mala genera fricciones visibles (retrasos, datos duplicados, caídas).  
    **- Ejemplo real:** En el ecosistema de Slack (lanzado en 2013), la integración API con herramientas como Trello o Google Calendar permite que bots automaticen flujos de trabajo, como crear tarjetas en Trello desde un mensaje en Slack, reduciendo silos y acelerando productividad en equipos de dev remotos.  
      
    
- **Stakeholders:** Son las personas, grupos u organizaciones que mantienen un interés real (económico, emocional, regulatorio o de poder) en un proyecto o empresa, porque pueden influir en su curso o verse directamente afectados por sus resultados.  
    **- Origen:** La palabra surge en el siglo XVIII de las apuestas (“stake” = apuesta o participación puesta en juego, + “holder” = quien la custodia o tiene en custodia). Originalmente era el tercero neutral que guardaba el dinero de una apuesta. Hacia 1960–1970 se trasladó al mundo empresarial gracias a pensadores como R. Edward Freeman, quien en 1984 lo elevó a concepto estratégico: ya no solo “quien tiene algo en juego”, sino quien debe ser considerado activamente para que el sistema funcione sin fricciones graves.  
    **- Básico:** Como en una partida de cartas donde todos los jugadores tienen fichas sobre la mesa; si uno se retira o cambia reglas, el juego entero se altera.  
    **- Práctico:** En el desarrollo de una app como Spotify, los stakeholders incluyen programadores (interés en código estable), usuarios premium (interés en nuevas playlists), artistas (interés en royalties justos) y accionistas (interés en crecimiento de suscriptores). Un cambio en el algoritmo afecta a todos.  
    **- Naturaleza profunda:** En el fondo, representan la realidad relacional del éxito: ningún proyecto existe aislado; su ser depende de redes de expectativas mutuas y poder distribuido (ontología de interdependencia).  
    **- Manifestación concreta:** En la práctica diaria vemos categorías claras: internos (equipo de devs, QA testers) que controlan recursos en un sprint de Agile, externos pasivos (usuarios beta que dan feedback) que votan con su uso, y externos activos (inversores de venture capital o reguladores de datos como GDPR) que pueden bloquear o acelerar releases. Esta distinción óntica ayuda a mapear quién realmente mueve la aguja en cada fase.  
    **- Ejemplo real:** En el proyecto open-source de Kubernetes (iniciado por Google en 2014), stakeholders como ingenieros de Google (internos), contribuyentes de la comunidad CNCF (externos activos) y empresas usuarias como Netflix (externos pasivos) colaboraron para evolucionar el orquestador de contenedores, priorizando features basadas en necesidades compartidas para evitar forks innecesarios.

- - - - - - -  - - - - - - - - - -  - - - - - - - - - -  - - -