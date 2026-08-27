# UD3. La nube

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

## 2. Modelos de servicio: IaaS, PaaS y SaaS

Según qué capa de la infraestructura gestiona el proveedor y cuál gestiona el cliente, se distinguen tres modelos principales:

| Modelo | Qué proporciona el proveedor | Qué gestiona el cliente | Ejemplo |
|---|---|---|---|
| **IaaS** (*Infrastructure as a Service*) | Servidores virtuales, almacenamiento, redes | Sistema operativo, middleware, aplicaciones y datos | Una máquina virtual en Amazon EC2 o Azure Virtual Machines |
| **PaaS** (*Platform as a Service*) | Infraestructura + sistema operativo + entorno de ejecución (bases de datos, lenguajes de programación) | Solo la aplicación y los datos que despliega sobre esa plataforma | Google App Engine, Azure App Service |
| **SaaS** (*Software as a Service*) | Aplicación completa, lista para usar | Solo su configuración y sus datos | Gmail, Microsoft 365, Google Workspace |

Una forma habitual de visualizar la diferencia es pensar en el nivel de "capas" que gestiona cada uno: en un centro de datos propio (*on-premise*), la organización gestiona absolutamente todo (desde el edificio y la electricidad hasta la aplicación); a medida que se avanza de IaaS a PaaS y a SaaS, el proveedor va asumiendo más capas y el cliente se puede centrar cada vez más en su negocio y menos en la infraestructura técnica.

!!! reto "Reto: clasifica estos servicios"
    Clasifica cada uno de estos servicios como IaaS, PaaS o SaaS, y justifica tu respuesta: Dropbox, una máquina virtual alquilada en la que instalas tu propio sistema operativo, un servicio que te permite subir el código de tu aplicación web sin preocuparte del servidor donde se ejecuta, Netflix.

## 3. Modelos de despliegue

Además del modelo de servicio, hay que distinguir **quién tiene acceso** a la infraestructura en la nube:

- **Nube pública**: infraestructura compartida por múltiples clientes, gestionada por un proveedor externo (AWS, Azure, Google Cloud). Es la opción más económica y flexible, pero implica menos control directo sobre la infraestructura física.
- **Nube privada**: infraestructura de uso exclusivo de una única organización, ya sea alojada en sus propias instalaciones o gestionada por un tercero en exclusiva. Ofrece más control y personalización, a cambio de mayor coste e implicación técnica.
- **Nube híbrida**: combina nube pública y privada, permitiendo mover cargas de trabajo entre ambas según necesidades de coste, rendimiento o normativa (por ejemplo, mantener los datos más sensibles en la nube privada y usar la nube pública para picos de demanda).
- **Nube comunitaria**: infraestructura compartida por varias organizaciones con necesidades o requisitos comunes (por ejemplo, varios organismos públicos de una misma administración).

## 4. Principales proveedores y soberanía digital

Los tres grandes proveedores globales de nube pública son **Amazon Web Services (AWS)**, **Microsoft Azure** y **Google Cloud Platform (GCP)**, que concentran la mayor parte del mercado mundial. Junto a ellos existen proveedores especializados o regionales, incluidos proveedores europeos (como OVHcloud o Ionos) que se promocionan destacando el cumplimiento estricto de la normativa europea de protección de datos.

Esto conecta con el concepto de **soberanía digital**: la capacidad de un país, una administración o una empresa de mantener el control sobre sus datos e infraestructuras digitales, sin depender en exceso de proveedores extranjeros sujetos a legislaciones distintas (por ejemplo, normativa de un tercer país que pudiera obligar a ese proveedor a facilitar acceso a los datos alojados, incluso si el cliente está en la Unión Europea). Es un factor cada vez más relevante en las decisiones de contratación de servicios en la nube por parte de administraciones públicas y empresas que manejan datos sensibles.

## 5. Ventajas e inconvenientes de migrar a la nube

**Ventajas:**

- Reducción de la inversión inicial en infraestructura propia (se pasa de un gasto de capital, *CAPEX*, a un gasto operativo recurrente, *OPEX*).
- Escalabilidad casi inmediata ante picos de demanda.
- Acceso desde cualquier lugar y dispositivo.
- El proveedor se encarga del mantenimiento físico, las actualizaciones de seguridad de la infraestructura y, en muchos casos, de la disponibilidad garantizada mediante acuerdos de nivel de servicio (SLA).
- Facilita la colaboración y el trabajo distribuido.

**Inconvenientes:**

