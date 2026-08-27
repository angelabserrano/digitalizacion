# UD5. Evaluación de datos

!!! abstract "Resultado de aprendizaje"
    **RA5.** Evalúa la importancia de los datos, así como su protección en una economía digital globalizada, definiendo sistemas de seguridad y ciberseguridad tanto a nivel de equipo/sistema, como globales.

## 1. El dato como activo

En una organización digitalizada, el **dato** se ha convertido en un activo con valor propio, comparable al de otros recursos económicos: se genera, se almacena, se procesa, se protege y, sobre todo, se utiliza para tomar decisiones. Pero un dato solo tiene valor real si se puede confiar en él: un dato incorrecto puede llevar a una decisión equivocada con más facilidad que la ausencia total de datos, precisamente porque transmite una falsa sensación de certeza.

Esta unidad se centra en cómo **evaluar** los datos: su calidad, cómo se analizan y visualizan para apoyar decisiones, y las obligaciones legales y éticas que implica su tratamiento, en particular cuando se trata de datos personales.

### 1.1. Ciclo de vida del dato

1. **Recogida**: captación del dato en origen (formularios, sensores IoT, transacciones, interacciones web).
2. **Almacenamiento**: en bases de datos, hojas de cálculo, *data lakes* o *data warehouses* (véase UD2).
3. **Procesamiento**: limpieza, transformación y combinación de datos de distintas fuentes.
4. **Análisis**: aplicación de técnicas estadísticas o de aprendizaje automático (véase UD4) para extraer conclusiones.
5. **Uso y difusión**: presentación de resultados (informes, paneles) y toma de decisiones basada en ellos.
6. **Conservación o eliminación**: los datos deben conservarse solo el tiempo necesario según su finalidad y la normativa aplicable, y eliminarse de forma segura cuando ya no proceda conservarlos.

<figure markdown="span">
  ![Diagrama circular con las seis fases del ciclo de vida del dato](assets/img/ud5-ciclo-dato.svg){ width="640" }
  <figcaption>Las seis fases del ciclo de vida del dato se encadenan de forma continua: la conservación o eliminación cierra el ciclo y la recogida de nuevos datos lo reinicia.</figcaption>
</figure>

## 2. Calidad del dato

Antes de analizar cualquier dato hay que preguntarse si es fiable. Las principales dimensiones de la **calidad del dato** son:

| Dimensión | Qué evalúa | Ejemplo de problema |
|---|---|---|
| **Exactitud** | Si el dato refleja fielmente la realidad | Una dirección postal mal escrita |
| **Completitud** | Si faltan datos que deberían estar presentes | Un formulario con el campo "teléfono" vacío en el 40% de los registros |
| **Consistencia** | Si el mismo dato se representa igual en distintos sistemas | Un mismo cliente registrado como "Juan Pérez" en un sistema y "J. Pérez García" en otro |
| **Actualidad** | Si el dato sigue siendo válido en el momento de usarlo | Un stock de almacén que no refleja las ventas del último día |
| **Unicidad** | Si existen registros duplicados | El mismo cliente dado de alta dos veces con datos ligeramente distintos |
| **Validez** | Si el dato cumple el formato o rango esperado | Una fecha de nacimiento en el futuro, o una edad de 250 años |

!!! reto "Reto: audita un conjunto de datos"
    Consigue (o te proporcionará el/la docente) una pequeña hoja de cálculo con datos de ejemplo que contenga errores intencionados. Identifica al menos un problema de cada una de las dimensiones de calidad anteriores.

### 2.1. Consecuencias de una mala calidad del dato

Una mala calidad del dato no es solo un problema técnico: tiene consecuencias organizativas y económicas — decisiones erróneas basadas en cifras poco fiables, pérdida de tiempo y recursos en corregir errores a posteriori, pérdida de confianza de clientes o usuarios, e incluso incumplimientos normativos si los datos personales tratados son incorrectos o están desactualizados.

## 3. Big Data y ciencia de datos

Como se introdujo en la UD2, el **Big Data** agrupa las técnicas y la infraestructura necesarias para manejar conjuntos de datos que, por su volumen, velocidad o variedad, superan la capacidad de las herramientas tradicionales. La **ciencia de datos (*data science*)** es la disciplina que se apoya en esa infraestructura para extraer conocimiento útil de los datos, combinando estadística, programación y conocimiento del negocio.

### 3.1. Etapas típicas de la ciencia de datos

1. **Definición del problema**: qué pregunta de negocio se quiere responder.
2. **Recogida y preparación de los datos**: captación, limpieza y transformación (conecta directamente con la calidad del dato vista en el punto 2).
3. **Exploración y análisis**: aplicación de técnicas estadísticas para detectar patrones.
4. **Modelado**: cuando el volumen y la complejidad de los datos lo justifican, se recurre a técnicas de **aprendizaje automático (*machine learning*)** y **aprendizaje profundo (*deep learning*)** — vistas en detalle en la UD4 — para construir modelos capaces de clasificar, predecir o agrupar datos de forma automática.
5. **Comunicación de resultados**: presentación de conclusiones mediante visualización (punto 4) o paneles de control.

