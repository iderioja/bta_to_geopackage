## [![Icono](http://www.iderioja.larioja.org/imagenes/logo_iderioja_56x70.gif)](http://www.iderioja.org)     [BTA to GeoPackage](https://github.com/iderioja/bta_to_geopackage)

[Versión en español](https://github.com/iderioja/bta_to_geopackage/blob/master/README.md)

GeoPackage (http://www.geopackage.org/) is a format for storing geographic information created by the Open Geospatial Consortium, specially designed for use in mobile environments.

One of the most interesting properties of this new format is its ability to integrate into a single repository (file) vector data and images.

The format offers a SQLite extension that allows managing geographic data directly without the mediation of any API, thus ensuring the integrity of information regardless of the software used.

To the possibility of a mixed raster-vector storage, the ability to define what in a database language are called "restrictions" (constraints) is added. Conditions that must be met in editing data, designed to ensure their referential integrity, regardless of the platform from which the edition is done.

The Government of La Rioja is involved in the implementation in that format of the data model that the National Geographic High Council of Spain defined for the [BTA Harmonised Topographic Database 1:5,000/1:10,000] (http://www.csg-cnc.es//web/cnccontent/en/bta.html).

In the first phase of development we have addressed the works of the 1:5,000 topographic data migration of the Autonomous Community of La Rioja (Spain) from a BTA model, currently managed in a spatial database.

In this first work, there have been moved to different GeoPackage files all the BTA layers from each cartographic sheet.

The GeoPackage files that we created can be downloaded through the file [bta_to_geopackage.geojson](https://github.com/iderioja/bta_to_geopackage/blob/master/bta_1_5000_geopackage.geojson) which is available in this directory.

![Alt text](/imagenes/bta_to_geopackage_geojson.jpg "This is not an embedded viewer, it's just a map image")

The conversion process has been performed using the 2015 version of the software ETL [FME] (http://www.safe.com/fme/), because this last release includes a specific transformer for this task, based on the GDAL library.

As this transformer does not yet incorporate the ability to define "constraints", we are manually building them personalized for each of the domains of values of the diverse attributes of the different tables.

Files with the definition of the complete model and corresponding restrictions will be provided as they become available.

In this GitHub repository we plan to maintain a [wiki](https://github.com/iderioja/bta_to_geopackage/wiki) in which we will describe the details of the project with comments and distribution of the processing Workbenchs and in which you can also collaborate.

We hope our work to be of interest and that serves to extend and consolidate the GeoPackage format, which full specification can be seen in http://www.geopackage.org/spec/

The IDErioja Technical Team.

http://www.iderioja.org

http://twitter.com/iderioja