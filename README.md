# Resistivimetrodedeteccionsuperficialv1.2

Dispositivo experimental de bajo costo para la adquisición de datos de resistividad eléctrica del subsuelo mediante técnicas de prospección geofísica con corriente continua.

## Descripción

El **Resistivímetro de detección superficial** es un dispositivo desarrollado para realizar mediciones de variables eléctricas del subsuelo y obtener los parámetros necesarios para la estimación de su resistividad.

El sistema emplea una plataforma Arduino junto con módulos especializados para la medición de tensión y corriente, así como un sistema de conmutación que permite realizar las diferentes etapas del proceso de medición.

El proyecto fue desarrollado con un enfoque de **instrumentación geofísica de bajo costo**, buscando facilitar la construcción, reproducción y evaluación experimental de un sistema destinado a aplicaciones de detección superficial.

## Antecedentes y finalidad

El desarrollo del dispositivo forma parte del proyecto de tesis:

> **“Desarrollo de un dispositivo de prospección geofísica para aplicaciones en arqueología forense”**

realizado en la **Escuela Nacional de Antropología e Historia (ENAH), México**.

El propósito de la investigación es evaluar la utilidad de un sistema de resistividad eléctrica de bajo costo para la identificación de contrastes eléctricos asociados con alteraciones subsuperficiales, particularmente dentro de contextos de interés para la prospección arqueológica y forense.

El dispositivo debe entenderse como una herramienta experimental de prospección geofísica y no como un sistema destinado, por sí mismo, a determinar la existencia de un contexto arqueológico o forense.

## Principio de funcionamiento

El sistema se basa en la aplicación de corriente eléctrica al subsuelo mediante electrodos y en la medición de la diferencia de potencial generada como consecuencia del flujo de corriente a través del terreno.

A partir de las variables eléctricas medidas es posible obtener la resistencia eléctrica y, de acuerdo con la configuración de electrodos empleada y el procedimiento de adquisición, calcular los parámetros necesarios para estudios de resistividad eléctrica.

La interpretación de los resultados depende de factores como:

* configuración del arreglo de electrodos;
* separación entre electrodos;
* propiedades eléctricas del terreno;
* humedad y condiciones ambientales;
* calidad del contacto entre los electrodos y el suelo;
* corriente utilizada durante la medición;
* características y limitaciones del sistema de adquisición.

## Arquitectura del dispositivo

El sistema está integrado principalmente por:

* **Arduino Uno R3**, como unidad de control;
* **ADS1115**, para adquisición diferencial de tensión;
* **INA226**, para medición de corriente y variables eléctricas;
* **pantalla OLED de 128 × 64 píxeles**, para visualización de información;
* **relés de conmutación**, para controlar las diferentes etapas del circuito de medición;
* sistema de alimentación mediante baterías recargables;
* electrodos para la inyección de corriente y medición de potencial.

La comunicación entre los módulos de adquisición y la unidad de control se realiza mediante el protocolo **I²C**.

## Contenido del repositorio

El repositorio contiene los archivos utilizados para la construcción, programación y evaluación experimental del dispositivo.

### `hardware/`

Contiene los archivos relacionados con el diseño electrónico y las conexiones del dispositivo.

### `firmware/`

Contiene el código utilizado para programar el sistema mediante Arduino IDE.

### `data/`

Contiene los datos obtenidos durante las pruebas experimentales y los archivos empleados para su análisis estadístico.

### `documentation/`

Contiene documentación complementaria relacionada con la construcción, configuración, operación y limitaciones del dispositivo.

## Validación experimental

El dispositivo fue sometido a pruebas experimentales destinadas a evaluar su comportamiento y capacidad de medición.

Entre las pruebas realizadas se encuentra una evaluación mediante **resistencias de precisión**, compuesta por **2500 pares de mediciones**, cuyos resultados se encuentran disponibles en este repositorio.

También se incluyen los archivos correspondientes al análisis estadístico de los estudios realizados durante el desarrollo experimental.

Los resultados de estas pruebas forman parte de la evaluación presentada en el proyecto de tesis mencionado anteriormente.

## Reproducción

Los archivos publicados en este repositorio permiten consultar los elementos necesarios para reproducir el sistema de manera experimental.

Antes de realizar el montaje definitivo se recomienda:

1. Revisar completamente el esquema de conexiones.
2. Verificar las características eléctricas de cada módulo.
3. Comprobar las direcciones I²C de los dispositivos utilizados.
4. Realizar pruebas iniciales en protoboard.
5. Verificar las mediciones eléctricas antes de conectar los electrodos al terreno.
6. Utilizar una fuente de alimentación adecuada para las características del circuito.

Las direcciones I²C pueden variar entre módulos dependiendo del fabricante y de la configuración de sus puentes de soldadura.

## Limitaciones

El Resistivímetro de detección superficial es un **instrumento experimental de bajo costo** desarrollado con fines académicos y de investigación.

Su diseño no pretende sustituir equipos comerciales de prospección geofísica especializados o sistemas de adquisición profesional debidamente calibrados.

La calidad y alcance de las mediciones pueden verse afectados por las condiciones del terreno, el contacto de los electrodos, la configuración utilizada, las características de la fuente de alimentación, el rango de medición de los sensores y las características propias de los componentes electrónicos empleados.

Asimismo, la identificación de una anomalía eléctrica no constituye por sí misma una evidencia suficiente para establecer la presencia de una estructura arqueológica, alteración antrópica o contexto forense. Los resultados deben ser interpretados dentro de un procedimiento de prospección geofísica y, cuando corresponda, contrastados con otras líneas de evidencia.

## Autoría

**Jesús Salvador Cortés Díaz**

Escuela Nacional de Antropología e Historia (ENAH), México.

El dispositivo fue desarrollado como parte del proyecto de tesis:

**“Desarrollo de un dispositivo de prospección geofísica para aplicaciones en arqueología forense”.**

## Uso académico y citación

Si este proyecto, su diseño, firmware, documentación o datos son utilizados en una investigación académica, publicación científica, trabajo de titulación o proyecto derivado, se solicita reconocer la autoría del desarrollo y citar la versión correspondiente del repositorio.

La información sobre las condiciones de uso, reproducción, modificación y distribución del proyecto se encuentra en el archivo:

[LICENSE](LICENSE.md)

## Publicación científica

Los resultados derivados del desarrollo y evaluación experimental del dispositivo forman parte de una investigación académica destinada a su posterior comunicación mediante publicación científica.

La referencia bibliográfica correspondiente será incorporada a este repositorio cuando la publicación se encuentre disponible.

## Estado del proyecto

**Versión:** 1.2.0
**Estado:** Desarrollo experimental / investigación académica

Este repositorio corresponde a la versión pública del dispositivo utilizada como referencia para la documentación de su desarrollo y evaluación experimental.
