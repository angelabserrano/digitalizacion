# UD4. Aplicación de la inteligencia artificial

## 1. Qué es la inteligencia artificial

La **inteligencia artificial (IA)** es la disciplina que desarrolla sistemas capaces de realizar tareas que, si las hiciera una persona, requerirían inteligencia: reconocer imágenes, entender lenguaje natural, tomar decisiones, aprender de la experiencia.

Es útil distinguir dos niveles:

- **IA débil (o estrecha)**: sistemas diseñados para realizar una tarea concreta y específica, aunque lo hagan muy bien (reconocer caras en una foto, recomendar productos, traducir un texto). **Es la única IA que existe hoy en día de forma real y aplicada.**
- **IA fuerte (o general)**: una hipotética inteligencia artificial con capacidad de razonamiento general, comparable o superior a la humana en cualquier tarea intelectual. Es, por ahora, un objetivo teórico y de investigación, no una realidad disponible.

!!! tip "Cuidado con el lenguaje"
    Es habitual atribuir a los sistemas de IA actuales cualidades como "entender" o "pensar". En realidad son sistemas estadísticos muy sofisticados que identifican patrones en enormes cantidades de datos; no tienen consciencia ni comprensión en el sentido humano del término, aunque su comportamiento pueda parecerlo.

### 1.1. Breve contexto histórico

El término "inteligencia artificial" se acuñó en 1956. Desde entonces el campo ha vivido alternancia de fases de gran expectación y fases de estancamiento (los llamados "inviernos de la IA"), hasta el impulso reciente provocado por tres factores que han convergido en la última década: la disponibilidad de enormes volúmenes de datos (Big Data, UD2), la capacidad de cómputo necesaria para procesarlos (impulsada en buena parte por la computación en la nube, UD3) y avances en las técnicas de aprendizaje automático.

## 2. Machine learning y deep learning

- **Aprendizaje automático (*machine learning*)**: en lugar de programar explícitamente todas las reglas de un sistema, se le proporcionan datos de ejemplo para que "aprenda" a partir de ellos los patrones necesarios para resolver una tarea.
- **Aprendizaje profundo (*deep learning*)**: subconjunto del aprendizaje automático basado en redes neuronales artificiales con muchas capas, inspiradas de forma simplificada en el funcionamiento del cerebro. Es la técnica que ha impulsado los avances más recientes, especialmente en reconocimiento de imágenes, voz y generación de lenguaje.

### 2.1. Tipos de aprendizaje automático

| Tipo | Cómo funciona | Ejemplo |
|---|---|---|
| **Supervisado** | Se entrena con datos ya etiquetados (entrada + resultado correcto conocido) | Clasificar un correo como spam o no spam, a partir de miles de correos ya etiquetados |
| **No supervisado** | Se entrena con datos sin etiquetar; el sistema busca patrones o agrupaciones por sí mismo | Segmentar clientes en grupos según su comportamiento de compra |
| **Por refuerzo** | El sistema aprende por ensayo y error, recibiendo una recompensa o penalización según el resultado de sus acciones | Un sistema que aprende a jugar a un videojuego, o un robot que aprende a caminar |

## 3. Aplicaciones de la IA por sectores

Conectando con la digitalización sectorial vista en la UD1:

- **Industria**: control de calidad automatizado mediante visión artificial (detectar defectos en piezas), mantenimiento predictivo (analizando los datos generados por sensores IoT).
- **Salud**: apoyo al diagnóstico mediante análisis de imágenes médicas, predicción de riesgo de determinadas enfermedades, optimización de la gestión de listas de espera.
- **Atención al cliente**: chatbots y asistentes virtuales que resuelven consultas frecuentes, sistemas de recomendación personalizados en comercio electrónico.
- **Educación**: sistemas de tutoría adaptativa que ajustan el ritmo y la dificultad de los contenidos a cada estudiante, corrección automática de ejercicios.
- **Administración pública**: automatización de la tramitación de expedientes sencillos, detección de fraude en subvenciones o prestaciones, chatbots de atención ciudadana.
- **Transporte y logística**: optimización de rutas, mantenimiento predictivo de flotas, sistemas de conducción asistida o autónoma.

