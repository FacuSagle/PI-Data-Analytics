# Siniestros viales en CABA

## Introduccion 

Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas y que pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.

En el contexto de una ciudad como Buenos Aires, los siniestros viales pueden ser una preocupación importante debido al alto volumen de tráfico y la densidad poblacional. Estos incidentes pueden tener un impacto significativo en la seguridad de los residentes y visitantes de la ciudad, así como en la infraestructura vial y los servicios de emergencia.

Las tasas de mortalidad relacionadas con siniestros viales suelen ser un indicador crítico de la seguridad vial en una región. Estas tasas se calculan, generalmente, como el número de muertes por cada cierto número de habitantes o por cada cierta cantidad de vehículos registrados. Reducir estas tasas es un objetivo clave para mejorar la seguridad vial y proteger la vida de las personas en la ciudad.

Es importante destacar que la prevención de siniestros viales involucra medidas como la educación vial, el cumplimiento de las normas de tráfico, la infraestructura segura de carreteras y calles, así como la promoción de vehículos más seguros. El seguimiento de las estadísticas y la implementación de políticas efectivas son esenciales para abordar este problema de manera adecuada.

### Contexto
En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, esta sigue siendo la principal causa de muertes violentas en el país. Los informes del Sistema Nacional de Información Criminal (SNIC), del Ministerio de Seguridad de la Nación, revelan que entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Estas cifras equivalen a 11 personas por día que resultaron víctimas fatales por accidentes de tránsito.

Solo en 2022, se contabilizaron 3.828 muertes fatales en este tipo de hechos. Los expertos en la materia indican que en Argentina es dos o tres veces más alta la probabilidad de que una persona muera en un siniestro vial que en un hecho de inseguridad delictiva.

## Objetivo y datos disponibles
Elaboración de un proyecto de anális de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales. Se cuenta con un dataset sobre homicidios  en siniestros viales acaecidos en la Ciudad de Buenos Aires durante el periodo 2016-2021 (homicidios.xlsx). Este dataset se encuentra en formato xlsx y contiene dos hojas llamadas: hechos y víctimas. Asimismo, se incluyen dos hojas adicionales de diccionarios de datos. La principal fuente de informacion para el armado de este dataset son datos policiales, generando una base de datos que incluyen fecha y ubicación del hecho y tipo de transporte involucrado. Además se especifica el género y edad de las víctimas.

### Datasets adicionales:
- cruces-semaforizados: Este conjunto de datos proporciona información detallada sobre los cruces que cuentan con semáforos. Incluye detalles como la fecha de inauguración y finalización de cada semáforo, su tipo y ubicación geográfica. 

