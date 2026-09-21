# UD2. Tecnologías digitales habilitadoras

[:material-arrow-left: Volver al índice de todas las unidades](index.md)

!!! abstract "Resultado de aprendizaje"
    **RA2.** Caracteriza las tecnologías habilitadoras digitales necesarias para la adecuación/transformación de las empresas a entornos digitales describiendo sus características y aplicaciones.

## 1. Qué es una tecnología habilitadora

Se llaman **tecnologías digitales habilitadoras** (en inglés, *enabling technologies*) a aquellas tecnologías que, por sí mismas, no resuelven un problema concreto de un sector, pero **hacen posible** que se desarrollen soluciones digitales avanzadas en múltiples sectores a la vez. Son la base técnica sobre la que se construye la Industria 4.0 y, en general, la digitalización de los sectores productivos vista en la UD1.

En esta unidad estudiamos las principales: el Internet de las Cosas, el Big Data, la inteligencia artificial, los gemelos digitales, la robótica y automatización de procesos, blockchain, la realidad extendida, la impresión 3D, la conectividad avanzada (5G) y la ciberseguridad como tecnología transversal. La **inteligencia artificial** y la **computación en la nube** se presentan aquí de forma introductoria y se desarrollan en detalle en las UD4 y UD3, respectivamente. Al final de la unidad se analiza el impacto conjunto de estas tecnologías en la **productividad**, la **sostenibilidad** y la aparición de **nuevos mercados**.

<figure markdown="span">
  ![Nueve tecnologías digitales habilitadoras -IoT, Big Data, inteligencia artificial, gemelos digitales, robótica y automatización, blockchain, realidad extendida, impresión 3D y 5G-, con la ciberseguridad como tecnología transversal y la computación en la nube remitida a la UD3](assets/img/ud2-tecnologias-habilitadoras.svg){ width="820" }
  <figcaption>Las tecnologías digitales habilitadoras más importantes: la ciberseguridad protege al resto de forma transversal, mientras que la nube y la IA, por su peso, se estudian en detalle en las UD3 y UD4.</figcaption>
</figure>

!!! tip "Cómo se relacionan entre sí"
    Estas tecnologías raramente se usan aisladas: un sistema de mantenimiento predictivo típico combina **sensores IoT** (que generan datos), **big data** (que los almacena y procesa), **inteligencia artificial** (que detecta patrones de fallo) y **la nube** (donde se ejecuta todo el proceso).

## 2. Internet de las Cosas (IoT)

El **Internet de las Cosas (*Internet of Things*, IoT)** es la red de objetos físicos (sensores, electrodomésticos, vehículos, maquinaria industrial) equipados con capacidad de conexión que les permite recopilar y transmitir datos, y en muchos casos recibir órdenes, a través de internet.

### 2.1. Arquitectura básica de un sistema IoT

1. **Dispositivos y sensores**: capturan datos del entorno (temperatura, humedad, movimiento, localización, consumo eléctrico...).
2. **Conectividad**: los datos se transmiten mediante distintas tecnologías según el caso de uso — Wi-Fi, Bluetooth, redes móviles (4G/5G), o protocolos de bajo consumo como LoRaWAN, Zigbee o NB-IoT (pensados para dispositivos que envían pocos datos y deben durar años con batería).
3. **Plataforma / nube**: recibe, almacena y procesa los datos, a menudo en la nube (véase UD3).
4. **Aplicación**: capa que presenta la información al usuario o dispara acciones automáticas (una alarma, el encendido de un actuador, una notificación).

<figure markdown="span">
  ![Las cuatro capas de un sistema IoT: dispositivos y sensores, conectividad, plataforma o nube y aplicación](assets/img/ud2-arquitectura-iot.svg){ width="800" }
  <figcaption>El dato viaja desde los sensores hasta la aplicación, que puede devolver una orden a un actuador del entorno físico.</figcaption>
</figure>

### 2.2. Aplicaciones del IoT

| Ámbito | Ejemplos |
|---|---|
| Hogar (*smart home*) | Termostatos inteligentes, cerraduras conectadas, asistentes de voz |
| Ciudad (*smart city*) | Sensores de tráfico, contenedores de basura que avisan cuando están llenos, farolas que regulan su intensidad |
| Industria (IIoT) | Sensores de vibración y temperatura en maquinaria para mantenimiento predictivo |
| Agricultura de precisión | Sensores de humedad del suelo, estaciones meteorológicas (véase UD1) |
| Salud (*wearables*) | Pulseras y relojes que monitorizan constantes vitales |
| Logística | Trazabilidad de mercancías, sensores de temperatura en transporte de productos refrigerados |

