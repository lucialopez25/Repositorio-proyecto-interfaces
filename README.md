# Repositorio_Proyecto_Intermodular

## 1. INTRODUCCIÓN

### 1.1. Contexto del proyecto
En la última década, la industria del entretenimiento digital ha experimentado una transformación radical impulsada por la proliferación de plataformas de streaming (como Netflix, HBO Max, Disney+ o Prime Video) y videojuegos (como Xbox Game Pass, PlayStation Plus o Steam). Esta oferta masiva ha democratizado el acceso al contenido, pero también ha generado un fenómeno social recurrente en reuniones presenciales o de ocio compartido: la incapacidad de tomar decisiones grupales de manera ágil.

Paralelamente, el diseño de interfaces de usuario ha evolucionado con la adopción masiva de la mecánica de interacción mediante deslizamiento de tarjetas (swipe), popularizada originalmente por aplicaciones de citas como Tinder o Tiktok. Este patrón de diseño destaca por reducir ofrecer una respuesta visual inmediata y convertir procesos de decisión complejos en interacciones lúdicas e intuitivas.

El presente proyecto nace de la convergencia de estas dos realidades: la necesidad de agilizar la elección de contenido de ocio en grupo y el aprovechamiento de una interfaz de swipe sincronizada en tiempo real.

### 1.2. Problema o necesidad detectada
El problema principal que aborda este proyecto es la parálisis por elección o choice overload que ocurre en reuniones sociales presenciales, ya sean parejas, grupos de amigos o familiares al intentar seleccionar una película, serie o videojuego para disfrutar en conjunto.

Esta problemática se manifiesta a través de los siguientes factores:

* **Pérdida de tiempo:** Inversión de períodos prolongados (a menudo superiores a 30 minutos) navegando por los catálogos de distintas plataformas sin llegar a un acuerdo.
* **Fricción e indecisión grupal:** Conflictos o discusiones derivadas de opiniones encontradas, donde el debate abierto perjudica la experiencia de ocio.
* **Sesgo de visibilidad:** Tendencia a elegir siempre los mismos títulos o recomendaciones principales de las plataformas por fatiga de búsqueda, ignorando opciones del catálogo que complacerían a todos.
* **Ausencia de herramientas:** Inexistencia de una solución unificada que aplique esta dinámica tanto al sector cinematográfico como al de los videojuegos multijugador o cooperativos locales.
### 1.3. Propuesta de solución
La solución propuesta consiste en el diseño y desarrollo de una aplicación móvil multiplataforma que automatiza el proceso de toma de decisiones en grupo.

El funcionamiento del sistema se basa en la creación de salas locales sincronizadas en tiempo real. El anfitrión crea una sala mediante un código único o código QR y configura unos filtros previos como el tipo de contenido y las plataformas activas. Los participantes se unen a la sala desde sus propios dispositivos móviles y comienzan a deslizar una lista limitada de opciones (Like hacia un lado, Pass hacia el otro).

Mediante un algoritmo de coincidencia (match), en el momento en que se detecta unanimidad (o la mayor puntuación ponderada), la aplicación detiene el proceso y muestra de forma destacada la opción elegida, indicando además la plataforma o medio en el que está disponible para su consumo inmediato.

### 1.4. Objetivos del proyecto

#### 1.4.1. Objetivo general

Diseñar, desarrollar e implementar una aplicación móvil multiplataforma que facilite la toma de decisiones grupales en la elección de películas, series y videojuegos, mediante una interfaz de deslizamiento de tarjetas (swipe) sincronizada en tiempo real entre múltiples dispositivos conectados a una misma sala virtual.

#### 1.4.2. Objetivos específicos

Analizar y definir los requisitos del sistema, identificando las necesidades clave de usabilidad (UX/UI) y sincronización en tiempo real.
Integrar la aplicación con APIs externas de catálogos de entretenimiento (como TMDB para cine/series e IGDB para videojuegos) para mantener información, portadas y metadatos actualizados.
Desarrollar una arquitectura de backend en tiempo real (utilizando WebSockets o bases de datos en tiempo real) capaz de gestionar salas simultáneas con baja latencia.
Implementar un flujo de entrada sin fricción, permitiendo la autenticación anónima para que los usuarios puedan unirse a las salas mediante código PIN o código QR sin necesidad de registros extensos.
Diseñar e implementar el algoritmo de asignación y cálculo de coincidencia (match), contemplando modalidades por unanimidad y por votación ponderada.
Realizar pruebas de integración, rendimiento y usabilidad en dispositivos con sistemas operativos Android e iOS para validar la experiencia de usuario.
### 1.5. Alcance del proyecto

