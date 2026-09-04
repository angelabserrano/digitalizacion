# UD3. La nube

[:material-arrow-left: Volver al índice de todas las unidades](index.md)

!!! abstract "Resultado de aprendizaje"
    **RA3.** Identifica sistemas basados en *cloud*/nube y su influencia en el desarrollo de los sistemas digitales.

## 1. Qué es la computación en la nube

La **computación en la nube (*cloud computing*)** es un modelo que permite acceder bajo demanda, a través de internet, a recursos informáticos compartidos (servidores, almacenamiento, bases de datos, redes, software) sin necesidad de que el usuario los posea ni los administre físicamente.

El **NIST** (Instituto Nacional de Estándares y Tecnología de EE. UU.) define cinco características esenciales que debe cumplir un servicio para considerarse "en la nube":

1. **Autoservicio bajo demanda**: el usuario puede contratar recursos (por ejemplo, un servidor) de forma automática, sin intervención humana del proveedor.
2. **Acceso amplio a la red**: los servicios son accesibles desde cualquier dispositivo con conexión a internet.
3. **Recursos compartidos (*pooling*)**: el proveedor sirve a múltiples clientes desde una misma infraestructura física, asignando recursos de forma dinámica según la demanda (multiarrendamiento o *multi-tenant*).
4. **Elasticidad rápida**: los recursos pueden aumentar o reducirse de forma ágil según las necesidades, dando la sensación de capacidad ilimitada.
5. **Servicio medido**: el uso de los recursos se monitoriza y se factura según el consumo real (pago por uso).

!!! tip "La nube no es "el ordenador de otro" sin más"
    Es cierto que, en último término, la nube consiste en centros de datos con servidores físicos gestionados por un proveedor. Pero lo que la caracteriza no es solo "que esté en otro sitio", sino el modelo de **autoservicio, elasticidad y pago por uso** que la distingue de simplemente alquilar un servidor físico dedicado.

!!! question "💡 Comprueba que lo has entendido"
    Una empresa alquila un servidor físico dedicado a un proveedor: tiene que pedirlo por teléfono, tarda dos días en estar listo y paga una cuota fija mensual lo use o no.

    **¿Cumple las cinco características de computación en la nube del NIST? Justifícalo.**

??? note "Ver respuesta"
    No. Fallan el **autoservicio bajo demanda** (hay que pedirlo por teléfono y esperar), la **elasticidad rápida** (no escala de forma ágil) y el **servicio medido / pago por uso** (cuota fija). Es alquilar hardware, no computación en la nube.

## 2. Funciones y posibilidades de la nube

Más allá de *dónde* están los recursos, conviene saber **para qué** se usa la nube.

### 2.1. Funciones principales

- **Almacenamiento e intercambio de información**: guardar archivos y datos y compartirlos entre personas, sedes o aplicaciones (Drive, OneDrive, repositorios de datos).
- **Procesamiento de datos**: ejecutar cálculos intensivos bajo demanda —análisis de *big data*, entrenamiento de modelos de IA, procesado de vídeo— sin comprar servidores.
- **Ejecución de aplicaciones**: alojar y servir aplicaciones web, APIs y servicios a los que se accede desde cualquier dispositivo.
- **Bases de datos gestionadas**: almacenar y consultar datos estructurados sin administrar el motor de base de datos.
- **Copia de seguridad y recuperación ante desastres**: mantener copias externas y poder restaurar el servicio si falla la infraestructura local (véase apartado 8).
- **Plataforma de desarrollo y despliegue**: entornos donde programar, probar y publicar software (integración y entrega continuas).
- **Servicios avanzados "as a service"**: IA, analítica, IoT o mensajería listos para integrar en las aplicaciones.

En los **sistemas conectados (IoT)**, la nube es habitualmente el lugar donde se reciben, almacenan y analizan los datos de los sensores, y desde donde se envían órdenes a los actuadores (véase UD2).

### 2.2. El trabajo en la nube

La nube ha cambiado la forma de trabajar en las organizaciones:

- **Colaboración en tiempo real**: varias personas editan a la vez un mismo documento, hoja de cálculo o presentación, con historial de versiones.
- **Acceso multidispositivo y multisede**: se trabaja con la misma información desde el ordenador de la oficina, el portátil de casa o el móvil.
- **Teletrabajo y equipos distribuidos**: la nube proporciona el escritorio, las aplicaciones y los datos allí donde haya conexión.
- **Escritorio como servicio (DaaS) y aplicaciones virtualizadas**: el puesto de trabajo se ejecuta en la nube y el dispositivo local actúa solo como terminal.
- **Entornos de desarrollo y pruebas** que se crean y se destruyen en minutos, sin montar servidores físicos.

!!! question "💡 Comprueba que lo has entendido"
    Una asesoría con tres oficinas quiere que su personal edite los mismos expedientes a la vez, acceda a ellos desde casa y no dependa de un servidor físico en una de las sedes.

    **Cita dos funciones o posibilidades de la nube que respondan a esta necesidad.**

??? note "Ver respuesta"
    Por ejemplo: **colaboración en tiempo real** sobre los mismos documentos con control de versiones; **acceso multidispositivo y multisede** a la información; **almacenamiento e intercambio de información** centralizado en la nube en lugar de en un servidor local; y, si procede, **escritorio como servicio (DaaS)** para trabajar desde casa.

## 3. Modelos de servicio: IaaS, PaaS y SaaS

Según qué capa de la infraestructura gestiona el proveedor y cuál gestiona el cliente, se distinguen tres modelos principales:

| Modelo | Qué proporciona el proveedor | Qué gestiona el cliente | Ejemplo |
|---|---|---|---|
| **IaaS** (*Infrastructure as a Service*) | Servidores virtuales, almacenamiento, redes | Sistema operativo, middleware, aplicaciones y datos | Una máquina virtual en Amazon EC2 o Azure Virtual Machines |
| **PaaS** (*Platform as a Service*) | Infraestructura + sistema operativo + entorno de ejecución (bases de datos, lenguajes de programación) | Solo la aplicación y los datos que despliega sobre esa plataforma | Google App Engine, Azure App Service |
| **SaaS** (*Software as a Service*) | Aplicación completa, lista para usar | Solo su configuración y sus datos | Gmail, Microsoft 365, Google Workspace |

Una forma habitual de visualizar la diferencia es pensar en el nivel de "capas" que gestiona cada uno: en un centro de datos propio (*on-premise*), la organización gestiona absolutamente todo (desde el edificio y la electricidad hasta la aplicación); a medida que se avanza de IaaS a PaaS y a SaaS, el proveedor va asumiendo más capas y el cliente se puede centrar cada vez más en su negocio y menos en la infraestructura técnica.

<figure markdown="span">
  ![Matriz de capas gestionadas por el cliente y por el proveedor en on-premise, IaaS, PaaS y SaaS](assets/img/ud3-iaas-paas-saas.svg){ width="720" }
  <figcaption>Al pasar de on-premise a IaaS, PaaS y SaaS, el proveedor asume cada vez más capas (naranja sólido) y el cliente gestiona menos (naranja claro).</figcaption>
</figure>

!!! reto "Reto: clasifica estos servicios"
    Clasifica cada uno de estos servicios como IaaS, PaaS o SaaS, y justifica tu respuesta: Dropbox, una máquina virtual alquilada en la que instalas tu propio sistema operativo, un servicio que te permite subir el código de tu aplicación web sin preocuparte del servidor donde se ejecuta, Netflix.

!!! question "💡 Comprueba que lo has entendido"
    Un equipo de desarrollo quiere publicar una aplicación web y no quiere ocuparse de instalar ni actualizar el sistema operativo ni el motor de base de datos, pero sí necesita desplegar su propio código.

    **¿Qué modelo de servicio le conviene: IaaS, PaaS o SaaS?**

??? note "Ver respuesta"
    **PaaS**: el proveedor aporta la infraestructura, el sistema operativo y el entorno de ejecución (bases de datos, lenguajes); el cliente solo gestiona su aplicación y sus datos. Con IaaS tendría que administrar el sistema operativo; con SaaS no podría desplegar código propio.

## 4. Modelos de despliegue

Además del modelo de servicio, hay que distinguir **quién tiene acceso** a la infraestructura en la nube:

- **Nube pública**: infraestructura compartida por múltiples clientes, gestionada por un proveedor externo (AWS, Azure, Google Cloud). Es la opción más económica y flexible, pero implica menos control directo sobre la infraestructura física.
- **Nube privada**: infraestructura de uso exclusivo de una única organización, ya sea alojada en sus propias instalaciones o gestionada por un tercero en exclusiva. Ofrece más control y personalización, a cambio de mayor coste e implicación técnica.
- **Nube híbrida**: combina nube pública y privada, permitiendo mover cargas de trabajo entre ambas según necesidades de coste, rendimiento o normativa (por ejemplo, mantener los datos más sensibles en la nube privada y usar la nube pública para picos de demanda).
- **Nube comunitaria**: infraestructura compartida por varias organizaciones con necesidades o requisitos comunes (por ejemplo, varios organismos públicos de una misma administración).

!!! question "💡 Comprueba que lo has entendido"
    Un hospital quiere guardar las historias clínicas en infraestructura de uso exclusivo y bajo su control, pero usar servidores de un gran proveedor para absorber los picos de la web de cita previa.

    **¿Qué modelo de despliegue describe esta situación?**

??? note "Ver respuesta"
    **Nube híbrida**: combina una **nube privada** (datos sensibles bajo control exclusivo) con una **nube pública** (picos de demanda de la web), moviendo cargas entre ambas según coste, rendimiento o normativa.

## 5. Principales proveedores y soberanía digital

Los tres grandes proveedores globales de nube pública son **Amazon Web Services (AWS)**, **Microsoft Azure** y **Google Cloud Platform (GCP)**, que concentran la mayor parte del mercado mundial. Junto a ellos existen proveedores especializados o regionales, incluidos proveedores europeos (como OVHcloud o Ionos) que se promocionan destacando el cumplimiento estricto de la normativa europea de protección de datos.

Esto conecta con el concepto de **soberanía digital**: la capacidad de un país, una administración o una empresa de mantener el control sobre sus datos e infraestructuras digitales, sin depender en exceso de proveedores extranjeros sujetos a legislaciones distintas (por ejemplo, normativa de un tercer país que pudiera obligar a ese proveedor a facilitar acceso a los datos alojados, incluso si el cliente está en la Unión Europea). Es un factor cada vez más relevante en las decisiones de contratación de servicios en la nube por parte de administraciones públicas y empresas que manejan datos sensibles.

!!! question "💡 Comprueba que lo has entendido"
    Una administración pública europea descarta a un proveedor porque su matriz está sujeta a leyes de un tercer país que podrían obligarle a entregar datos alojados aunque el cliente esté en la UE.

    **¿Qué concepto está pesando en esa decisión?**

??? note "Ver respuesta"
    La **soberanía digital**: mantener el control sobre los datos y las infraestructuras propias sin quedar sujeto a legislaciones extranjeras. La **localización de los datos** y el cumplimiento del RGPD son factores relacionados.

## 6. Ventajas e inconvenientes de migrar a la nube

**Ventajas:**

- Reducción de la inversión inicial en infraestructura propia (se pasa de un gasto de capital, *CAPEX*, a un gasto operativo recurrente, *OPEX*).
- Escalabilidad casi inmediata ante picos de demanda.
- Acceso desde cualquier lugar y dispositivo.
- El proveedor se encarga del mantenimiento físico, las actualizaciones de seguridad de la infraestructura y, en muchos casos, de la disponibilidad garantizada mediante acuerdos de nivel de servicio (SLA).
- Facilita la colaboración y el trabajo distribuido.

**Inconvenientes:**

- **Dependencia del proveedor (*vendor lock-in*)**: cambiar de proveedor puede resultar técnica y económicamente costoso.
- Dependencia de la conectividad a internet: sin conexión, el acceso al servicio puede verse comprometido.
- Preocupaciones de seguridad y privacidad, especialmente con datos sensibles (se desarrolla en el apartado 9).
- Coste a largo plazo: el pago por uso puede acabar siendo más caro que una infraestructura propia bien dimensionada, si el uso es intensivo y constante en el tiempo.
- Cuestiones de soberanía digital, ya comentadas.