!!! reto "Reto: identifica un sistema IoT"
    Piensa en un dispositivo IoT que uses o conozcas (una pulsera de actividad, un termostato inteligente, un contador de electricidad "inteligente"). Describe qué dato capta, cómo lo transmite y qué decisión o acción se toma con ese dato.

!!! question "💡 Comprueba que lo has entendido"
    Un invernadero coloca sondas de humedad en el suelo; cuando la humedad baja de un umbral, se abre automáticamente una electroválvula de riego y el agricultor recibe un aviso en el móvil.

    **Asocia cada elemento con su capa de la arquitectura IoT: dispositivos/sensores, conectividad, plataforma/nube y aplicación.**

??? note "Ver respuesta"
    - **Dispositivos/sensores**: las sondas de humedad del suelo (y la electroválvula, como actuador).
    - **Conectividad**: la red que transmite las lecturas (por ejemplo, LoRaWAN o Wi-Fi).
    - **Plataforma/nube**: el servicio que recibe los datos, guarda el histórico y los compara con el umbral.
    - **Aplicación**: la lógica que ordena abrir la válvula y envía el aviso al móvil del agricultor.

### 2.3. Objetos inteligentes, ciudades inteligentes y oportunidades de negocio

Cuando un objeto cotidiano incorpora sensores, conectividad y algo de capacidad de proceso, se convierte en un **objeto inteligente (*smart object*)**: sabe medir su entorno, comunicarse y, a veces, decidir por sí mismo (un termostato que aprende horarios, una máquina que pide su propio repuesto).

La suma de muchos objetos inteligentes en un entorno urbano da lugar a la **ciudad inteligente (*smart city*)**: tráfico, alumbrado, aparcamiento, riego de parques, recogida de residuos o calidad del aire gestionados con datos en tiempo real. Para el sector informático, la *smart city* es un **mercado en sí mismo**: despliegue de sensores, plataformas de datos, aplicaciones ciudadanas, integración de sistemas y analítica.

### 2.4. Ventajas y riesgos del IoT para las empresas

**Ventajas:**

- **Visibilidad en tiempo real** de procesos, activos y productos (dónde están y en qué estado).
- **Mantenimiento predictivo**: menos paradas no planificadas y menos averías graves.
- **Eficiencia**: se ajusta el consumo de energía, agua y materias primas al necesario; menos desplazamientos.
- **Calidad**: detección temprana de desviaciones en el proceso.
- **Nuevos servicios**: pago por uso, monitorización remota, servitización (véase UD1).
- **Decisiones basadas en datos** a lo largo de toda la cadena (convergencia IT-OT).

**Riesgos:**

- **Seguridad**: cada dispositivo conectado amplía la superficie de ataque; muchos equipos IoT mantienen contraseñas por defecto y se actualizan poco, y pueden acabar integrados en redes de bots (*botnets*).
- **Privacidad**: los sensores captan datos personales o de comportamiento que hay que proteger (RGPD, véase UD5).
- **Dependencia y disponibilidad**: si falla la conectividad o la plataforma, el proceso se resiente.
- **Interoperabilidad**: fabricantes y protocolos distintos dificultan integrarlo todo en un único sistema.
- **Coste y obsolescencia**: desplegar, mantener y sustituir miles de dispositivos, y gestionar sus residuos electrónicos.

!!! question "💡 Comprueba que lo has entendido"
    Una empresa de transporte instala sensores de temperatura y localización en todos sus camiones frigoríficos y los conecta a una plataforma en la nube.

    **Indica dos ventajas para la empresa y dos riesgos que debe vigilar.**

??? note "Ver respuesta"
    - **Ventajas** (dos cualesquiera): visibilidad en tiempo real de la flota y de la cadena de frío, alertas tempranas si la temperatura se desvía, mantenimiento predictivo de los equipos, posibilidad de ofrecer al cliente un servicio de trazabilidad.
    - **Riesgos** (dos cualesquiera): seguridad de los dispositivos (acceso no autorizado a la plataforma o a los camiones), privacidad de los datos de localización del personal, dependencia de la conectividad móvil, coste de mantener y renovar los sensores.