El alcance del proyecto abarca las siguientes áreas funcionales y técnicas:

Módulo de Gestión de Salas: Creación, configuración, cierre y unión a salas mediante código numérico único de 4 a 6 dígitos o escaneo de código QR.
Módulo de Filtros Previos: Definición de parámetros de búsqueda (modo película/juego, plataformas de streaming/consola disponibles, número de jugadores y géneros.
Módulo de Interacción (Swipe): Interfaz gráfica interactiva para el deslizamiento de tarjetas con gestos táctiles, limitando el mazo a una cantidad optimizada de cartas por ronda.
Sincronización en Tiempo Real: Comunicación bi-direccional entre el servidor y los móviles de la sala para detectar coincidencias al instante.
Módulo de Resultados e Información: Pantalla de victoria (Match) que muestra las plataformas donde consumir el contenido.
Compatibilidad Multiplataforma: Despliegue funcional en dispositivos móviles Android e iOS.
### 1.6. Limitaciones y exclusiones

Limitaciones
Dependencia de APIs de terceros: La disponibilidad, precisión y actualización del catálogo de películas y videojuegos dependerá directamente de los tiempos de respuesta y límites de consulta (rate limits) de las APIs externas (TMDB e IGDB).
Conectividad a Internet: Aunque la sala se denomine "local" por la proximidad física de los usuarios, la sincronización requiere una conexión activa a Internet para la comunicación con la base de datos en la nube.
Exclusiones
Reproducción de contenido directo: La aplicación no actuará como plataforma de reproductor de vídeo ni ejecutor de juegos (cloud gaming), su alcance se limita estrictamente a la facilitación de la decisión.
Gestión de compras o suscripciones integradas: No se procesarán pagos dentro de la app ni se gestionarán las suscripciones de los usuarios a las plataformas de streaming.
Red social persistente: En esta versión del proyecto no se incluirá un sistema de mensajería interna, chat global ni listas de amigos permanentes entre salas.
### 1.7. Estructura de la memoria



## 2. ANÁLISIS DEL CONTEXTO Y VIABILIDAD

### 2.1. Sector profesional y perfil de usuarios

El proyecto se encuadra en el sector del desarrollo de software móvil y soluciones digitales para el ocio y entretenimiento. Se sitúa en la intersección entre las aplicaciones de recomendación de contenido y las herramientas de toma de decisiones grupales. El público objetivo se divide en dos perfiles principales:

Usuario Principal (Gen Z y Millennials, 18-35 años): Nativos o adoptantes digitales avanzados, consumidores habituales de plataformas de streaming (Netflix, HBO Max, Disney+, Prime Video) y servicios de videojuegos (Xbox Game Pass, PlayStation Plus, Steam). Acostumbrados a la navegación por gestos en redes sociales y aplicaciones de citas y que valoran la inmediatez, la simplicidad visual y la ausencia de fricciones (como formularios de registro largos).

Usuario Secundario (Grupos familiares, amigos y parejas): Usuarios de diversa edad que buscan una herramienta funcional para resolver rápidamente la elección de ocio en el hogar durante los fines de semana o momentos de reunión.

### 2.2. Análisis de la necesidad El crecimiento de los catálogos ha generado la paradoja de la elección: a mayor cantidad de opciones, mayor es la fatiga cognitiva y el tiempo requerido para tomar una decisión.

El análisis de esta necesidad revela tres puntos de dolor fundamentales:

* **Sesgo de grupo y dominante:** En las discusiones abiertas, la decisión suele inclinarse hacia la persona más firme del grupo, dejando insatisfechos a otros integrantes.
* **Tiempo de búsqueda desproporcionado:** El tiempo invertido en seleccionar qué ver o a qué jugar llega a consumir una fracción significativa del tiempo libre total disponible.
* **Falta de una solución transversal:** Las soluciones actuales suelen limitarse exclusivamente al cine o carecen de capacidades sincrónicas locales y transversales que incluyan videojuegos cooperativos/multijugador.