Enlace: [Cruces semaforizados](https://cdn.buenosaires.gob.ar/datosabiertos/datasets/transporte-y-obras-publicas/cruces-semaforizados/cruces-semaforizados.csv)https://cdn.buenosaires.gob.ar/datosabiertos/datasets/transporte-y-obras-publicas/cruces-semaforizados/cruces-semaforizados.csv

- **Conteociclistas-GCBA:** Conjunto de datos que ofrece información sobre los viajes anuales realizados por ciclistas en la Ciudad Autónoma de Buenos Aires.

- **Mapa de CABA en Formato GeoJSON:** Representación geográfica de la Ciudad Autónoma de Buenos Aires en formato GeoJSON, ideal para análisis espaciales y visualizaciones geográficas.

Enlace: [Mapa de CABA](https://cdn.buenosaires.gob.ar/datosabiertos/datasets/ministerio-de-educacion/comunas/comunas.geojson)

**Barrios de las Comunas:** Este conjunto de datos ofrece una lista completa de los barrios que conforman cada comuna en la Ciudad Autónoma de Buenos Aires.

Enlace: [Barrios de las comunas](https://cdn.buenosaires.gob.ar/datosabiertos/datasets/ministerio-de-educacion/comunas/comunas.csv)

### Paginas webs utilizadas

**- Población de las Comunas:** Este enlace te dirige a una página de Wikipedia que presenta una lista de las comunas de la Ciudad de Buenos Aires ordenadas por población, ofreciendo así un panorama detallado de la distribución demográfica en la ciudad.

Enlace: [Poblacion de las comunas]("https://es.wikipedia.org/wiki/Anexo:Comunas_de_la_ciudad_de_Buenos_Aires_por_poblaci%C3%B3n")

## EDA

Durante el Análisis Exploratorio de Datos (EDA), se realizarán las siguientes tareas para preparar los datos y facilitar la creación de un dashboard interactivo en Power BI:

- Definición de Tipos de Variables: Se identificarán y categorizarán los diferentes tipos de variables presentes en el conjunto de datos.

- Búsqueda de Valores Faltantes: Se detectarán y gestionarán los valores faltantes en el conjunto de datos, evaluando posibles estrategias para su manejo.

- Identificación de Valores Atípicos/Extremos (Outliers): Se identificarán y analizarán los valores que se desvían significativamente del patrón general del conjunto de datos.

- Detección de Registros Duplicados: Se identificarán y eliminarán los registros duplicados para garantizar la integridad de los datos.

- Estudio de Relaciones entre Variables: Se explorarán las relaciones y correlaciones entre las diferentes variables para comprender mejor la estructura y las interacciones dentro del conjunto de datos.

- Análisis Estadísticos de las Variables: Se realizarán análisis estadísticos descriptivos para obtener insights sobre la distribución, tendencias y patrones presentes en las variables del conjunto de datos.

### Archivos generados en el archivo del EDA

En este archivo se generan tablas adicionales que son fundamentales para el análisis. A continuación, se detallan los archivos CSV generados:

- ubicacion_homicidios_semaforos: Contiene información sobre si los accidentes ocurrieron en calles con o sin semáforos. Aunque no se distingue específicamente si la calle es un cruce, al relacionar esta tabla con otros datos se puede determinar qué accidentes ocurrieron en cruces.

- tasa_kpi: Esta tabla se ha generado para proporcionar la información esencial que permite determinar el primer KPI y permite su correcta visualizacionen el dashboard posteriormente.

- semaforos: Ofrece información relacionada con la ubicación y características de los semáforos en la Ciudad Autónoma de Buenos Aires (CABA).

-relaciones: Proporciona los datos necesarios para visualizar posibles relaciones entre diferentes variables, como auto-pasajero acompañante, moto-conductor, género y tipo de vía.

- licencias: Esta tabla ofrece información detallada sobre las licencias de conducir otorgadas en la Ciudad Autónoma de Buenos Aires (CABA), incluyendo datos relevantes sobre el género de los titulares y el tipo de licencia (nueva o renovada).

- kpis: Después de un análisis exhaustivo de los datos, esta tabla se ha preparado con la información esencial para visualizar el segundo y tercer KPI en el dashboard.

- df_homicidios_victimas: Esta tabla ofrece información detallada sobre las víctimas tras la realización del EDA. 

- df_homicidios_hechos: Proporciona datos sobre los incidentes o hechos relevantes después de la realización del EDA.

- df_comunas: Esta tabla combina información sobre la población y los barrios de las comunas de CABA.


## KPIs

Los tres indicadores claves de rendimiento (KPIs) propuestos son:

- **Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.**

Se define a la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000

-  **Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.**

Se define a la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

- **Reducir un 7% la cantidad de accidentes mortales en avenidas en el último año, en CABA, respecto al año anterior.**

## Dashboard

Se ha diseñado un dashboard interactivo que presenta visualizaciones detalladas de los KPIs, información sobre incidentes y víctimas, así como análisis de las relaciones entre las variables del conjunto de datos. Además, se incluye información relevante sobre los cruces y la ubicación de los semáforos.

### Mapa de formas de CABA
A continuación, se describirá el proceso para generar un Mapa de Formas de la Ciudad Autónoma de Buenos Aires (CABA) a partir de un archivo GeoJSON en Power BI.

1. **Descarga del Mapa**: Primero, descarga el mapa de la página oficial del gobierno de la ciudad de Buenos Aires. El archivo estará en formato GeoJSON.

2. **Manipulacion de archivo GeoJSON**:  Copia y pega el archivo GeoJSON en la página [geojson.io](http://geojson.io/) y accede a la pestaña "Tabla". Elimina las columnas innecesarias y asegúrate de que las comunas coincidan con los datos que vas a utilizar. Cambia los nombres de las columnas según sea necesario y guarda nuevamente el archivo en formato GeoJSON. Este archivo se encuentra en la carpeta mapas con el nombre de map.geojson.

3. **Conversión a TopoJSON**: Carga el archivo map.geojson en la página Mapshaper](https://mapshaper.org/) y exporta el archivo como TopoJSON, que se denominará map2.

4. **Configuración en Power BI**:

	- **Activación de Mapa de Formas:** En "Opciones y configuración", ve a "Opciones" -> "Global" -> "Características de versión preliminar" y activa la opción "Objeto visual mapa de formas".

	- **Selección de Mapa de Formas:** En la vista de informe, accede a la pestaña de visualizaciones y selecciona "Mapa de Formas". En el campo de ubicaciones, añade la columna que contiene las comunas.

	- **Configuración del Mapa:** Aún en visualizaciones, ve a "Formato visual" -> "Configuración del mapa". En "Tipo de asignación", elige "Mapa personalizado". En la opción para agregar un tipo de mapa, selecciona el archivo TopoJSON creado anteriormente. Si deseas visualizar un mapa de densidades, añade la columna que contiene los IDs de las víctimas al campo de "Saturación de color".

### Paleta de colores:
Dentro del archivo `theme.txt`, encontrará la paleta de colores personalizada diseñada siguiendo las directrices del manual de marca de Buenos Aires Ciudad. Esta paleta se ha creado con el objetivo de mantener una coherencia visual el proyecto.

Para más detalles sobre los colores y las pautas de diseño, consulte el [Manual de Marca de Buenos Aires Ciudad](https://buenosaires.gob.ar/jefedegobierno/manual-de-marca).

## Analisis

**Desempeño de KPIs**
De los tres KPIs planteados, únicamente se cumplió el primero en 2021. Se alcanzó el primer KPI en cinco semestres de los 11 analizados, mientras que los dos restantes se alcanzaron en tres de los 5 años.

**Víctimas de Siniestros Viales**
En total, se registraron 717 víctimas a causa de siniestros viales.

**Distribución de Accidentes**
El 78% de los accidentes se produjeron en cruces, de  los cuales, en el 87% de los casos no contaban con semáforos. 

**Localización de Accidentes Fatales**

La General Paz fue la calle con la mayor cantidad de muertes, registrando 61 víctimas.

Los cruces semaforizados con múltiples accidentes:
- Alcorta, Amancio Av. y Zavaleta
- Corrientes Av. y Dorrego Av.
- Santa Fe Av. y Godoy Cruz

Los cruces con más accidentes fueron:
- 27 de Febrero Av. y Escalada Av. (5 víctimas)
- Paz Gral. Av. y Bablin, Ricardo, Dr. Av. (4 víctimas)
- Paz, Gral. Av. y Del Libertador Av. (4 víctimas)
- Alcorta, Amancio Av. y Bonavena, Oscar Natalio (3 víctimas)
- Castillo, Ramon S. Pres. Av. y Calle 12 (3 víctimas)
- Del Libertador Av. y Ramos Mejía, Jose María, Dr. Av. (3 víctimas)
- Independencia Av. y Cevallos, Virrey (3 víctimas)
- Paz Gral. Av. y de los Corrales Av. (3 víctimas)

Es crucial señalar que todos los cruces mencionados son intersecciones sin semáforos. Al enfocarnos en los accidentes en cruces con avenidas, donde las víctimas circulaban en motocicleta, ambos aspecto clave en nuestro análisis, se contabilizaron 146 víctimas. Resulta notable que, a pesar de la escasa presencia de semáforos en la comuna 8, esta área representa una proporción significativa de estos accidentes, con el 12% del total. En esta comuna se ubica la intersección con el mayor número de víctimas, 27 de Febrero Av. y Escalada Av., donde el 94% de los cruces involucrados en los accidentes carecían de semáforos.
En la comuna 8 se observa una escasa presencia de semáforos, ademas de concentrar un número significativo de accidentes en este grupo de las victimas, representando el 12% del total y de los cuales el 94% ocurrieron en lugares sin semaforo. La intersección de 27 de Febrero Av. y Escalada Av., ubicada en esta comuna, es la que registra el mayor número de víctimas.

**Tipos de Calles**
Las avenidas resultaron ser las más críticas, siendo el escenario del 62% de los accidentes.

**Actores Involucrados**
Los autos y los pasajeros son los actores más frecuentes en los accidentes, representando el 30% y el 26% respectivamente.

**Roles de las Víctimas**
Los conductores y los peatones son los roles más afectados, representando el 43% y el 38% de las víctimas, respectivamente.

**Demografía de las Víctimas**
El 77% de las víctimas eran hombres. Además, el 94% de las víctimas que conducían eran hombres, un dato significativo considerando que solo el 71% de las licencias de conducir son otorgadas a hombres.

**Comuna mas afectada**
La comuna 1, que incluye barrios como Constitución, Monserrat, Puerto Madero, Retiro, San Nicolás y San Telmo, es la que presenta la mayor cantidad de accidentes.

**Evolución Temporal**
Se observó una reducción en la cantidad de víctimas a lo largo del periodo analizado, pasando de 146 en 2016 a 97 en 2021.
A pesar del aumento en los viajes en bicicleta, la cantidad de víctimas en este medio ha disminuido. El rango de edad con más accidentes es de 19-30 años, representando el 34% del total. En cuanto al horario, la mañana (6 am-12 pm) es el período con más accidentes, con el 30% del total.

**Rango Etario mas afectado**
El grupo de edad más afectado por accidentes está en el rango de 19-30 años, representando el 34% de los casos.

**Horario con mayor cantidad de victimas**
El horario con mayor incidencia de accidentes es por la mañana, entre las 6:00 am y las 12:00 pm, con un 30% de los accidentes registrados.


### Conclusion
Para lograr alcanzar los KPI propuestos, seria interesante enfocarse en la comuna 1 (que es la que presenta mayor cantidad de accidentes) y la comuna 8, que presenta una baja cantidad de semaforos pero una gran cantidad de accidentes en cruces semaforizados. Ademas, se podria evaluar la posibilidad de instalar semaforos en la ciudad, priorizando los cruces donde se han producido mas de 2 victimas. Otra medida preventiva podria ser realizar campañas sobre el uso de cascos, debido a que como se pudo observar, la mayoria de las victimas circulan en moto.  

### Consideraciones:
- Rangos horarios: madrugada(0-6), mañana(6-12), tarde(12-18) y noche(18-24)
-Rangos etarios: 0-18,19-30,31-45,45-60,+61.

## Tecnologías y herramientas aplicadas:
- Jupyter Notebook
- Python
- Power BI
- Excel

## Librerias
- geopy: Utilizada para obtener las coordenadas geográficas a partir de una dirección.

- pandas: Empleada para leer archivos en formatos xlsx y xsv, así como para exportar dataframes a archivos csv. Facilita la creación, manipulación y análisis estadístico de dataframes.

- seaborn: Usada para generar visualizaciones atractivas y efectivas.

- matplotlib.pyplot: Empleada para la creación de gráficos y visualizaciones.

- numpy: Utilizada para simplificar operaciones en dataframes, como la creación de columnas basadas en condiciones utilizando np.where.

- datetime: Usada para la manipulación y análisis de fechas.

- warnings: Utilizada para ignorar advertencias y mantener un flujo de ejecución limpio al correr el código.
