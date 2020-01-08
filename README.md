# Barcelona's traffic accidents analysis

En este proyecto se analizan los accidentes de tráfico ocurridos en la ciudad de Barcelona durante el año 2018. El Ayuntamiento de Barcelona, a través de su portal de [Open Data](https://opendata-ajuntament.barcelona.cat/data/es/organization/seguretat), publica anualmente los datos de los accidentes gestionados por la Guardia Urbana durante cada periodo.

Se usarán esos datos para caracterizar los accidentes de tráfico en la ciudad, poniendo especial énfasis en determinar qué factores influyen en mayor medida en la gravedad del accidente. Conocer esos factores puede ayudar a las administraciones y organismos a establecer medidas que prevengan o palien las consecuencias de un accidente.


*This project analyzes traffic accidents that occurred in the city of Barcelona during 2018. The City Council of Barcelona, ​​through its [Open Data] portal (https://opendata-ajuntament.barcelona.cat/data/ es / organization / seguretat), publishes annually the data of the accidents managed by the Urban Guard during each period.*

*These data will be used to characterize traffic accidents in the city, with special emphasis on determining which factors most influence the severity of the accident. Knowing these factors can help administrations and agencies to establish measures that prevent or mitigate the consequences of an accident.*

![](https://www.metropoliabierta.com/uploads/s1/75/18/01/accidentes-trafico-barcelona-muertos_5_570x340.jpeg)

## Conclusiones del estudio

En base a este estudio se pueden extraer algunas conclusiones que nos ayudan a caracterizar los accidentes de tráfico en la ciudad de Barcelona y determinar los factores de riesgo en los mismos.

  * Aproximadamente la mitad de los accidentes se producen durante la tarde.
  
  * El viernes es el día de mayor concentración de accidentes. 
  
  * Los fines de semana se producen menos accidentes que durante los días laborales; sin embargo, en estos dos días se produce un porcentaje mayor de accidentes durante la noche.
  
  * El tipo más frecuente de accidente se produce por una colisión lateral, seguido del alcance (por detrás), la colisión fronto-lateral, el atropello y la caída en vehículos de 2 ruedas.
  
  * La mayoría de accidentes se concentran en el centro de la ciudad (zona del Eixample), en las rondas y en las principales vías (Diagonal y Gran Vía)
  
  * Los accidentados en motocicleta (7017) doblan a los accidentados que viajaban en coche (3035). Les siguen los accidentados en bicicleta (730).
  
  * Respecto a la gravedad, se comprueba que la edad media de los accidentados graves es superior a los accidentados leves. 
  
  * Respecto al tipo de accidente, los choques contra objetos estáticos o por salída de la vía, son los que producen los accidentes más graves, seguidos de las caídas en el interior de los autobuses o autocares y las colisiones frontales o fronto-laterales.
  
  * Los vehículos más inseguros son las motocicletas y las bicicletas. Por ejemplo, la posibilidad de resultar herido grave o muerto en un accidente de motocicleta es casi 6 veces mayor que si se tuviese el msimo accidente en coche.
  
## Descripción del dataset

La información se puede obtener a través de varios ficheros que representan distintas dimensiones de los accidentes. Por un lado encontramos el fichero '2018_accidents_gu_bcn.csv' que contiene los datos de los accidentes en sí mismos. En el fichero '2018_accidents_persones_gu_bcn_.csv' encontramos los datos de las personas accidentadas y en el fichero '2018_accidents_tipus_gu_bcn_.csv' encontramos la tipología de cada accidente (colisión frontal, alcance, salida de vía, etc.)

**Fichero "Accidentes" (2018_accidents_gu_bcn.csv)**

Este dataset de accidentes encontramos:

  * **Numero_expedient**: Identificador del expediente del accidente
  * **Codi_districte**:   Código numérico del distrito
  * **Nom_districte**:    Nombre del distrito
  * **Codi_barri**:       Código numérico del barrio
  * **Nom_barri**: Nombre del barrio
  * **Codi_carrer**: Código numérico de la calle
  * **Nom_carrer**: Nombre de la calle
  * **Num_postal**: Número de la calle
  * **Descripcio_dia_setmana**: Descripción del día de la semana
  * **Dia_setmana**: Código del día de la semana
  * **Descripcio_tipus_dia**: Tipo de día (laboral)
  * **Any**: Año del accidente
  * **Mes_any**: Mes del accidente, en número
  * **Nom_mes**: Nombre del mes del accidente
  * **Dia_mes**: Día del mes del accidente
  * **Hora_dia**: Hora del accidente
  * **Descripcio_torn**: Descripción del turno (matí, tarda, nit)
  * **Descripcio_causa_vianant**: Descripción de la causa del accidente, si es por motivo de un viandante
  * **Numero_morts**: Número de muertos en el accidente
  * **Numero_lesionats_lleus**: Número de lesionados leves
  * **Numero_lesionats_greus**: Número de lesionados graves
  * **Numero_victimes**: Número de víctimas (leves y graves)
  * **Numero_vehicles_implicats**: Número de vehículos implicados
  * **Coordenada_UTM_X**: Coordenada X de la localización del accidente en estandar UTM
  * **Coordenada_UTM_Y**: Coordenada Y de la localización del accidente en estandar UTM
  * **Longitud**: Coordenada del accidente (longitud)
  * **Latitud**: Coordenada del accidente (latitud)

**Fichero "Personas" (2018_accidents_persones_gu_bcn_.csv)**

Contiene en parte los mismos campos que el fichero de accidentes (los que hacen referencia al expediente, datos de localización y fecha). Los campos que difieren son:
 
  * **Desc_Tipus_vehicle_implicat**: Descripción del tipo de vehiculo accidentado  (turismo, ciclomotor, ...)
  * **Descripcio_sexe**: Descripción del sexo de la persona accidentada
  * **Edat**: Edad de la persona accidentada
  * **Descripcio_tipus_persona**: Tipo de persona (conductor, pasajero, viandante)
  * **Descripcio_victimitzacio**: Gravedad del accidentado (leve, grave, muerto)
  
**Fichero "Tipología de accidente" (2018_accidents_tipus_gu_bcn_.csv)**

Este fichero también contiene en parte los mismos campos que el fichero de accidentes (los que hacen referencia al expediente, datos de localización y fecha). Se añade un campo:

  * **Tipus_accident**: Descripción del tipo de accidente  (colisión frontal, colisión lateral, alcance por detras, etc.)
  
******

La clave que permite enlazar estos datasets es el número de expediente del accidente. Los registros pueden encontrarse duplicados: por ejemplo, un accidente con dos tipologías de accidente (colisión frontal y lateral) aparecerá dos veces en el fichero de "Tipología de accidentes".


## Más información

Se puede encontrar información adicional, incluyendo una descripción de los archivos del proyecto, en la [Wiki](https://github.com/NemoIT/INCIBE-security-warnings/wiki) de este proyecto.
