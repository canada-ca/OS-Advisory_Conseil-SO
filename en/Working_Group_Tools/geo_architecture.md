# Geospatial Systems Reference Architectures

Reference architectures for multiple layers within a geospatial systems stack.

All of the tiers are required to meet standards for accessibility and security for their respective environments.

## Data Tier (Database)

### Business Requirements

* OGC [Simple Features](http://www.opengeospatial.org/standards/sfa) specification compliant
* Allows SQL query level spatial analysis through [ST_* functions](http://www.opengeospatial.org/standards/sfs)
* Support for more detailed analysis like routing, distance calculations, etc

### Technologies

* [PostgreSQL / PostGIS](https://postgis.net/)

## Application Tier

### Business Requirements

* Support common OGC services
  * [Web Map Service (WMS)](http://www.opengeospatial.org/standards/wms) and [Web Map Tile Service (WMTS)](http://www.opengeospatial.org/standards/wmts)
  * [Web Feature Service (WFS)](http://www.opengeospatial.org/standards/wfs)
  * [Web Coverage Service (WCS)](http://www.opengeospatial.org/standards/wcs)
  * [Web Processing Service (WPS)](http://www.opengeospatial.org/standards/wps)
  * [Catalog Services for Web (CSW)](http://www.opengeospatial.org/standards/cat)
* Support for producing various output formats
  * [GeoPackage](http://www.geopackage.org/)
  * [GeoJSON](http://geojson.org/)
  * Vector Tiles ([mbtiles](https://github.com/mapbox/mbtiles-spec), for example)
* Query features by bounding box
* Leverages DB level functions for analysis

### Technologies

* [GeoServer](http://geoserver.org/)
* [MapServer](https://mapserver.org/)

## Client Tier

Both web and desktop clients are potential candidates. Web clients will be for end users and 
public consumers, but desktop clients will be used to provide more advanced functionality.

### Business Requirements

* Consumes OGC services from the application layer 
* Allow download of data in various formats (as much as the app layer can provide)
* Able to combine geospatial data with tabular data
* Provides facilities to create/perform more advanced analysis (can be through libraries/plugins)
* Web interfaces integrate with other systems (WET)
  * Note: WET includes [OpenLayers](http://openlayers.org/), but it is out of date
  
### Technologies

* [Leaflet](https://leafletjs.com/)
* [OpenLayers](http://openlayers.org/)
* [QGIS](https://qgis.org/en/site/)
* [GeoNode](http://geonode.org/)