## 3. Big Data

El **Big Data** hace referencia a conjuntos de datos tan grandes, rápidos o variados que las herramientas tradicionales de gestión de bases de datos no son capaces de procesarlos eficientemente. Suele caracterizarse mediante las llamadas **"V" del Big Data**:

- **Volumen**: cantidad de datos generados (terabytes, petabytes...).
- **Velocidad**: rapidez con la que se generan y deben procesarse los datos (a veces en tiempo real).
- **Variedad**: diversidad de formatos — datos estructurados (tablas), semiestructurados (JSON, XML) y no estructurados (texto libre, imágenes, vídeo, audio).
- **Veracidad**: fiabilidad y calidad de los datos (datos incompletos, duplicados o erróneos afectan a las conclusiones).
- **Valor**: la utilidad real que se extrae de los datos; el objetivo final de todo el proceso.

### 3.1. Ciclo de vida del dato en Big Data

1. **Captación**: sensores IoT, transacciones, formularios web, redes sociales, registros de sistemas (*logs*).
2. **Almacenamiento**: bases de datos distribuidas, *data lakes* (almacenes de datos en bruto) y *data warehouses* (almacenes de datos estructurados y depurados para análisis).
3. **Procesamiento y análisis**: técnicas estadísticas, minería de datos y modelos de aprendizaje automático (véase UD4) para encontrar patrones.
4. **Visualización y toma de decisiones**: paneles de control (*dashboards*) e informes que traducen los resultados en decisiones de negocio (se profundiza en la UD5).

!!! tip "Relación con la UD5"
    El Big Data se centra en la infraestructura y las técnicas para *manejar* grandes volúmenes de datos; la evaluación de la calidad de esos datos, su análisis y su uso responsable se trabajan en profundidad en la UD5.

!!! question "💡 Comprueba que lo has entendido"
    Una cadena de tiendas analiza cada noche millones de tickets de compra (tablas), reseñas de clientes en texto libre y vídeo de las cámaras de sala; además, necesita que los datos de stock se procesen al instante.

    **¿Qué "V" del Big Data se reconocen en este caso?**

??? note "Ver respuesta"
    - **Volumen**: millones de tickets cada día.
    - **Variedad**: datos estructurados (tablas) y no estructurados (texto de reseñas, vídeo).
    - **Velocidad**: parte del procesamiento debe hacerse en tiempo real (stock).
    - Todavía habría que valorar la **veracidad** (calidad de los datos) para poder extraer **valor**.

## 4. Inteligencia artificial

La **inteligencia artificial (IA)** es la capacidad de un sistema informático para realizar tareas que normalmente requieren inteligencia humana: reconocer imágenes o voz, entender lenguaje natural, detectar patrones, predecir valores o tomar decisiones. El enfoque dominante hoy es el **aprendizaje automático (*machine learning*)**: en lugar de programar reglas explícitas, el sistema aprende a partir de grandes volúmenes de datos, de ahí su estrecha relación con el Big Data.

Como tecnología habilitadora, la IA aporta:

- **Automatización cognitiva**: tareas que no son puramente mecánicas — clasificar documentos, atender consultas, inspeccionar piezas mediante visión artificial.
- **Predicción**: mantenimiento predictivo, previsión de demanda, detección de fraude.
- **Optimización**: rutas de reparto, precios, consumo energético, planificación de la producción.

Por su peso específico, la IA se estudia en profundidad en la **UD4** (aplicaciones en el sector, relación con los datos, lenguajes de programación y retos).

!!! question "💡 Comprueba que lo has entendido"
    Un taller quiere que un sistema revise automáticamente las fotos de cada pieza fabricada y avise cuando detecte un defecto, aprendiendo a partir de miles de imágenes de piezas correctas y defectuosas.

    **¿Qué tecnología habilitadora se está aplicando y con qué otra se apoya?**

??? note "Ver respuesta"
    **Inteligencia artificial** (visión artificial mediante aprendizaje automático), que se apoya en el **Big Data**: necesita un gran conjunto de imágenes etiquetadas para aprender a distinguir una pieza correcta de una defectuosa.

## 5. Gemelos digitales