!!! question "💡 Comprueba que lo has entendido"
    Una empresa con una carga de trabajo intensiva y constante durante todo el año se plantea si migrarlo todo a la nube pública le saldrá más barato que su centro de datos actual, que está bien dimensionado.

    **¿Es necesariamente más barata la nube en este caso? ¿Qué otro riesgo debería valorar?**

??? note "Ver respuesta"
    No necesariamente: con uso **intensivo y constante**, el pago por uso puede acabar costando más que una infraestructura propia bien dimensionada. Además debería valorar el **vendor lock-in**: cambiar de proveedor más adelante puede ser técnica y económicamente costoso.

## 7. Del *cloud* al *edge*: edge computing, fog y mist

Enviar **todos** los datos a la nube no siempre es la mejor opción: si hay millones de sensores generando datos cada segundo, o si una máquina necesita reaccionar en milisegundos, esperar la ida y vuelta hasta un centro de datos lejano introduce **latencia**, consume **ancho de banda** y crea **dependencia de la conexión**. La respuesta es **acercar el procesamiento al lugar donde se generan los datos**.

### 7.1. Edge computing (computación en el borde)

El **edge computing** consiste en procesar los datos **en el propio dispositivo o muy cerca de él** (una pasarela, un pequeño servidor local, el propio sensor "inteligente"), en lugar de enviarlos todos a la nube. A la nube solo se envían los **resultados** o los datos que de verdad conviene conservar o analizar de forma global.

No sustituye a la nube, la **complementa**: el *edge* se encarga de la respuesta inmediata y del filtrado local; la nube, del almacenamiento histórico, el análisis a gran escala, el entrenamiento de modelos de IA y la gestión centralizada.

| | **Cloud computing** | **Edge computing** |
|---|---|---|
| Dónde se procesa | Centro de datos remoto | En el dispositivo o cerca de él |
| Latencia | Mayor (ida y vuelta por internet) | Muy baja (local) |
| Ancho de banda | Alto (se envía todo) | Bajo (se envía lo esencial) |
| Dependencia de la conexión | Alta | Baja: sigue funcionando sin conexión |
| Cómputo y almacenamiento | Prácticamente ilimitados | Limitados por el hardware local |
| Gestión y actualización | Centralizada y sencilla | Más compleja (muchos nodos distribuidos) |
| Coste | Pago por uso; sube con mucho tráfico | Inversión en hardware local |

**Ventajas del edge**: respuesta en tiempo real, menos tráfico de red, funcionamiento aunque falle la conexión y posibilidad de que los datos sensibles no salgan de las instalaciones (privacidad).

**Desventajas del edge**: menor capacidad de proceso y almacenamiento, mantenimiento y actualización más difíciles (muchos equipos repartidos) y necesidad de proteger físicamente los nodos.

Ejemplos: un vehículo autónomo que decide frenar sin consultar a un servidor; una cámara que reconoce una matrícula en local y solo sube el texto; una línea de producción que ajusta una máquina al instante.

### 7.2. Fog computing y mist computing

Entre el *edge* y la nube pueden existir **capas intermedias** que reparten el procesamiento según su urgencia y su alcance:

- **Fog computing (computación en la niebla)**: capa intermedia formada por nodos con cierta capacidad (pasarelas IoT, routers, pequeños servidores) situados en la **red local o de área**, entre los dispositivos y la nube. Agregan y preprocesan los datos de muchos dispositivos antes de decidir qué se resuelve localmente y qué sube a la nube. Zona de aplicación: una fábrica, un edificio, una subestación eléctrica, una *smart city* por barrios.
- **Mist computing (computación en la bruma)**: lleva el procesamiento **al extremo mismo de la red**, a los microcontroladores y sensores más simples. Realiza tareas mínimas (filtrar una lectura, disparar una alarma local) con muy poco consumo. Zona de aplicación: el propio nodo sensor, redes de sensores alimentadas por batería.

Visto en conjunto se forma un **continuo**: *mist* (sensor) → *edge* (dispositivo o pasarela) → *fog* (red local) → *cloud* (centro de datos). Cada capa asume la parte del trabajo para la que es más eficiente: cuanto más cerca del dato, menor latencia y menor consumo de red; cuanto más cerca de la nube, más capacidad y más visión global.

