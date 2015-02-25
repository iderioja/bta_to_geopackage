## [![Icono](http://www.iderioja.larioja.org/imagenes/logo_iderioja_56x70.gif)](http://www.iderioja.org)     [BTA to GeoPackage](https://github.com/iderioja/bta_to_geopackage)

[English version](https://github.com/iderioja/bta_to_geopackage/blob/master/README_EN.md)


GeoPackage (http://www.geopackage.org/) es un formato para el almacenamiento de información geográfica, creado por el Open Geospatial Consortium, diseñado especialmente para su utilización en entornos móviles.

Una de las propiedades más interesantes de este nuevo formato, es su capacidad para integrar en un mismo repositorio (fichero) datos vectoriales e imágenes.

El formato ofrece una extensión SQLite que permite gestionar directamente los datos geográficos sin la intermediación de ninguna API, asegurando así la integridad de la información independientemente del software utilizado.

A la posibilidad de un almacenamiento mixto ráster-vectorial, se suma la capacidad de definir lo que en un lenguaje de base de datos se denominan "restricciones" (constraints). Condiciones que se deben cumplir en la edición de datos, diseñadas para asegurar la integridad referencial de estos, independientemente de la plataforma desde la que se ejecute la edición.

El Gobierno de La Rioja, está involucrado en la implementación en dicho formato del modelo de datos que el Consejo Superior Geográfico de España ha definido para la [Base Topográfica Armonizada BTA 1:5000/1:10.000 ](http://www.csg-cnc.es/web/cnccontent/bta.html).

En una primera fase de desarrollo, hemos abordado los trabajos de migración de los datos topográficos 1:5.000 de la Comunidad Autónoma de La Rioja (España), desde un modelo BTA, actualmente gestionado en una base de datos espacial.

En este primer desarrollo del trabajo, se han trasladado a distintos ficheros GeoPackage el conjunto de las capas BTA correspondientes a cada una de las hojas cartográficas.

Los ficheros GeoPackage que hemos creado, los podéis descargar consultando el fichero [bta_to_geopackage.geojson](https://github.com/iderioja/bta_to_geopackage/blob/master/bta_1_5000_geopackage.geojson) que se encuentra disponible en este directorio.

![Alt text](/imagenes/bta_to_geopackage_geojson.jpg "Esto no es un visualizador incrustado, es solo una imagen del mapa")

El proceso de conversión se ha realizado utilizando la versión 2015 del software ETL [FME](http://www.safe.com/fme/) , al incorporar esta última release un transformador específico para realizar esta tarea, basado en la librería GDAL.

Dado que dicho transformador todavía no incorpora la posibilidad de definir "constraints", estas las estamos construyendo manualmente de forma personalizada para cada uno de los dominios de valores de los distintos atributos, de las diferentes tablas.

Los ficheros con la definición del modelo completo y sus correspondientes restricciones se facilitarán en cuanto se encuentren disponibles.

En  este repositorio GitHub tenemos previsto mantener una [wiki](https://github.com/iderioja/bta_to_geopackage/wiki) en la que  describiremos los detalles del proyecto con comentarios y distribución de los Workbenchs de procesamiento y en la que también vosotros podéis colaborar.

Esperamos que nuestro trabajo os resulte de interés y sirva para extender y consolidar el formato GeoPackage, cuya especificación completa podéis consultar en http://www.geopackage.org/spec/

El Equipo Técnico IDErioja.

http://www.iderioja.org

http://twitter.com/iderioja

