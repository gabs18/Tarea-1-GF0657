# Conectividad del Parque Metropolitano La Sabana, Costa Rica

![Imagen_Sabana](https://iconnia.com/wp-content/uploads/2020/11/lago-la-sabana5.jpg)
_Créditos de la fotografía: [ICONIA](https://iconnia.com/wp-content/uploads/2020/11/lago-la-sabana5.jpg)_

&nbsp;

## Resumen
>
>El Parque Metropolitano La Sabana, con sus 68 hectáreas, es el principal espacio verde de San José, Costa Rica, ubicado en el distrito de Mata Redonda. Este parque ofrece una variedad de actividades recreativas y culturales, contando con canchas de fútbol, pistas de atletismo, lagos artificiales, áreas de picnic, el Museo de Arte Costarricense y el Estadio Nacional.  Además, su estratégica ubicación y conectividad con múltiples medios de transporte facilitan el acceso desde diferentes puntos de la ciudad, promoviendo su uso frecuente. La investigación destaca el papel crucial en la movilidad urbana.

**Palabras clave:** _La Sabana, Parque Metropolitano, Costa Rica, StoryMap, Geovisualización._

&nbsp;

### Tema de investigación

#### Conectividad, tomando en cuenta las rutas de transporte, del Parque Metropolitano La Sabana, Costa Rica

&nbsp;

### Objetivo general

**Evaluar la efectividad y conectividad de las rutas de transporte para facilitar el acceso al Parque Metropolitano La Sabana.**

&nbsp;
&nbsp;

## Introducción

El Parque Metropolitano La Sabana juega un papel importante en cuanto a la conectividad y movilidad urbana de San José. Por los cuatro costados del parque transitan autobuses, automóviles, trenes y bicicletas, lo que lo convierte en un lugar altamente interconectado. Según el [Diagnóstico Cantonal de la Municipalidad de San José (2016)](https://www.msj.go.cr/docu/Informes%20y%20Estudios%20de%20Desarrollo%20Urbano/Diagn%C3%B3stico%20Cantonal%202016.pdf), esta conectividad facilita el acceso al parque desde diferentes puntos de la ciudad y sus alrededores, promoviendo su uso frecuente por parte de los residentes y visitantes.

Este parque cuenta con una gran **conectividad** en el sentido de rutas y medios de transporte por lo que cartografiar las rutas y medios de transporte que conectan el parque con diferentes puntos de la ciudad, es crucial para así poder entender cómo la infraestructura de transporte facilita o dificulta el acceso al parque, y cómo la ubicación estratégica del parque influye en su uso y frecuencia de visitantes. Es así que se tiene que tomar en cuenta la efectividad de dichas rutas y de esta manera poder determinar si las rutas actuales son adecuadas y eficientes y/o si existen barreras que impidan un acceso fluido.

&nbsp;

## Contexto geográfico

El Parque Metropolitano de La Sabana se encuentra entre las coordenadas 9.9382571 a 9.937749 al norte, -84.108779 a -84.098331 al este, en el distrito de Mata Redonda. Tiene una extensión de casi 68 hectáreas y se encuentra a 1333 m.s.n.m. Su clima es de sabana tropical, _Aw_ según la clasificación _Köppen-Geiger_, y tiene una temperatura media anual de 19,5°C con una precipitación de alrededor de 2699 mm (Climate-Data, 2024). 

En los costados del parque se encuentran las rutas nacionales: 104 al oeste y al norte, ruta 27 y Avenida 12 al sur, ruta 1 al este, y el comienzo del Paseo Colón y Avenida 10 al este. Estas calles son altamente transitadas por las personas que quieren atravesar el Gran Área Metropolitana, por lo que La Sabana se ha convertido en un lugar interconectado con el resto del GAM. Distritos como Merced, Hospital, Pavas y Uruca son los que tienen mayor cercanía con el parque, y por ende, los cuales tienen mayor influencia.

&nbsp;

## Fuentes de información

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Openstreetmap_logo.svg/800px-Openstreetmap_logo.svg.png" alt="Logo de OpenStreetMap" width="80" align="right" />

<img src="https://www.iphonelife.com/sites/iphonelife.com/files/Screen%20Shot%202015-06-02%20at%208.56.52%20PM.png" alt="Logo de Moovit" width="80" align="right" />

Las rutas de transporte se pretenden analizar con datos de OpenStreetMap (OSM), y la base de datos de la aplicación móvil Moovit; específicamente, para crear un campo con las rutas de los autobuses que se detienen en cada parada. Se pretende filtrar los campos de los polígonos _leisure, sport_ y _name_ para el mapa de usos, y el campo de _highway_ de líneas y puntos en las rutas y paradas. Además, se piensa utilizar la capa del rutas de la Autoridad Reguladora de Servicios Públicos [(ASESEP)](https://mapas.aresep.go.cr/portal/apps/webappviewer/index.html?id=ce2bc92156f5463c8a244d9457896a64).

&nbsp;

## Tipos de datos geoespaciales

Los **datos geoespaciales** que se pretenden emplear son los siguientes:

| Capa                                            |  Tipo de geometría |
|-------------------------------------------------|--------------------|
| Extensión del Parque Metropolitano La Sabana    | Polígono           |
| Rutas de transporte                             | Línea              |
| Carreteras principales y secundarias            | Línea              |
| Paradas de autobús                              | Punto              |
| Paradas de ferrocarril                          | Punto              |

_Tabla 1. Capas geoespaciales a utilizar._

&nbsp;

## Problemas a resolver

El Parque Metropolitano La Sabana está bien conectado y es accesible por numerosas rutas de autobuses, la alta demanda de estas rutas puede resultar en tráfico denso, lo que afecta la fluidez de la movilidad en ciertos momentos. Esta situación refleja tanto las ventajas como los desafíos de tener un espacio recreativo y cultural de gran importancia en una ubicación central y altamente accesible. Ahora, los principales desafíos para tratar los datos geoespaciales son los siguientes:

1. **Extracción de los datos de la capa del ARESEP.** La capa de tipo línea no tiene un campo específicamente de geometría, su tabla de atributos contiene solamente los orígenes y destinos de cada ruta de transporte. Por lo tanto, habría que idear una forma de visualizar y filtrar las rutas que pasen por La Sabana. 
&nbsp;
2. **Visualización e identificación de las rutas.** Es necesario que las rutas se puedan visualizar en la cartografía interactiva se forma eficiente y clara porque muchas rutas de autobús y una de ferrocarril pasan por las mismas calles. Por ende, hay que resolver cómo poder visualizar bien las rutas de transporte.
&nbsp;
3. **Paradas de autobús.** Se pretende integrar información de Moovit a la capa de puntos de paradas de autobús, y de esa forma, crear un pop-up que indique cuáles rutas de autobús paran en dicha parada. Esto puede verse como un problema a resolver por la cantidad de información que hay que integrar al campo nuevo de autobuses que paran en las paradas.

&nbsp;
&nbsp;
&nbsp;

### Referencias bibliográficas

* Climate-Data. (2024). Clima San José. Climate-Data.org. [https://es.climate-data.org/america-del-norte/costa-rica/san-jose-1003/](https://es.climate-data.org/america-del-norte/costa-rica/san-jose-1003/) 
&nbsp;
* Dufoe, A. (2015). Moovit: Navigate Public Transit Like a Pro. _iPhoneLife._ [https://www.iphonelife.com/sites/iphonelife.com/files/Screen%20Shot%202015-06-02%20at%208.56.52%20PM.png](https://www.iphonelife.com/sites/iphonelife.com/files/Screen%20Shot%202015-06-02%20at%208.56.52%20PM.png)
&nbsp;
* Municipalidad de San José,  (2016). DIAGNÓSTICO CANTONAL. Dirección de Planificación y Evaluación. [https://www.msj.go.cr/docu/Informes%20y%20Estudios%20de%20Desarrollo%20Urbano/Diagn%C3%B3stico%20Cantonal%202016.pdf](https://www.msj.go.cr/docu/Informes%20y%20Estudios%20de%20Desarrollo%20Urbano/Diagn%C3%B3stico%20Cantonal%202016.pdf)
&nbsp;
* Openstreetmap Foundation (2011). Logo of the OpenStreetMap project.  _Wikimedia Foundation, Inc._ [https://es.wikipedia.org/wiki/OpenStreetMap#/media/Archivo:Openstreetmap_logo.svg](https://es.wikipedia.org/wiki/OpenStreetMap#/media/Archivo:Openstreetmap_logo.svg)
&nbsp;
* Solera, G. (2017). Parque La Sabana. Icoder.go.cr.  [https://icoder.go.cr/servicios/parques-recreativos/68-parque-la-sabana](https://icoder.go.cr/servicios/parques-recreativos/68-parque-la-sabana)
&nbsp;

‌