!!! question "💡 Comprueba que lo has entendido"
    Clasifica cada caso como *edge*, *fog*, *mist* o *cloud*:

    1. Un sensor de vibración que, con su microcontrolador, solo envía un aviso si supera un umbral.
    2. Un servidor en la propia fábrica que reúne los datos de todas las máquinas de una nave y decide qué sube al centro de datos.
    3. El entrenamiento de un modelo de IA con el histórico de dos años de toda la empresa.
    4. Un autómata de la línea que corrige la posición de un brazo en milisegundos.

??? note "Ver respuesta"
    1. **Mist** — procesamiento mínimo en el propio sensor.
    2. **Fog** — nodo intermedio en la red local que agrega y filtra.
    3. **Cloud** — gran capacidad de cómputo y visión global, sin urgencia de milisegundos.
    4. **Edge** — procesamiento junto a la máquina para responder en tiempo real.

## 8. Almacenamiento y copias de seguridad en la nube

El almacenamiento en la nube es uno de los servicios más extendidos, tanto a nivel personal (Google Drive, Dropbox, OneDrive) como profesional. Conviene distinguir:

- **Sincronización**: los archivos se mantienen actualizados y accesibles desde varios dispositivos en tiempo real.
- **Copia de seguridad (*backup*)**: copia adicional de los datos, pensada para poder recuperarlos si se pierden, se corrompen o son cifrados por un ataque de tipo *ransomware*. No es lo mismo sincronizar que respaldar: si un archivo sincronizado se borra o se cifra por error, ese cambio también se propaga a la nube, por lo que hace falta una estrategia de copias de seguridad con **versiones históricas**, no solo sincronización.

!!! tip "La regla 3-2-1"
    Una buena práctica de copias de seguridad consiste en mantener al menos **3 copias** de los datos, en **2 soportes distintos**, con **1 copia fuera de las instalaciones** (por ejemplo, en la nube). Aplicada a la nube: no basta con tener los datos solo en la nube ni solo en local; conviene combinar ambos.

!!! question "💡 Comprueba que lo has entendido"
    Un usuario tiene todas sus fotos en una carpeta sincronizada con la nube. Un *ransomware* cifra la carpeta local y, al instante, esos archivos cifrados se suben también a la nube.

    **¿Por qué la sincronización no le ha servido de copia de seguridad? ¿Qué le habría protegido?**

??? note "Ver respuesta"
    La sincronización **propaga cualquier cambio**, incluido el cifrado malicioso: la copia de la nube queda igual de inservible. Le habría protegido una **copia de seguridad con versiones históricas** (poder restaurar una versión anterior al ataque) y aplicar la **regla 3-2-1**.

## 9. Seguridad, privacidad y cumplimiento normativo en la nube

Un concepto clave para entender la seguridad en la nube es el **modelo de responsabilidad compartida**: el proveedor de la nube es responsable de la seguridad *de* la nube (la infraestructura física, la red, la virtualización), mientras que el cliente es responsable de la seguridad *en* la nube (la configuración de sus servicios, la gestión de accesos, el cifrado de sus propios datos, las copias de seguridad de su información). Un fallo de seguridad muy habitual no es un fallo del proveedor, sino una mala configuración por parte del cliente (por ejemplo, dejar un almacenamiento en la nube accesible públicamente por error).

Aspectos normativos relevantes en el contexto europeo y español:

- **RGPD** (Reglamento General de Protección de Datos) y **LOPDGDD** (Ley Orgánica de Protección de Datos Personales y garantía de los derechos digitales): regulan el tratamiento de datos personales, también cuando se almacenan en la nube (se desarrolla con detalle en la UD5).
- **Localización de los datos**: en qué país físico se encuentran los servidores donde se almacenan los datos, relevante por motivos legales y de soberanía digital.
- **Esquema Nacional de Seguridad (ENS)**: normativa española que establece los principios y requisitos de seguridad que deben cumplir las administraciones públicas, también aplicable cuando contratan servicios en la nube.

!!! question "💡 Comprueba que lo has entendido"
    Una empresa deja por error un almacenamiento en la nube accesible públicamente y se filtran datos de clientes. El proveedor alega que su infraestructura no ha fallado en ningún momento.

    **Según el modelo de responsabilidad compartida, ¿de quién es la responsabilidad?**

