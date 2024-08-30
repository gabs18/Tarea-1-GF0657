# <p style="text-align: center;"> Conectividad del Parque Metropolitano La Sabana, Costa Rica </p>

![Imagen_Sabana](https://iconnia.com/wp-content/uploads/2020/11/lago-la-sabana5.jpg)
_Créditos de la fotografía: [ICONIA](https://iconnia.com/wp-content/uploads/2020/11/lago-la-sabana5.jpg)_

&nbsp;

## Resumen
>
>El Parque Metropolitano La Sabana, con sus 68 hectáreas, es el principal espacio verde de San José, Costa Rica, ubicado en el distrito de Mata Redonda. Este parque ofrece una variedad de actividades recreativas y culturales, contando con canchas de fútbol, pistas de atletismo, lagos artificiales, áreas de picnic, el Museo de Arte Costarricense y el Estadio Nacional.  Además, su estratégica ubicación y conectividad con múltiples medios de transporte facilitan el acceso desde diferentes puntos de la ciudad, promoviendo su uso frecuente. La investigación destaca el papel crucial en la movilidad urbana.

_<h5>_ **Palabras clave:** _La Sabana, Parque Metropolitano, Costa Rica, StoryMap, Geovisualización._

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

## Fuentes de información

<p> Las rutas de transporte se pretenden analizar con datos de OpenStreetMap (OSM), y la base de datos de la aplicación móvil Moovit; específicamente, para crear un campo con las rutas de los autobuses que se detienen en cada parada.

<p style='text-align: right;'>
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Openstreetmap_logo.svg/800px-Openstreetmap_logo.svg.png" alt="Logo de OpenStreetMap" width="80"/>

<img src="https://www.iphonelife.com/sites/iphonelife.com/files/Screen%20Shot%202015-06-02%20at%208.56.52%20PM.png" alt="Logo de Moovit" width="80">

</p>

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

&nbsp;

## Problemas a resolver

Se debe filtrar por categorizaron los campos de los polígonos leisure, sport y name para el mapa de usos, y el campo de highway de líneas y puntos en las rutas y paradas.

&nbsp;
&nbsp;

### Referencias bibliográficas

* Solera, G. (2017). Parque La Sabana. Icoder.go.cr.  [https://icoder.go.cr/servicios/parques-recreativos/68-parque-la-sabana](https://icoder.go.cr/servicios/parques-recreativos/68-parque-la-sabana)
&nbsp;
* Municipalidad de San José,  (2016). DIAGNÓSTICO CANTONAL. Dirección de Planificación y Evaluación. [https://www.msj.go.cr/docu/Informes%20y%20Estudios%20de%20Desarrollo%20Urbano/Diagn%C3%B3stico%20Cantonal%202016.pdf](https://www.msj.go.cr/docu/Informes%20y%20Estudios%20de%20Desarrollo%20Urbano/Diagn%C3%B3stico%20Cantonal%202016.pdf)
&nbsp;
* Dufoe, A. (2015). Moovit: Navigate Public Transit Like a Pro. _iPhoneLife._ [https://www.iphonelife.com/sites/iphonelife.com/files/Screen%20Shot%202015-06-02%20at%208.56.52%20PM.png](https://www.iphonelife.com/sites/iphonelife.com/files/Screen%20Shot%202015-06-02%20at%208.56.52%20PM.png)
&nbsp;
* Openstreetmap Foundation (2011). Logo of the OpenStreetMap project.  _Wikimedia Foundation, Inc._ [https://es.wikipedia.org/wiki/OpenStreetMap#/media/Archivo:Openstreetmap_logo.svg](https://es.wikipedia.org/wiki/OpenStreetMap#/media/Archivo:Openstreetmap_logo.svg)
&nbsp;

‌

‌