Un **gemelo digital (*digital twin*)** es una réplica virtual de un objeto, proceso o sistema físico, alimentada **en tiempo real** con los datos que envían sus sensores. No es solo un modelo 3D: el gemelo evoluciona con el elemento real y permite **simular** escenarios ("¿qué pasaría si…?") antes de actuar sobre el mundo físico.

Se habla de gemelo digital de un **componente** (un motor), de un **producto** completo (un vehículo), de un **proceso** (una línea de montaje) o de un **sistema** (una planta, un edificio, una ciudad).

Aplicaciones:

- **Diseño y prototipado**: probar variantes sin necesidad de fabricarlas.
- **Operación**: monitorizar el estado real del activo y anticipar fallos.
- **Optimización**: ensayar cambios de parámetros en el gemelo y trasladar al sistema real solo los que mejoran el resultado.
- **Formación**: entrenar al personal sobre la réplica, sin riesgo ni coste de parada.

El gemelo digital es un buen ejemplo de **convergencia de varias THD**: IoT (datos en tiempo real), Big Data (histórico), IA (predicción) y, a menudo, realidad extendida (visualización).

!!! question "💡 Comprueba que lo has entendido"
    Una fábrica crea una réplica virtual de su línea de envasado que recibe los datos de los sensores en directo. Antes de cambiar la velocidad de la cinta, prueba el cambio en la réplica y comprueba el efecto sobre la producción y el consumo.

    **¿Por qué esto es un gemelo digital y no un simple plano o modelo 3D?**

??? note "Ver respuesta"
    Porque está **conectado en tiempo real** con la línea física (a través de los sensores) y **evoluciona con ella**, lo que permite simular cambios sobre el estado real actual antes de aplicarlos. Un plano o un modelo 3D son estáticos y no reflejan lo que está ocurriendo ahora en la planta.

## 6. Robótica y automatización de procesos

- **Robótica industrial clásica**: robots programados para tareas repetitivas en entornos controlados (brazos robóticos en cadenas de montaje).
- **Robótica colaborativa (*cobots*)**: robots diseñados para trabajar codo con codo con personas, con sensores de seguridad que detienen su movimiento ante un contacto imprevisto.
- **Automatización robótica de procesos (RPA — *Robotic Process Automation*)**: software que imita las acciones de una persona sobre aplicaciones informáticas (rellenar formularios, copiar datos entre sistemas, generar informes) para automatizar tareas administrativas repetitivas, sin necesidad de robots físicos.

!!! question "💡 Comprueba que lo has entendido"
    Una gestoría quiere automatizar el traspaso de datos entre su programa de facturación y el de contabilidad, una tarea que hoy hace una persona copiando campos a mano.

    **¿Qué opción encaja mejor: robótica industrial, cobots o RPA? ¿Por qué?**

??? note "Ver respuesta"
    **RPA**: es una tarea administrativa, repetitiva y realizada sobre aplicaciones informáticas, sin ningún componente físico. No se necesitan robots (ni industriales ni colaborativos), sino software que reproduzca las acciones de la persona sobre esos programas.

## 7. Blockchain y tecnologías de registro distribuido

**Blockchain** (cadena de bloques) es una tecnología de registro distribuido: una base de datos compartida entre múltiples participantes (nodos), en la que la información se organiza en bloques enlazados criptográficamente, de forma que una vez registrado un dato resulta extremadamente difícil modificarlo sin que se detecte.

Características principales:

- **Descentralización**: no depende de una autoridad central única; la copia del registro se distribuye entre muchos nodos.
- **Inmutabilidad**: los bloques están enlazados criptográficamente y el registro se distribuye entre múltiples nodos, por lo que modificar información ya registrada resulta extremadamente difícil y, además, puede ser detectado.
- **Transparencia y trazabilidad**: todas las operaciones quedan registradas y son verificables.

Aplicaciones más allá de las criptomonedas: trazabilidad de la cadena de suministro (por ejemplo, seguir el origen de un alimento desde el productor hasta el punto de venta), contratos inteligentes (*smart contracts*, programas que ejecutan automáticamente cláusulas contractuales cuando se cumplen ciertas condiciones), certificación de documentos y títulos académicos.