??? note "Ver respuesta"
    Del **cliente**. El proveedor responde de la seguridad *de* la nube (infraestructura física, red, virtualización); la **configuración de los servicios y la gestión de accesos** son seguridad *en* la nube, responsabilidad del cliente. Una mala configuración es el fallo más habitual.

## 10. Sostenibilidad y eficiencia de los centros de datos

Como se avanzó en la UD1, los centros de datos que sostienen la nube consumen cantidades muy significativas de electricidad y, en muchos casos, de agua para refrigeración. Los grandes proveedores de nube compiten actualmente por mejorar su eficiencia energética, mediante indicadores como el **PUE (*Power Usage Effectiveness*)**, que mide la relación entre la energía total consumida por un centro de datos y la que realmente utilizan sus equipos informáticos (cuanto más próximo a 1, más eficiente es el centro de datos), así como mediante el uso de energías renovables y la ubicación de centros de datos en climas fríos que reducen la necesidad de refrigeración activa.

!!! question "💡 Comprueba que lo has entendido"
    El centro de datos A tiene un PUE de 1,1 y el centro de datos B, un PUE de 1,8.

    **¿Cuál es más eficiente energéticamente y qué significa ese número?**

??? note "Ver respuesta"
    El **A** (PUE 1,1). El PUE es la relación entre la energía total que consume el centro de datos y la que usan realmente sus equipos informáticos: cuanto más cerca de 1, menos energía se "pierde" en refrigeración y otros usos. Un PUE de 1,8 significa que por cada vatio útil se consumen 0,8 adicionales.

---

## Actividades

<span class="actividad-titulo">**Actividad 3.1 — IaaS, PaaS o SaaS**</span>

Elabora una tabla con al menos seis servicios en la nube que utilices o conozcas (por ejemplo, Google Drive, un hosting web, Microsoft 365, una máquina virtual...) y clasifica cada uno según el modelo de servicio (IaaS, PaaS o SaaS) al que pertenece, justificando brevemente tu clasificación.

<span class="actividad-titulo">**Actividad 3.2 — Diseña tu estrategia de copias de seguridad**</span>

Aplicando la regla 3-2-1, diseña una estrategia de copias de seguridad para los archivos de un pequeño negocio (por ejemplo, una peluquería con un ordenador para la gestión de citas y facturación). Indica qué soportes usarías y con qué frecuencia harías las copias.

<span class="actividad-titulo">**Actividad 3.3 — Modelo de responsabilidad compartida**</span>

Busca información sobre un incidente de seguridad real relacionado con almacenamiento en la nube mal configurado (por ejemplo, un bucket de almacenamiento accesible públicamente por error). Explica si la responsabilidad fue del proveedor o del cliente, según el modelo de responsabilidad compartida.

<span class="actividad-titulo">**Actividad 3.4 — ¿Mist, edge, fog o cloud?**</span>

Para cada escenario, decide en qué capa se procesarían los datos y justifícalo en una línea:

1. Un coche autónomo que decide frenar ante un obstáculo.
2. El análisis del histórico de ventas de dos años de toda la empresa.
3. Un sensor de temperatura con batería que solo envía un aviso si supera un umbral.
4. Un servidor en una nave industrial que reúne los datos de todas sus máquinas y decide qué sube al centro de datos.
5. La copia de seguridad diaria de los archivos de la oficina.

## Mapa conceptual

<figure markdown="span">
  ![Mapa conceptual de la Unidad 3: la computación en la nube y sus tres ramas —concepto y niveles, funciones y uso en la empresa, y arquitecturas y retos](assets/img/ud3-mapa-conceptual.png){ width="960" }
  <figcaption>Síntesis de la unidad: la computación en la nube se aborda desde su <strong>concepto y niveles</strong> (definición, características del NIST, modelos de servicio IaaS/PaaS/SaaS y modelos de despliegue), sus <strong>funciones y uso en la empresa</strong> (procesar y almacenar datos, ejecutar aplicaciones, trabajo colaborativo, ventajas e inconvenientes y copias de seguridad) y sus <strong>arquitecturas y retos</strong> (del *cloud* al *edge*, *fog* y *mist*; seguridad y responsabilidad compartida; soberanía digital y sostenibilidad).</figcaption>