## 4. IA generativa

La **IA generativa** agrupa a los modelos capaces de crear contenido nuevo (texto, imágenes, audio, vídeo o código) en lugar de limitarse a clasificar o predecir sobre datos ya existentes. Es, con diferencia, el ámbito de la IA que más ha impactado en el uso cotidiano en los últimos años.

- **Modelos de lenguaje (LLM — *Large Language Models*)**: entrenados con enormes cantidades de texto, son capaces de generar texto coherente, responder preguntas, resumir documentos, traducir o incluso escribir código. Los asistentes conversacionales (*chatbots* basados en IA) son la aplicación más visible de estos modelos.
- **Generación de imágenes**: modelos capaces de crear imágenes a partir de una descripción textual.
- **Generación de audio y vídeo**: síntesis de voz realista, clonación de voz, generación o edición de vídeo.
- **Generación de código**: asistentes que ayudan a programadores a escribir, completar o depurar código.

!!! reto "Reto: pon a prueba un asistente de IA generativa"
    Usa un asistente conversacional basado en IA para realizar una tarea concreta relacionada con tus estudios (por ejemplo, que te explique un concepto técnico, o que te ayude a estructurar un documento). Anota: ¿la respuesta fue correcta al 100%? ¿Detectaste algún error o "invención" (lo que se conoce como *alucinación*)? ¿Cómo verificarías la información antes de darla por buena?

### 4.1. Limitaciones de la IA generativa

- **Alucinaciones**: los modelos pueden generar información que suena plausible pero es incorrecta o directamente inventada, presentada con total seguridad.
- **Desactualización**: un modelo entrenado con datos hasta una fecha determinada no conoce, por defecto, información posterior a ese momento.
- **Falta de razonamiento verificable**: el modelo no "comprueba" hechos como lo haría una persona consultando fuentes; genera la respuesta estadísticamente más probable según sus datos de entrenamiento.

Por ello, un principio fundamental en el uso profesional de la IA generativa es la **verificación humana** de sus resultados, especialmente en información crítica.

## 5. Ética y regulación de la inteligencia artificial

### 5.1. Sesgos algorítmicos

Un sistema de IA aprende de los datos con los que se entrena. Si esos datos reflejan sesgos históricos o sociales (por ejemplo, discriminación pasada en procesos de contratación), el sistema puede **reproducir e incluso amplificar** esos sesgos, aunque no exista intención discriminatoria por parte de quien lo desarrolla. Es un riesgo especialmente relevante en aplicaciones como la selección de personal, la concesión de créditos o la valoración de riesgo penal.

### 5.2. Transparencia y explicabilidad

Muchos modelos de IA, especialmente los basados en *deep learning*, funcionan como "cajas negras": es difícil explicar exactamente por qué han llegado a una conclusión concreta. Esto plantea problemas cuando la IA se usa para tomar decisiones que afectan a derechos de las personas (por ejemplo, denegar un préstamo), donde suele exigirse poder explicar el motivo de la decisión.

### 5.3. El Reglamento europeo de Inteligencia Artificial (AI Act)

La Unión Europea ha aprobado un reglamento específico para regular el desarrollo y uso de sistemas de IA, que clasifica los sistemas según su **nivel de riesgo**:

- **Riesgo inaceptable**: sistemas prohibidos por vulnerar derechos fundamentales (por ejemplo, sistemas de puntuación social por parte de gobiernos, o determinadas formas de manipulación subliminal).
- **Riesgo alto**: sistemas usados en ámbitos sensibles (selección de personal, evaluación crediticia, infraestructuras críticas, sistemas relacionados con procesos judiciales o educativos), sujetos a requisitos estrictos de transparencia, supervisión humana y gestión de riesgos.
- **Riesgo limitado**: sistemas sujetos sobre todo a obligaciones de transparencia (por ejemplo, informar a la persona usuaria de que está interactuando con un chatbot, o de que un contenido ha sido generado o manipulado por IA).
- **Riesgo mínimo o nulo**: la mayoría de aplicaciones actuales (filtros antispam, videojuegos con IA), sin requisitos específicos adicionales.