!!! question "💡 Comprueba que lo has entendido"
    Una cooperativa quiere que cualquier consumidor pueda comprobar el recorrido de una botella de aceite desde el olivar hasta la tienda, sin depender de que la propia cooperativa "dé fe" de esos datos.

    **¿Qué propiedades de blockchain responden a esta necesidad?**

??? note "Ver respuesta"
    - **Descentralización**: el registro no depende de una única autoridad; lo mantienen varios nodos.
    - **Inmutabilidad**: una vez anotado un paso de la cadena, no se puede alterar sin que se detecte.
    - **Transparencia y trazabilidad**: cada operación queda registrada y es verificable por cualquiera.

    Un *smart contract* podría, además, liberar el pago al productor en cuanto se confirma la entrega.

## 8. Realidad virtual, aumentada y mixta

| Tecnología | Qué hace | Ejemplo de uso |
|---|---|---|
| **Realidad virtual (RV)** | Sumerge al usuario en un entorno totalmente digital, generalmente con gafas o cascos | Simuladores de formación (pilotaje, cirugía, manejo de maquinaria peligrosa) |
| **Realidad aumentada (RA)** | Superpone información digital sobre el entorno real, visible a través de una pantalla, gafas o cámara | Manual de reparación que muestra indicaciones superpuestas sobre la propia máquina |
| **Realidad mixta** | Combina elementos reales y virtuales que pueden interactuar entre sí | Diseño colaborativo de un producto donde varias personas manipulan un modelo 3D compartido |

Aplicaciones profesionales destacadas: formación de personal en entornos de riesgo sin peligro real, mantenimiento asistido (un técnico ve superpuestas las instrucciones sobre la propia máquina), diseño y prototipado virtual, y visitas o *showrooms* virtuales en comercio y turismo.

!!! question "💡 Comprueba que lo has entendido"
    Clasifica cada situación como RV, RA o realidad mixta:

    1. Un operario ve, a través de unas gafas, las instrucciones de reparación superpuestas sobre la máquina real.
    2. Un alumno de enfermería practica una intervención con un casco que le muestra un quirófano totalmente digital.
    3. Dos ingenieros en salas distintas manipulan a la vez el mismo modelo 3D, anclado sobre una mesa real.

??? note "Ver respuesta"
    1. **Realidad aumentada** — se añade información digital sobre el entorno real.
    2. **Realidad virtual** — el entorno es totalmente digital.
    3. **Realidad mixta** — objetos reales y virtuales conviven e interactúan entre sí.

## 9. Impresión 3D y fabricación aditiva

La **fabricación aditiva**, popularmente conocida como impresión 3D, construye objetos añadiendo material capa a capa (a partir de un diseño digital), frente a la fabricación tradicional o sustractiva (que parte de un bloque de material y elimina lo sobrante, como en el mecanizado).

Ventajas: permite prototipado rápido, personalización de piezas sin coste adicional de reconfiguración, fabricación bajo demanda (reduciendo la necesidad de almacenar stock) y producción descentralizada (fabricar la pieza cerca de donde se necesita, en lugar de transportarla).

Limitaciones: velocidad de producción más lenta que la fabricación en serie tradicional para grandes volúmenes, y limitaciones en los materiales disponibles según la tecnología de impresión.

!!! question "💡 Comprueba que lo has entendido"
    Un fabricante de maquinaria agrícola necesita una pieza de repuesto descatalogada para un tractor antiguo: solo necesita una unidad y la necesita pronto.

    **¿Por qué la fabricación aditiva encaja bien aquí y no lo haría para producir 50.000 unidades de esa misma pieza?**

??? note "Ver respuesta"
    Para **una pieza única y urgente** aprovecha sus ventajas: fabricación bajo demanda, sin utillaje ni reconfiguración, y producción cerca de donde se necesita. Para **50.000 unidades** pesan sus limitaciones: es más lenta que la fabricación en serie y el coste por pieza no compensa frente al moldeado o el mecanizado a gran escala.

## 10. Conectividad avanzada: 5G y redes de nueva generación

Las tecnologías anteriores (IoT masivo, realidad aumentada, vehículos autónomos, telecirugía) necesitan redes de comunicación con prestaciones que las generaciones anteriores de telefonía móvil no podían ofrecer. El **5G** aporta tres mejoras clave:

- **Mayor velocidad de transmisión** (banda ancha móvil mejorada).
- **Menor latencia** (tiempo de respuesta), crítica en aplicaciones que requieren reacción casi instantánea, como el control remoto de maquinaria o vehículos.
- **Mayor densidad de conexiones simultáneas**, necesaria para escenarios con miles de sensores IoT en un espacio reducido (una fábrica, un puerto).

!!! question "💡 Comprueba que lo has entendido"
    Relaciona cada necesidad con la mejora del 5G que la hace posible:

    1. Un puerto con decenas de miles de sensores en pocas hectáreas.
    2. El control remoto en tiempo real de una grúa desde una sala de operaciones.
    3. Descargar planos en alta resolución al móvil desde cualquier punto de la obra.

??? note "Ver respuesta"
    1. **Mayor densidad de conexiones simultáneas.**
    2. **Menor latencia** (tiempo de respuesta casi instantáneo).
    3. **Mayor velocidad de transmisión** (banda ancha móvil mejorada).

## 11. Impacto de las tecnologías habilitadoras en la empresa

### 11.1. Productividad y mejoras en los entornos IT y OT

Cada tecnología habilitadora mejora tanto la **parte de negocio (IT)** como la **parte de planta (OT)** y, sobre todo, la **conexión entre ambas** (véase UD1):

| Tecnología | Mejora en negocio (IT) | Mejora en planta (OT) |
|---|---|---|
| IoT / IIoT | Datos de operación disponibles para la gestión | Monitorización y control de máquinas |
| Big Data | Cuadros de mando, previsión de demanda | Análisis de los datos de proceso |
| Inteligencia artificial | Automatización de tareas administrativas, previsión | Visión artificial, mantenimiento predictivo |
| Gemelos digitales | Simulación de escenarios de negocio | Optimización de líneas y equipos |
| Robótica / RPA | RPA en procesos administrativos | Cobots y robots en producción |
| Blockchain | Contratos y pagos automáticos | Trazabilidad de la cadena de suministro |
| Impresión 3D | Catálogo bajo demanda, menos stock | Repuestos y utillaje fabricados en planta |
| 5G | Movilidad y acceso remoto | Conexión masiva de sensores, control en tiempo real |

En conjunto, las THD **reducen tiempos y errores, aumentan la calidad y permiten decidir más rápido**, porque el dato fluye sin fricción entre la planta y la gestión.

### 11.2. Tecnologías habilitadoras, sostenibilidad y eficiencia

Bien implantadas, las THD contribuyen a una **economía más sostenible y eficiente**:

- **Menos consumo de recursos**: sensores e IA ajustan el uso de energía, agua y materias primas al estrictamente necesario.
- **Menos residuos y desperdicio**: control de calidad temprano, mantenimiento predictivo (menos averías y piezas desechadas) y fabricación bajo demanda.
- **Menos transporte**: producción descentralizada (impresión 3D) y operación o mantenimiento en remoto (5G, realidad aumentada, gemelos digitales).
- **Economía circular**: la trazabilidad (blockchain, IoT) facilita reparar, reutilizar y reciclar.

**Contrapartida:** las propias THD consumen energía y generan residuos electrónicos (centros de datos, dispositivos IoT), por lo que su balance ambiental debe evaluarse caso a caso (*Green IT*, véase UD1).

### 11.3. Nuevos productos, servicios y mercados

Las THD no solo mejoran lo que ya se hacía: **abren mercados que antes no existían**:

- **Servitización y pago por uso**: vender el resultado (horas de máquina, aire comprimido, kilómetros) en lugar del producto.
- **Productos conectados**: electrodomésticos, vehículos o maquinaria que prestan servicios digitales después de la venta.
- **Plataformas y datos**: intermediar entre oferta y demanda o poner en valor datos agregados, con las debidas garantías.
- **Ciudades inteligentes**: gestión de tráfico, alumbrado, residuos o aparcamiento como oportunidad de negocio para empresas tecnológicas (sensores, plataformas, integración, analítica).
- **Fabricación personalizada**: series cortas y productos a medida a un coste asumible (impresión 3D, fabricación flexible).

!!! question "💡 Comprueba que lo has entendido"
    Un fabricante de compresores instala sensores en sus equipos, analiza los datos con IA y deja de vender la máquina: ahora cobra por el aire comprimido suministrado, con mantenimiento incluido.

    **Relaciona este caso con (a) una mejora de eficiencia/sostenibilidad y (b) un nuevo mercado.**