!!! tip "Big Data, machine learning y deep learning: cómo encajan"
    El Big Data aporta el volumen y la infraestructura de datos; el machine learning y el deep learning (UD4) son las técnicas que permiten extraer patrones de ese volumen de datos cuando la relación entre variables es demasiado compleja para un análisis estadístico tradicional. Cuantos más datos de calidad estén disponibles, mejor suele funcionar un modelo de aprendizaje automático: por eso ambas tecnologías están tan estrechamente ligadas en la práctica.

### 3.2. Almacenamiento en la nube y ciencia de datos

El procesamiento y almacenamiento de grandes volúmenes de datos rara vez se realiza sobre infraestructura local: el **cloud computing**, estudiado en profundidad en la UD3, ofrece el almacenamiento elástico y el potencial de cómputo bajo demanda que la ciencia de datos necesita, sin obligar a la organización a invertir en infraestructura propia dimensionada para los picos de carga.

## 4. Análisis de datos y Business Intelligence

El **Business Intelligence (BI)** o inteligencia de negocio es el conjunto de estrategias, procesos y herramientas orientadas a transformar datos en información útil para la toma de decisiones.

### 3.1. Niveles de análisis de datos

1. **Análisis descriptivo**: ¿qué ha pasado? Resume datos históricos (por ejemplo, ventas del último trimestre por región).
2. **Análisis diagnóstico**: ¿por qué ha pasado? Busca las causas de un fenómeno observado (por ejemplo, por qué han caído las ventas en una región concreta).
3. **Análisis predictivo**: ¿qué es probable que pase? Utiliza datos históricos y técnicas estadísticas o de aprendizaje automático (UD4) para anticipar tendencias futuras.
4. **Análisis prescriptivo**: ¿qué se debería hacer? Va un paso más allá del predictivo, sugiriendo acciones concretas para lograr o evitar un resultado.

## 5. Visualización de datos

Presentar los datos de forma visual facilita su interpretación y la detección de patrones que resultan difíciles de ver en una tabla de cifras. Algunos principios básicos:

- **Elegir el tipo de gráfico adecuado al dato**: por ejemplo, un gráfico de líneas para mostrar evolución en el tiempo, un gráfico de barras para comparar categorías, un mapa para datos geográficos.
- **Evitar la sobrecarga visual**: incluir solo la información relevante para el mensaje que se quiere transmitir.
- **No distorsionar la percepción**: por ejemplo, truncar el eje vertical de un gráfico de barras puede exagerar visualmente diferencias que en realidad son pequeñas.
- **Etiquetar con claridad**: unidades, fuente de los datos y fecha de actualización.

Los **paneles de control (*dashboards*)** son la forma más habitual de poner esta visualización al servicio de la toma de decisiones continua en una organización, combinando varios indicadores clave (**KPI — *Key Performance Indicators***) en una sola vista actualizada.

!!! tip "Herramientas habituales"
    Desde hojas de cálculo con tablas y gráficos dinámicos (Excel, Google Sheets), hasta herramientas específicas de BI (Power BI, Tableau, Google Looker Studio) o soluciones *no-code/low-code* que permiten crear paneles sin necesidad de programar.

## 6. Protección de datos personales

Cuando los datos que se tratan son **datos personales** (información que identifica o permite identificar a una persona física), su tratamiento está sujeto a una normativa específica y estricta.

### 6.1. Marco normativo

- **RGPD** (Reglamento General de Protección de Datos, de aplicación en toda la Unión Europea).
- **LOPDGDD** (Ley Orgánica de Protección de Datos Personales y garantía de los derechos digitales), que desarrolla el RGPD en España.

### 6.2. Principios básicos del tratamiento de datos personales

- **Licitud, lealtad y transparencia**: solo se pueden tratar datos con una base legal (consentimiento, contrato, obligación legal, entre otras) y de forma comprensible para la persona afectada.
- **Limitación de la finalidad**: los datos se recogen para un fin determinado y explícito, y no deben usarse posteriormente para fines incompatibles con ese fin original.
- **Minimización de datos**: solo deben recogerse los datos estrictamente necesarios para la finalidad declarada.
- **Exactitud**: los datos deben mantenerse actualizados y correctos.
- **Limitación del plazo de conservación**: no deben conservarse más tiempo del necesario para la finalidad que justificó su recogida.
- **Integridad y confidencialidad**: deben protegerse mediante medidas técnicas y organizativas adecuadas (cifrado, control de accesos...).
- **Responsabilidad proactiva (*accountability*)**: quien trata los datos debe poder demostrar en todo momento que cumple estos principios.

### 6.3. Derechos de las personas (derechos ARSULI)

| Derecho | En qué consiste |
|---|---|
| **Acceso** | Saber qué datos propios se están tratando y con qué finalidad |
| **Rectificación** | Corregir datos inexactos o incompletos |
| **Supresión** ("derecho al olvido") | Solicitar que se eliminen los datos propios, cuando proceda |
| **Limitación** | Solicitar que se restrinja temporalmente el tratamiento de los datos, sin eliminarlos |
| **Portabilidad** | Recibir los datos propios en un formato estructurado para poder trasladarlos a otro proveedor |
| **Oposición** | Oponerse a un tratamiento concreto de los datos propios (por ejemplo, con fines de marketing) |

