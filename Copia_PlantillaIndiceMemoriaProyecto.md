# Plantilla de índice propuesta

Willman Acosta Lugo

Te propongo una **plantilla de índice completa, adaptable y orientada a un producto software real** para la Memoria del Proyecto Intermodular de DAM o DAW. La idea es que no sea solo “documentación de lo programado”: debe justificar el problema, las decisiones técnicas, el proceso de trabajo, las pruebas y el resultado obtenido.

El módulo 0492 exige, entre otros aspectos, planificar la ejecución del proyecto y determinar tanto el plan de intervención como la documentación asociada. Además, el proyecto intermodular tiene carácter integrador de las competencias adquiridas durante el ciclo.

[https://github.com/users/lucialopez25/projects/1/views/1](https://github.com/users/lucialopez25/projects/1/views/1)

# Plantilla de Índice Propuesta

PORTADA

DECLARACIÓN DE AUTORÍA Y ORIGINALIDAD

AGRADECIMIENTOS (opcional)

RESUMEN EJECUTIVO

PALABRAS CLAVE

ÍNDICE GENERAL

ÍNDICE DE FIGURAS

ÍNDICE DE TABLAS

LISTADO DE ACRÓNIMOS Y ABREVIATURAS

1\. INTRODUCCIÓN

###    **1.1. Contexto del proyecto**

En la última década, la industria del entretenimiento digital ha experimentado una transformación radical impulsada por la proliferación de plataformas de streaming (como Netflix, HBO Max, Disney+ o Prime Video) y videojuegos (como Xbox Game Pass, PlayStation Plus o Steam). Esta oferta masiva ha democratizado el acceso al contenido, pero también ha generado un fenómeno social recurrente en reuniones presenciales o de ocio compartido: la incapacidad de tomar decisiones grupales de manera ágil.

Paralelamente, el diseño de interfaces de usuario ha evolucionado con la adopción masiva de la mecánica de interacción mediante deslizamiento de tarjetas (swipe), popularizada originalmente por aplicaciones de citas como Tinder o Tiktok. Este patrón de diseño destaca por reducir ofrecer una respuesta visual inmediata y convertir procesos de decisión complejos en interacciones lúdicas e intuitivas.

El presente proyecto nace de la convergencia de estas dos realidades: la necesidad de agilizar la elección de contenido de ocio en grupo y el aprovechamiento de una interfaz de swipe sincronizada en tiempo real.

### **1.2. Problema o necesidad detectada**

El problema principal que aborda este proyecto es la parálisis por elección o choice overload que ocurre en reuniones sociales presenciales, ya sean parejas, grupos de amigos o familiares al intentar seleccionar una película, serie o videojuego para disfrutar en conjunto.

Esta problemática se manifiesta a través de los siguientes factores:

* Pérdida de tiempo: Inversión de períodos prolongados (a menudo superiores a 30 minutos) navegando por los catálogos de distintas plataformas sin llegar a un acuerdo.  
* Fricción e indecisión grupal: Conflictos o discusiones derivadas de opiniones encontradas, donde el debate abierto perjudica la experiencia de ocio.  
* Sesgo de visibilidad: Tendencia a elegir siempre los mismos títulos o recomendaciones principales de las plataformas por fatiga de búsqueda, ignorando opciones del catálogo que complacerían a todos.  
* Ausencia de herramientas: Inexistencia de una solución unificada que aplique esta dinámica tanto al sector cinematográfico como al de los videojuegos multijugador o cooperativos locales.

### **1.3. Propuesta de solución**

La solución propuesta consiste en el diseño y desarrollo de una aplicación móvil multiplataforma que automatiza el proceso de toma de decisiones en grupo.

El funcionamiento del sistema se basa en la creación de salas locales sincronizadas en tiempo real. El anfitrión crea una sala mediante un código único o código QR y configura unos filtros previos como el tipo de contenido y las plataformas activas. Los participantes se unen a la sala desde sus propios dispositivos móviles y comienzan a deslizar una lista limitada de opciones (Like hacia un lado, Pass hacia el otro).

Mediante un algoritmo de coincidencia (match), en el momento en que se detecta unanimidad (o la mayor puntuación ponderada), la aplicación detiene el proceso y muestra de forma destacada la opción elegida, indicando además la plataforma o medio en el que está disponible para su consumo inmediato.

**1.4. Objetivos del proyecto**

**1.4.1. Objetivo general**

Diseñar, desarrollar e implementar una aplicación móvil multiplataforma que facilite la toma de decisiones grupales en la elección de películas, series y videojuegos, mediante una interfaz de deslizamiento de tarjetas (swipe) sincronizada en tiempo real entre múltiples dispositivos conectados a una misma sala virtual. 

**1.4.2. Objetivos específicos**

* Analizar y definir los requisitos del sistema, identificando las necesidades clave de usabilidad (UX/UI) y sincronización en tiempo real.  
* Integrar la aplicación con APIs externas de catálogos de entretenimiento (como TMDB para cine/series e IGDB para videojuegos) para mantener información, portadas y metadatos actualizados.  
* Desarrollar una arquitectura de backend en tiempo real (utilizando WebSockets o bases de datos en tiempo real) capaz de gestionar salas simultáneas con baja latencia.  
* Implementar un flujo de entrada sin fricción, permitiendo la autenticación anónima para que los usuarios puedan unirse a las salas mediante código PIN o código QR sin necesidad de registros extensos.  
* Diseñar e implementar el algoritmo de asignación y cálculo de coincidencia (match), contemplando modalidades por unanimidad y por votación ponderada.  
* Realizar pruebas de integración, rendimiento y usabilidad en dispositivos con sistemas operativos Android e iOS para validar la experiencia de usuario.

**1.5. Alcance del proyecto**

El alcance del proyecto abarca las siguientes áreas funcionales y técnicas:

* Módulo de Gestión de Salas: Creación, configuración, cierre y unión a salas mediante código numérico único de 4 a 6 dígitos o escaneo de código QR.  
* Módulo de Filtros Previos: Definición de parámetros de búsqueda (modo película/juego, plataformas de streaming/consola disponibles, número de jugadores y géneros.  
* Módulo de Interacción (Swipe): Interfaz gráfica interactiva para el deslizamiento de tarjetas con gestos táctiles, limitando el mazo a una cantidad optimizada de cartas por ronda.  
* Sincronización en Tiempo Real: Comunicación bi-direccional entre el servidor y los móviles de la sala para detectar coincidencias al instante.  
* Módulo de Resultados e Información: Pantalla de victoria (Match) que muestra las plataformas donde consumir el contenido.  
* Compatibilidad Multiplataforma: Despliegue funcional en dispositivos móviles Android e iOS.

**1.6. Limitaciones y exclusiones**

### Limitaciones

* Dependencia de APIs de terceros: La disponibilidad, precisión y actualización del catálogo de películas y videojuegos dependerá directamente de los tiempos de respuesta y límites de consulta (rate limits) de las APIs externas (TMDB e IGDB).  
* Conectividad a Internet: Aunque la sala se denomine "local" por la proximidad física de los usuarios, la sincronización requiere una conexión activa a Internet para la comunicación con la base de datos en la nube.

### Exclusiones

* Reproducción de contenido directo: La aplicación no actuará como plataforma de reproductor de vídeo ni ejecutor de juegos (cloud gaming), su alcance se limita estrictamente a la facilitación de la decisión.  
* Gestión de compras o suscripciones integradas: No se procesarán pagos dentro de la app ni se gestionarán las suscripciones de los usuarios a las plataformas de streaming.  
* Red social persistente: En esta versión del proyecto no se incluirá un sistema de mensajería interna, chat global ni listas de amigos permanentes entre salas.

**1.7. Estructura de la memoria**

2\. ANÁLISIS DEL CONTEXTO Y VIABILIDAD

   2.1. Sector profesional y perfil de usuarios
   
El proyecto se encuadra en el sector del desarrollo de software móvil y soluciones digitales para el ocio y entretenimiento. Se sitúa en la intersección entre las aplicaciones de recomendación de contenido y las herramientas de toma de decisiones grupales. 
El público objetivo se divide en dos perfiles principales:
* Usuario Principal (Gen Z y Millennials, 18-35 años): Nativos o adoptantes digitales avanzados, consumidores habituales de plataformas de streaming (Netflix, HBO Max, Disney+, Prime Video) y servicios de videojuegos (Xbox Game Pass, PlayStation Plus, Steam). Acostumbrados a la navegación por gestos en redes sociales y aplicaciones de citas y que valoran la inmediatez, la simplicidad visual y la ausencia de fricciones (como formularios de registro largos).
* Usuario Secundario (Grupos familiares, amigos y parejas): Usuarios de diversa edad que buscan una herramienta funcional para resolver rápidamente la elección de ocio en el hogar durante los fines de semana o momentos de reunión.


   2.2. Análisis de la necesidad
El crecimiento de los catálogos ha generado la paradoja de la elección: a mayor cantidad de opciones, mayor es la fatiga cognitiva y el tiempo requerido para tomar una decisión.

El análisis de esta necesidad revela tres puntos de dolor fundamentales:
* Sesgo de grupo y dominante: En las discusiones abiertas, la decisión suele inclinarse hacia la persona más firme del grupo, dejando insatisfechos a otros integrantes.
* Tiempo de búsqueda desproporcionado: El tiempo invertido en seleccionar qué ver o a qué jugar llega a consumir una fracción significativa del tiempo libre total disponible.
* Falta de una solución transversal: Las soluciones actuales suelen limitarse exclusivamente al cine o carecen de capacidades sincrónicas locales y transversales que incluyan videojuegos cooperativos/multijugador.


   2.3. Estudio de soluciones existentes

   2.4. Partes interesadas

   2.5. Estudio de viabilidad técnica

   2.6. Estudio de viabilidad económica

   2.7. Estudio de viabilidad legal y normativa

      2.7.1. Protección de datos personales

      2.7.2. Propiedad intelectual y licencias

      2.7.3. Accesibilidad y otros requisitos aplicables

   2.8. Análisis de riesgos inicial

3\. PLANIFICACIÓN Y GESTIÓN DEL PROYECTO

   3.1. Metodología de desarrollo empleada

   3.2. Organización del equipo y reparto de responsabilidades

   3.3. Roles del proyecto

* Scrum Master : Lucía   
* Especialista UI/UX (Frontend) : Felipe  
* Q/A tester : Sergio  
* Desarrollador de Lógica y Datos (Backend): Raúl 

	

   3.4. Plan de trabajo

   3.5. Cronograma e hitos

   3.6. Estimación de recursos

   3.7. Presupuesto estimado

   3.8. Gestión de riesgos

   3.9. Herramientas de comunicación, coordinación y seguimiento

* Github Projects : tablero Kanban(ToDo , InProgress , EnEspera, Done)  
*  Discord : Chat y videocámara en tiempo real  
* Whatsapp : chat de mensajería

   3.10. Gestión de versiones y repositorio de código

4\. ANÁLISIS DE REQUISITOS

   4.1. Identificación de usuarios y perfiles

   4.2. Requisitos funcionales

   4.3. Requisitos no funcionales

   4.4. Reglas de negocio

   4.5. Casos de uso o historias de usuario

   4.6. Priorización de requisitos

   4.7. Matriz de trazabilidad de requisitos

5\. DISEÑO DE LA SOLUCIÓN

   5.1. Visión general de la arquitectura

	Modelo Vista Controlador(MVC)

Para la aplicación se adopta el patrón MVC, que separa la aplicación en tres capas con funciones distintas. 

   5.2. Arquitectura software

      5.2.1. Patrón arquitectónico utilizado

      5.2.2. Componentes y módulos

      5.2.3. Comunicación entre componentes

   5.3. Diseño de la base de datos

      5.3.1. Modelo conceptual

      5.3.2. Modelo lógico

      5.3.3. Modelo físico

      5.3.4. Diccionario de datos

   5.4. Diseño de la interfaz de usuario

      5.4.1. Principios de usabilidad y accesibilidad

	Usabilidad

* Decisiones más rápidas. Cada tarjeta de swipe muestra solo lo esencial (imagen, nombre , iconos de swipe).  
* Feedback inmediato. Cada acción (swipe, match) debe tener una respuesta visual y/o sonora.  
* Consistencia. El mismo gesto (swipe) siempre significa lo mismo en toda la app; los iconos y colores se repiten con el mismo significado.  
* Menú de navegación siempre visible, sin que el usuario tenga que memorizar rutas.

	Accesibilidad

* Contraste de color: entre texto y fondo.  
* Tamaño de zona táctil:   
* Alternativa al gesto: toda acción de gesto complejo (swipe) debe tener una alternativa de un solo toque (botones de ❤️/✕ visibles).  
* Texto alternativo en imágenes de carátulas para lectores de pantalla.  
* Tipografía legible: mínimo de pixeles para texto de cuerpo, evitar fuentes decorativas en información funcional.

      5.4.2. Mapa de navegación

      5.4.3. Wireframes o prototipos

	Prototipo Login:

	Prototipo tarjeta Swipe:

      ![][image1]

5.4.4. Diseño visual final

   5.5. Diseño de seguridad

      5.5.1. Autenticación y autorización

      5.5.2. Protección de datos

      5.5.3. Gestión de errores y validaciones

   5.6. Diseño de integraciones y APIs externas

6\. DESARROLLO E IMPLEMENTACIÓN

   6.1. Tecnologías, lenguajes y frameworks utilizados

	Lenguajes de programación como Java , el Toolkit Swing 

	Frameworks como Android SDK

   6.2. Entorno de desarrollo

	NetBeans

   6.3. Estructura del proyecto y organización del código

   6.4. Implementación de funcionalidades principales

   6.5. Implementación de la persistencia de datos

   6.6. Implementación de la interfaz de usuario

   6.7. Integraciones con servicios externos

   6.8. Gestión de dependencias

   6.9. Control de versiones y estrategia de ramas

   6.10. Decisiones técnicas relevantes

7\. PRUEBAS Y ASEGURAMIENTO DE LA CALIDAD

   7.1. Estrategia de pruebas

   7.2. Entorno y herramientas de prueba

   7.3. Pruebas unitarias

   7.4. Pruebas de integración

   7.5. Pruebas funcionales o de sistema

   7.6. Pruebas de usabilidad y accesibilidad

   7.7. Pruebas de seguridad

   7.8. Resultados de las pruebas

   7.9. Incidencias detectadas y correcciones aplicadas

   7.10. Evaluación del cumplimiento de requisitos

8\. DESPLIEGUE Y PUESTA EN PRODUCCIÓN

   8.1. Infraestructura y entorno de despliegue

   8.2. Requisitos de instalación

   8.3. Proceso de despliegue

   8.4. Configuración de servicios y variables de entorno

   8.5. Dominio, certificados y comunicaciones seguras

   8.6. Copias de seguridad y recuperación

   8.7. Monitorización y registro de errores

   8.8. Plan de mantenimiento

9\. MANUALES DE USO

   9.1. Manual de instalación

   9.2. Manual técnico

   9.3. Manual de usuario

   9.4. Guía de administración, si procede

   9.5. Preguntas frecuentes e incidencias habituales

10\. RESULTADOS Y EVALUACIÓN FINAL

    10.1. Producto desarrollado

    10.2. Grado de cumplimiento de los objetivos

    10.3. Grado de cumplimiento de los requisitos

    10.4. Valor aportado a usuarios o cliente

    10.5. Comparación entre la planificación inicial y el resultado final

    10.6. Dificultades encontradas y soluciones adoptadas

    10.7. Competencias técnicas y transversales aplicadas

11\. CONCLUSIONES Y LÍNEAS FUTURAS

    11.1. Conclusiones

    11.2. Mejoras futuras

    11.3. Escalabilidad y evolución posible del producto

    11.4. Reflexión final sobre el aprendizaje adquirido

REFERENCIAS

ANEXOS

   Anexo A. Documento de requisitos completo

   Anexo B. Diagramas técnicos

   Anexo C. Modelo de datos y diccionario de datos

   Anexo D. Casos y evidencias de prueba

   Anexo E. Manual de instalación

   Anexo F. Manual de usuario

   Anexo G. Presupuesto detallado

   Anexo H. Planificación y cronograma

   Anexo I. Licencias y dependencias de terceros

   Anexo J. Enlace al repositorio y a la demostración del proyecto

# Cómo utilizarla bien

No es obligatorio que todos los proyectos incluyan todos los apartados con la misma extensión. La clave es ajustar el índice al alcance real sin eliminar elementos esenciales.

| Tipo de proyecto | Apartados que deben ganar peso |
| ----- | ----- |
| Aplicación web DAW | Arquitectura cliente-servidor, API REST, base de datos, diseño responsive, despliegue web, seguridad y accesibilidad |
| Aplicación móvil DAM | Arquitectura móvil, navegación, persistencia local/remota, permisos, pruebas en dispositivos y publicación o distribución |
| Aplicación de escritorio DAM | Arquitectura por capas, interfaz de escritorio, instalación, acceso a base de datos y manual técnico |
| Proyecto con IA o datos | Viabilidad de los datos, calidad del dataset, tratamiento de datos personales, métricas de evaluación y limitaciones del modelo |
| Proyecto con microservicios | Diagramas de servicios, comunicación API o mensajería, contenedores, observabilidad, despliegue y tolerancia a fallos |

Fíjate que los capítulos 4 a 8 deben mantener una relación **clara: cada requisito debe tener una solución diseñada, una implementación y una prueba que demuestre su cumplimiento**. Esa trazabilidad es una de las mejores evidencias de calidad de la memoria.

# Versión recomendada para alumnado

Para evitar memorias desproporcionadas, usaría esta distribución aproximada:

| Bloque | Extensión orientativa | Finalidad |
| ----- | :---: | ----- |
| Introducción, contexto y viabilidad | 10–15% | Explicar por qué el proyecto es necesario y viable |
| Planificación y requisitos | 15–20% | Demostrar organización y concreción de la solución |
| Diseño técnico | 20–25% | Justificar arquitectura, datos, interfaz y seguridad |
| Desarrollo e implementación | 15–20% | Documentar lo construido sin convertir la memoria en código |
| Pruebas y despliegue | 15–20% | Acreditar calidad y capacidad de puesta en funcionamiento |
| Resultados y conclusiones | 10–15% | Valorar el cumplimiento, las limitaciones y la evolución futura |

El código fuente completo no debería copiarse en la memoria. Es más profesional incorporar fragmentos breves y significativos, diagramas, capturas comentadas, enlaces al repositorio y anexos con las evidencias técnicas necesarias.

# Elementos que no deberían faltar

* **Portada normalizada**. Título, ciclo —DAM o DAW—, módulo 0492, autoría, tutoría, centro, curso y fecha.  
* **Resumen ejecutivo**. Una página. Debe permitir entender el problema, la solución, las tecnologías y el valor del proyecto sin leer el documento completo.  
* **Alcance y exclusiones**. Tan importante es indicar lo que hace la aplicación como dejar claro qué se ha decidido no implementar.  
* **Requisitos verificables**. Por ejemplo, “*el usuario podrá restablecer su contraseña mediante correo electrónico*”, no “*el sistema tendrá una gestión de usuarios adecuada*”.  
* **Diagramas con sentido**. Modelo entidad-relación, casos de uso, arquitectura, componentes y/o secuencia, según el tipo de solución.  
* **Evidencias de prueba**. Tabla de casos de prueba, resultado esperado, resultado real, estado y, cuando convenga, captura o enlace a la incidencia.  
* **Despliegue reproducible**. Otra persona debería poder instalar o ejecutar el sistema siguiendo el manual técnico.  
* **Referencias y licencias**. Documentación de tecnologías, bibliotecas, APIs, imágenes, tipografías, datos y cualquier recurso ajeno empleado.

# Ejemplo de trazabilidad

Un requisito no debe “desaparecer” tras el análisis. Por ejemplo:

| Elemento | Ejemplo |
| ----- | ----- |
| Requisito | RF-12: El administrador podrá consultar las reservas por intervalo de fechas |
| Diseño | Endpoint *GET /reservas?fechaInicio=\&fechaFin=*, consulta indexada por fecha y pantalla de filtros |
| Implementación | Servicio de reservas, repositorio de datos y componente de listado |
| Prueba | CP-12: búsqueda de reservas entre el 1 y el 30 de septiembre; se valida que solo aparecen resultados del intervalo |
| Resultado | Requisito cumplido |

Esta cadena evidencia que el trabajo se ha gestionado como un proyecto profesional y no como una colección de pantallas o funcionalidades independientes.

# Nota Final

La plantilla es una propuesta, **no un índice literal establecido**. Se fundamenta en la naturaleza integradora del Proyecto Intermodular y en el resultado de aprendizaje referido a planificar la ejecución y la documentación asociada del módulo 0492\.

[image1]: <data:image/png;base64,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>