??? note "Ver respuesta"
    - **(a) Eficiencia y sostenibilidad**: el mantenimiento predictivo evita averías y alarga la vida de los equipos, y el ajuste fino del funcionamiento reduce el consumo energético.
    - **(b) Nuevo mercado**: pasa de un mercado de venta de producto a uno de **servicio (servitización / pago por uso)**, con ingresos recurrentes y una relación continua con el cliente.

## 12. La ciberseguridad como tecnología habilitadora transversal

Cuantos más dispositivos, sensores y sistemas se conectan, mayor es la **superficie de exposición** a ciberataques. Por eso la ciberseguridad no es una tecnología habilitadora "más", sino una condición necesaria para que todas las demás puedan desplegarse con confianza: sin garantías de seguridad, ninguna empresa conectará su maquinaria industrial a internet, ni ningún ciudadano confiará sus datos a un sistema digital. Este módulo dedica contenido específico a la seguridad en la nube (UD3) y a la protección de datos (UD5); aquí basta con retener que **la seguridad debe diseñarse desde el principio (*security by design*)**, no añadirse al final del proceso.

!!! question "💡 Comprueba que lo has entendido"
    Una empresa termina de desarrollar su plataforma IoT para conectar la maquinaria y, solo entonces, encarga una auditoría para "añadirle seguridad" antes de salir a producción.

    **¿Qué principio no se ha respetado y qué implica?**

??? note "Ver respuesta"
    No se ha aplicado la **seguridad desde el diseño (*security by design*)**: la protección debe formar parte de las decisiones desde el inicio del proyecto, no añadirse al final. Corregir fallos de arquitectura al terminar suele ser más caro, más lento y menos eficaz que haberlos evitado desde el principio.

---

## Actividades

<span class="actividad-titulo">**Actividad 2.1 — Diseña un sistema IoT**</span>

Elige un problema cotidiano (por ejemplo, controlar el riego de las plantas de tu casa, o saber si queda sitio libre en un parking). Diseña sobre el papel un sistema IoT que lo resuelva, indicando: qué sensor(es) usarías, cómo transmitirías los datos, dónde se almacenarían y qué acción se dispararía automáticamente.

<span class="actividad-titulo">**Actividad 2.2 — Investigación: tecnologías habilitadoras en una empresa real**</span>

Busca una noticia reciente sobre una empresa (española o internacional) que haya implantado alguna de las tecnologías estudiadas en esta unidad (IoT, big data, IA, gemelos digitales, RPA o robótica, blockchain, realidad aumentada, impresión 3D o 5G). Resume en cinco líneas qué problema resolvía y qué resultado obtuvo.

<span class="actividad-titulo">**Actividad 2.3 — Cuadro comparativo**</span>

Elabora una tabla que relacione cada una de las tecnologías habilitadoras estudiadas con al menos un sector productivo de la UD1 en el que tenga especial relevancia.

## Mapa conceptual

<figure markdown="span">
  ![Mapa conceptual de la Unidad 2: las tecnologías digitales habilitadoras y sus tres ramas —concepto y tipos, aplicación en las empresas, e implicaciones clave](assets/img/ud2-mapa-conceptual.png){ width="960" }
  <figcaption>Síntesis de la unidad: las tecnologías digitales habilitadoras se abordan desde su <strong>concepto y tipos</strong> (IoT, Big Data, IA, gemelos digitales, robótica y automatización, blockchain, realidad extendida, impresión 3D y 5G), su <strong>aplicación en las empresas</strong> (mejoras en negocio y planta, sectores y ejemplos de uso) y sus <strong>implicaciones clave</strong> (sostenibilidad y eficiencia, nuevos mercados, y retos y riesgos, entre ellos la ciberseguridad).</figcaption>
</figure>

## Autoevaluación

??? question "1. ¿Qué son las 'V' del Big Data? Cita al menos tres."
    Volumen, velocidad, variedad, veracidad y valor. (Se consideran correctas cualesquiera tres de las cinco.)

??? question "2. Diferencia entre un robot industrial clásico y un cobot."
    El robot industrial clásico trabaja en un entorno controlado y aislado de las personas, realizando tareas repetitivas programadas. El cobot (robot colaborativo) está diseñado para trabajar junto a personas, con sensores de seguridad que detienen su movimiento ante un contacto imprevisto.