- **Dependencia del proveedor (*vendor lock-in*)**: cambiar de proveedor puede resultar técnica y económicamente costoso.
- Dependencia de la conectividad a internet: sin conexión, el acceso al servicio puede verse comprometido.
- Preocupaciones de seguridad y privacidad, especialmente con datos sensibles (se desarrolla en el punto siguiente).
- Coste a largo plazo: el pago por uso puede acabar siendo más caro que una infraestructura propia bien dimensionada, si el uso es intensivo y constante en el tiempo.
- Cuestiones de soberanía digital, ya comentadas.

## 6. Almacenamiento y copias de seguridad en la nube

El almacenamiento en la nube es uno de los servicios más extendidos, tanto a nivel personal (Google Drive, Dropbox, OneDrive) como profesional. Conviene distinguir:

- **Sincronización**: los archivos se mantienen actualizados y accesibles desde varios dispositivos en tiempo real.
- **Copia de seguridad (*backup*)**: copia adicional de los datos, pensada para poder recuperarlos si se pierden, se corrompen o son cifrados por un ataque de tipo *ransomware*. No es lo mismo sincronizar que respaldar: si un archivo sincronizado se borra o se cifra por error, ese cambio también se propaga a la nube, por lo que hace falta una estrategia de copias de seguridad con **versiones históricas**, no solo sincronización.

!!! tip "La regla 3-2-1"
    Una buena práctica de copias de seguridad consiste en mantener al menos **3 copias** de los datos, en **2 soportes distintos**, con **1 copia fuera de las instalaciones** (por ejemplo, en la nube). Aplicada a la nube: no basta con tener los datos solo en la nube ni solo en local; conviene combinar ambos.

## 7. Seguridad, privacidad y cumplimiento normativo en la nube

Un concepto clave para entender la seguridad en la nube es el **modelo de responsabilidad compartida**: el proveedor de la nube es responsable de la seguridad *de* la nube (la infraestructura física, la red, la virtualización), mientras que el cliente es responsable de la seguridad *en* la nube (la configuración de sus servicios, la gestión de accesos, el cifrado de sus propios datos, las copias de seguridad de su información). Un fallo de seguridad muy habitual no es un fallo del proveedor, sino una mala configuración por parte del cliente (por ejemplo, dejar un almacenamiento en la nube accesible públicamente por error).

Aspectos normativos relevantes en el contexto europeo y español:

- **RGPD** (Reglamento General de Protección de Datos) y **LOPDGDD** (Ley Orgánica de Protección de Datos Personales y garantía de los derechos digitales): regulan el tratamiento de datos personales, también cuando se almacenan en la nube (se desarrolla con detalle en la UD5).
- **Localización de los datos**: en qué país físico se encuentran los servidores donde se almacenan los datos, relevante por motivos legales y de soberanía digital.
- **Esquema Nacional de Seguridad (ENS)**: normativa española que establece los principios y requisitos de seguridad que deben cumplir las administraciones públicas, también aplicable cuando contratan servicios en la nube.

## 8. Sostenibilidad y eficiencia de los centros de datos

Como se avanzó en la UD1, los centros de datos que sostienen la nube consumen cantidades muy significativas de electricidad y, en muchos casos, de agua para refrigeración. Los grandes proveedores de nube compiten actualmente por mejorar su eficiencia energética, mediante indicadores como el **PUE (*Power Usage Effectiveness*)**, que mide la relación entre la energía total consumida por un centro de datos y la que realmente utilizan sus equipos informáticos (cuanto más próximo a 1, más eficiente es el centro de datos), así como mediante el uso de energías renovables y la ubicación de centros de datos en climas fríos que reducen la necesidad de refrigeración activa.

---

## Actividades

<span class="actividad-titulo">**Actividad 3.1 — IaaS, PaaS o SaaS**</span>

Elabora una tabla con al menos seis servicios en la nube que utilices o conozcas (por ejemplo, Google Drive, un hosting web, Microsoft 365, una máquina virtual...) y clasifica cada uno según el modelo de servicio (IaaS, PaaS o SaaS) al que pertenece, justificando brevemente tu clasificación.

<span class="actividad-titulo">**Actividad 3.2 — Diseña tu estrategia de copias de seguridad**</span>

Aplicando la regla 3-2-1, diseña una estrategia de copias de seguridad para los archivos de un pequeño negocio (por ejemplo, una peluquería con un ordenador para la gestión de citas y facturación). Indica qué soportes usarías y con qué frecuencia harías las copias.

<span class="actividad-titulo">**Actividad 3.3 — Modelo de responsabilidad compartida**</span>

Busca información sobre un incidente de seguridad real relacionado con almacenamiento en la nube mal configurado (por ejemplo, un bucket de almacenamiento accesible públicamente por error). Explica si la responsabilidad fue del proveedor o del cliente, según el modelo de responsabilidad compartida.

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
