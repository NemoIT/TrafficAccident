# Barcelona's traffic accidents analysis

En este proyecto se analizan los accidentes de tráfico ocurridos en la ciudad de Barcelona durante el año 2018. El Ayuntamiento de Barcelona, a través de su portal de [Open Data](https://opendata-ajuntament.barcelona.cat/data/es/organization/seguretat), publica anualmente los datos de los accidentes gestionados por la Guardia Urbana durante cada periodo.

*This repository presents the work to create a dataset based on security warnings provided by INCIBE, the Spanish National Cybersecurity Institute, using web scraping techniques with Python.*


![](https://www.metropoliabierta.com/uploads/s1/75/18/01/accidentes-trafico-barcelona-muertos_5_570x340.jpeg)


## Contexto

El [INCIBE](https://www.incibe.es/) (Instituto Nacional de Ciberseguridad) es un organismo dependiente del Ministerio de Economía y Empresa de España, dedicado al desarrollo de la ciberseguridad y de la confianza digital de los ciudadanos. Sus actividades se centran en la investigación, la prestación de servicios y la coordinación con los agentes con competencias en la materia.

Entre sus servicios se encuentra la publicación de **[avisos de seguridad](https://www.incibe.es/protege-tu-empresa/avisos-seguridad)** (phishing, ransomware, actualizaciones…), a través de los cuales facilitan la información necesaria para prevenir, proteger y responder ante incidentes de seguridad en el entorno empresarial.


## Descripción del dataset

El dataset generado incluye todos los avisos de seguridad emitidos por INCIBE desde Enero de 2014 hasta la actualidad (Noviembre de 2019). Para cada aviso se incluye una descripción del problema y su solución, el nivel de gravedad del aviso, la fecha de publicación y etiquetas varias para su categorización.


## Contenido

El dataset generado se proporciona en formato JSON. Su estructura es la siguiente:

|Nombre |Tipo                          |Uso                         |
|----------------|-------------------------------|-----------------------------|
|**title**|string|Título del aviso
| **date**:|date| 	Fecha de publicación
|**severity**:|integer| Gravedad (1-Mínima, 2-Baja, 3-Media, 4-Alta, 5-Crítica)
|**labels**:|string list| Etiquetas para categorizar ("Phising", "Fraude", "Vulnerabilidad", etc.)
|**description**:|string| Descripción del problema que genera el aviso
|**solution**:|string| Solución para prevenir, evitar o corregir la amenaza


## Movitación

La recopilación de los avisos de seguridad en este dataset abre la puerta a la realización de múltiples análisis que permitan obtener un conocimiento más amplio de las amenazas de seguridad.

Un primer análisis descriptivo nos ayudará a entender mejor este fenómeno: ¿cuáles son las amenazas más frecuentes? ¿qué evolución están teniendo? ¿podemos encontrar patrones en la aparición de las amenazas? 

Pero sin duda, la aplicación de técnicas de minería de textos nos permitirá obtener el máximo valor de este dataset. Mediante la extracción de palabras clave podremos determinar qué sistemas o recursos se ven afectados, qué características tienen los problemas y sus correspondientes soluciones.

## Licencia

This dataset is licensed under a [Creative Commons Attribution 4.0 International
License][cc-by-nc-sa].

[![CC BY 4.0][cc-by-image]][cc-by-nc-sa]

[cc-by-nc-sa]: https://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

## Más información

Se puede encontrar información adicional, incluyendo una descripción de los archivos del proyecto, en la [Wiki](https://github.com/NemoIT/INCIBE-security-warnings/wiki) de este proyecto.