### 6.4. Datos especialmente protegidos

El RGPD establece una categoría de **datos especialmente sensibles** que requieren garantías reforzadas: origen étnico o racial, opiniones políticas, convicciones religiosas o filosóficas, afiliación sindical, datos genéticos y biométricos, datos relativos a la salud, y datos sobre la vida u orientación sexual.

## 7. Ética del dato

Cumplir la normativa es el mínimo exigible, pero no siempre es suficiente para un tratamiento verdaderamente responsable de los datos. La **ética del dato** plantea preguntas adicionales:

- ¿Es justo el uso que se hace de estos datos, aunque sea legal? (por ejemplo, un algoritmo de fijación de precios que discrimina según la capacidad de pago estimada del usuario).
- ¿Se ha obtenido un consentimiento realmente informado, o se ha "escondido" en condiciones que nadie lee?
- ¿Podrían los datos, combinados entre sí (aunque cada uno por separado parezca inocuo), permitir identificar o perjudicar a una persona? Este riesgo se conoce como **reidentificación**.
- ¿Se están utilizando los datos de forma proporcionada a la finalidad perseguida, o se recopila "por si acaso" mucho más de lo necesario?

## 8. Herramientas de tratamiento y evaluación de datos

- **Hojas de cálculo**: siguen siendo la herramienta más extendida para tratar y analizar datos de volumen moderado (filtros, tablas dinámicas, funciones de búsqueda y validación de datos).
- **Herramientas de BI y visualización**: Power BI, Tableau, Google Looker Studio, para construir paneles interactivos.
- **Herramientas *no-code/low-code*** de automatización y análisis, que permiten combinar y transformar datos de distintas fuentes sin necesidad de programación avanzada.
- **Lenguajes y entornos de análisis de datos** (por ejemplo, Python o R con bibliotecas especializadas), habituales en perfiles más técnicos para análisis avanzados o modelos predictivos.

---

## Actividades

<span class="actividad-titulo">**Actividad 5.1 — Auditoría de calidad de datos**</span>

A partir de una hoja de cálculo con datos de clientes (proporcionada en clase o construida por ti con al menos 20 registros ficticios e introduciendo errores deliberados), identifica y corrige al menos un problema de cada dimensión de calidad del dato estudiada.

<span class="actividad-titulo">**Actividad 5.2 — De datos a decisión**</span>

A partir de una tabla de ventas mensuales de una pequeña tienda (real o inventada), elabora un gráfico adecuado que permita responder a la pregunta "¿en qué mes deberíamos reforzar el stock del producto más vendido?" y redacta en dos líneas la conclusión que extraes.

<span class="actividad-titulo">**Actividad 5.3 — Caso RGPD**</span>

Una empresa envía publicidad por correo electrónico a antiguos clientes que nunca dieron su consentimiento expreso para recibir comunicaciones comerciales. Identifica qué principio(s) del RGPD se estarían incumpliendo y qué derecho podrían ejercer esos clientes para dejar de recibir esas comunicaciones.

## Autoevaluación

??? question "1. Cita al menos cuatro dimensiones de la calidad del dato."
    Exactitud, completitud, consistencia, actualidad, unicidad y validez (se consideran correctas cualesquiera cuatro).

??? question "2. ¿Qué relación existe entre el Big Data, la ciencia de datos y el aprendizaje automático (*machine learning*)?"
    El Big Data aporta el volumen y la infraestructura de datos; la ciencia de datos es la disciplina que extrae conocimiento útil de esos datos combinando estadística, programación y conocimiento del negocio; el aprendizaje automático y el aprendizaje profundo son las técnicas que la ciencia de datos utiliza, en la fase de modelado, para detectar patrones cuando la relación entre variables es demasiado compleja para un análisis estadístico tradicional.

??? question "3. Diferencia entre análisis descriptivo y análisis predictivo."
    El análisis descriptivo resume y explica qué ha ocurrido a partir de datos históricos. El análisis predictivo utiliza esos datos históricos y técnicas estadísticas o de aprendizaje automático para anticipar qué es probable que ocurra en el futuro.

??? question "4. ¿Qué son los derechos ARSULI?"
    Los derechos que el RGPD reconoce a las personas sobre sus datos personales: Acceso, Rectificación, Supresión, Limitación, Portabilidad y Oposición.

??? question "5. ¿Qué diferencia hay entre cumplir la normativa de protección de datos y actuar de forma éticamente responsable con los datos?"
    Cumplir la normativa es el requisito legal mínimo. La ética del dato va más allá, planteando si el uso de los datos es justo, si el consentimiento fue realmente informado, o si existe riesgo de reidentificar a una persona combinando datos aparentemente inocuos, aunque el tratamiento sea legal.

??? question "6. ¿Qué es la minimización de datos?"
    El principio según el cual solo deben recogerse y tratarse los datos estrictamente necesarios para la finalidad concreta declarada, evitando recopilar información adicional "por si acaso".