</figure>

## Autoevaluación

??? question "1. Cita las cinco características esenciales de la computación en la nube según el NIST."
    Autoservicio bajo demanda, acceso amplio a la red, recursos compartidos (*pooling*), elasticidad rápida y servicio medido (pago por uso).

??? question "2. ¿Qué diferencia hay entre IaaS y SaaS?"
    En IaaS el proveedor ofrece solo la infraestructura básica (servidores, almacenamiento, redes) y el cliente gestiona el sistema operativo, las aplicaciones y los datos. En SaaS el proveedor ofrece la aplicación completa lista para usar, y el cliente solo gestiona su configuración y sus datos.

??? question "3. ¿Qué es el *vendor lock-in*?"
    La dependencia de un proveedor concreto que dificulta, técnica o económicamente, migrar a otro proveedor distinto.

??? question "4. Explica la diferencia entre sincronización y copia de seguridad en la nube."
    La sincronización mantiene los archivos actualizados en tiempo real entre dispositivos, pero un borrado o cifrado accidental también se propaga. La copia de seguridad crea una copia adicional, normalmente con versiones históricas, pensada específicamente para poder recuperar los datos ante una pérdida o ataque.

??? question "5. ¿En qué consiste el modelo de responsabilidad compartida en la nube?"
    El proveedor es responsable de la seguridad *de* la nube (infraestructura física, red, virtualización); el cliente es responsable de la seguridad *en* la nube (configuración de sus servicios, gestión de accesos, cifrado y copias de seguridad de sus propios datos).

??? question "6. ¿Qué diferencia hay entre nube pública, privada e híbrida?"
    La nube pública es infraestructura compartida por múltiples clientes y gestionada por un proveedor externo. La nube privada es de uso exclusivo de una organización, con más control y más coste. La nube híbrida combina ambas, moviendo cargas entre una y otra según coste, rendimiento o normativa.

??? question "7. ¿Qué mide el PUE de un centro de datos y qué valor es mejor?"
    El PUE (*Power Usage Effectiveness*) mide la relación entre la energía total que consume el centro de datos y la que usan realmente sus equipos informáticos. Cuanto más próximo a 1, más eficiente es el centro de datos.

??? question "8. ¿En qué consiste la regla 3-2-1 de copias de seguridad?"
    Mantener al menos 3 copias de los datos, en 2 soportes distintos, con 1 copia fuera de las instalaciones (por ejemplo, en la nube).

??? question "9. ¿Qué es la soberanía digital?"
    La capacidad de un país, una administración o una empresa de mantener el control sobre sus datos e infraestructuras digitales, sin depender en exceso de proveedores extranjeros sujetos a legislaciones distintas.

??? question "10. Cita tres funciones principales de la nube."
    Por ejemplo: almacenamiento e intercambio de información, procesamiento de datos bajo demanda, ejecución de aplicaciones y APIs, bases de datos gestionadas, copia de seguridad y recuperación ante desastres, y plataforma de desarrollo y despliegue.

??? question "11. Indica dos posibilidades que ofrece la nube para el trabajo en la empresa."
    Por ejemplo: colaboración en tiempo real sobre los mismos documentos con historial de versiones, acceso multidispositivo y multisede a la información, teletrabajo y equipos distribuidos, o escritorio como servicio (DaaS).

??? question "12. ¿Qué es el *edge computing* y qué ventaja principal aporta frente al *cloud computing*?"
    Consiste en procesar los datos en el propio dispositivo o muy cerca de él, en lugar de enviarlos todos a la nube. Su ventaja principal es la **baja latencia** (respuesta en tiempo real), además de reducir el tráfico de red y poder seguir funcionando sin conexión. A cambio, tiene menos capacidad de cómputo y almacenamiento y es más difícil de mantener.

??? question "13. ¿Qué diferencia hay entre *fog* y *mist computing*?"
    El *fog computing* es una capa intermedia en la red local o de área (pasarelas, routers, pequeños servidores) que agrega y preprocesa los datos de muchos dispositivos antes de decidir qué sube a la nube. El *mist computing* lleva el procesamiento al extremo mismo de la red, a los microcontroladores y sensores más simples, para tareas mínimas y de muy bajo consumo.