## 6. IA responsable en el entorno profesional

Algunas buenas prácticas para el uso profesional de herramientas de IA:

- **Verificar siempre** la información generada antes de utilizarla, especialmente en contextos con consecuencias reales.
- **No introducir datos confidenciales o personales** en herramientas de IA generativa de terceros sin conocer su política de tratamiento de datos (conecta con la protección de datos que se estudia en la UD5).
- **Ser transparente** sobre el uso de IA cuando afecte a terceros (por ejemplo, indicar si un contenido ha sido generado o asistido por IA, cuando sea relevante).
- **Mantener supervisión humana** en decisiones importantes, evitando delegar por completo la responsabilidad en el sistema automático.
- **Respetar la propiedad intelectual**, tanto de los materiales usados para entrenar o alimentar un sistema de IA como del contenido que este genera, cuya titularidad y derechos de uso pueden estar sujetos a condiciones específicas.

---

## Actividades

<span class="actividad-titulo">**Actividad 4.1 — Clasifica el tipo de aprendizaje**</span>

Para cada uno de estos casos, indica si el aprendizaje automático empleado sería supervisado, no supervisado o por refuerzo, y justifica tu respuesta: (a) un sistema que agrupa noticias similares sin que nadie le haya dicho previamente las categorías; (b) un sistema que aprende a jugar al ajedrez jugando miles de partidas contra sí mismo; (c) un sistema que detecta tumores en radiografías entrenado con miles de imágenes ya diagnosticadas por especialistas.

<span class="actividad-titulo">**Actividad 4.2 — Detecta una alucinación**</span>

Pide a un asistente de IA generativa información muy específica sobre un tema que conozcas bien (una fecha, un dato técnico, una referencia bibliográfica). Comprueba si la respuesta es exacta. Si detectas un error, descríbelo y reflexiona sobre qué riesgo tendría no haberlo verificado.

<span class="actividad-titulo">**Actividad 4.3 — Nivel de riesgo según el AI Act**</span>

Clasifica cada uno de estos sistemas de IA según los niveles de riesgo del Reglamento europeo de IA (inaceptable, alto, limitado o mínimo): un filtro de spam en el correo; un sistema que evalúa currículums para preseleccionar candidatos a un puesto de trabajo; un chatbot de atención al cliente de una tienda online; un sistema de puntuación social obligatorio implantado por un gobierno.

## Autoevaluación

??? question "1. ¿Qué diferencia hay entre IA débil e IA fuerte?"
    La IA débil está diseñada para realizar una tarea específica y es la única que existe realmente hoy en día. La IA fuerte sería una inteligencia artificial con capacidad de razonamiento general comparable a la humana en cualquier tarea; por ahora es solo un objetivo teórico, no una realidad disponible.

??? question "2. ¿Qué es el aprendizaje profundo (*deep learning*)?"
    Un subconjunto del aprendizaje automático basado en redes neuronales artificiales con muchas capas, que ha impulsado los avances recientes en reconocimiento de imágenes, voz y generación de lenguaje.

??? question "3. ¿Qué es una 'alucinación' en el contexto de la IA generativa?"
    Cuando un modelo genera información que suena plausible pero es incorrecta o inventada, presentándola con aparente seguridad, sin que exista intención de engañar por su parte: es una limitación técnica del propio modelo.

??? question "4. ¿Por qué pueden aparecer sesgos en un sistema de IA aunque no haya intención discriminatoria por parte de quien lo desarrolla?"
    Porque el sistema aprende de los datos con los que se entrena; si esos datos reflejan sesgos históricos o sociales, el modelo tiende a reproducirlos e incluso amplificarlos.

??? question "5. Según el Reglamento europeo de IA, ¿en qué categoría de riesgo se sitúan los sistemas usados en selección de personal o evaluación crediticia?"
    En la categoría de riesgo alto, sujeta a requisitos estrictos de transparencia, supervisión humana y gestión de riesgos.