??? question "3. ¿Qué característica de blockchain hace que sea difícil modificar un dato ya registrado?"
    Que los bloques están enlazados criptográficamente y el registro se distribuye entre múltiples nodos: modificar información ya registrada resulta extremadamente difícil y, además, puede ser detectado.

??? question "4. ¿Qué diferencia hay entre realidad virtual y realidad aumentada?"
    La realidad virtual sumerge al usuario en un entorno totalmente digital; la realidad aumentada superpone información digital sobre el entorno real, sin sustituirlo.

??? question "5. ¿Por qué el 5G es especialmente relevante para el Internet de las Cosas?"
    Porque ofrece mayor velocidad, menor latencia y capacidad para soportar un número muy elevado de dispositivos conectados simultáneamente, condiciones necesarias para escenarios de IoT masivo o aplicaciones que exigen respuesta casi instantánea.

??? question "6. Cita las cuatro capas de un sistema IoT."
    Dispositivos y sensores; conectividad; plataforma o nube; y aplicación. El dato viaja desde los sensores hasta la aplicación, que puede devolver una orden a un actuador.

??? question "7. ¿Qué es la RPA y en qué se diferencia de un robot físico?"
    La RPA (*Robotic Process Automation*) es software que imita las acciones de una persona sobre aplicaciones informáticas para automatizar tareas administrativas repetitivas (rellenar formularios, copiar datos entre sistemas). No hay ningún robot físico: todo ocurre dentro de los programas.

??? question "8. ¿Qué diferencia hay entre fabricación aditiva y fabricación sustractiva?"
    La fabricación aditiva construye el objeto añadiendo material capa a capa a partir de un diseño digital. La sustractiva parte de un bloque de material y elimina lo sobrante (por ejemplo, mediante mecanizado).

??? question "9. ¿Qué significa que la seguridad debe aplicarse *by design*?"
    Que la ciberseguridad se tiene en cuenta desde el principio del diseño de un sistema o proyecto, y no como un añadido final. Así se evitan fallos de arquitectura que después serían más caros y difíciles de corregir.

??? question "10. Cita dos ventajas y dos riesgos del IoT para una empresa."
    **Ventajas** (dos cualesquiera): visibilidad en tiempo real de procesos y activos, mantenimiento predictivo, eficiencia en el uso de recursos, nuevos servicios (pago por uso, monitorización remota). **Riesgos** (dos cualesquiera): mayor superficie de ataque, privacidad de los datos captados, dependencia de la conectividad y la plataforma, problemas de interoperabilidad, coste y obsolescencia de los dispositivos.

??? question "11. ¿Qué es un gemelo digital y en qué se diferencia de un modelo 3D?"
    Es una réplica virtual de un objeto, proceso o sistema físico conectada **en tiempo real** con él mediante sensores, que permite simular escenarios antes de actuar sobre el elemento real. A diferencia de un modelo 3D, que es estático, el gemelo digital evoluciona con el sistema real y refleja su estado actual.

??? question "12. Indica dos formas en que las tecnologías habilitadoras contribuyen a la sostenibilidad."
    Por ejemplo: ajustan el consumo de energía, agua y materias primas al necesario (sensores + IA); reducen residuos y desperdicio mediante control de calidad temprano y mantenimiento predictivo; disminuyen el transporte gracias a la producción descentralizada y la operación remota; facilitan la economía circular mediante la trazabilidad.

??? question "13. Pon un ejemplo de nuevo mercado u oportunidad de negocio generado por las THD."
    Por ejemplo: la servitización o pago por uso (vender horas de máquina en lugar del equipo), los productos conectados con servicios digitales posventa, las plataformas de datos, o los servicios para ciudades inteligentes (sensores, plataformas y analítica para tráfico, alumbrado o residuos).

??? question "14. ¿Qué aporta la inteligencia artificial como tecnología habilitadora?"
    Permite la **automatización** de tareas que no son puramente mecánicas (clasificar documentos, atender consultas, inspeccionar piezas por visión artificial), la **predicción** (mantenimiento predictivo, previsión de demanda, detección de fraude) y la **optimización** (rutas, precios, consumo energético, planificación). Aprende a partir de grandes volúmenes de datos, por lo que va unida al Big Data. Se estudia en detalle en la UD4.
