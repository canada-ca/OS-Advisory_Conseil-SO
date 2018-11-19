# Geospatial Systems Reference Architectures

Reference architectures for multiple layers within a geospatial systems stack.

All of the tiers are required to meet standards for accessibility and security for their respective environments.

## Data Tier (Database)

### Business Requirements

* OGC Simple Features specification compliant
* Allows SQL query level spatial analysis through ST_* functions
* Support for more detailed analysis like routing, distance calculations, etc

## Application Tier

### Business Requirements

* Support common OGC services
  * Web Map Service (WMS) and Web Map Tile Service (WMTS)
  * Web Feature Service (WFS)
  * Web Coverage Service (WCS)
  * Web Processing Service (WPS)
  * Catalog Services for Web (CSW)
* Support for producing various output formats
  * GeoJSON
  * Vector Tiles (mbtiles, for example)
* Query features by bounding box
* Leverages DB level functions for analysis

## Client Tier

Both web and desktop clients are potential candidates. Web clients will be for end users and 
public consumers, but desktop clients will be used to provide more advanced functionality.

### Business Requirements

* Consumes OGC services from the application layer 
* Allow download of data in various formats (as much as the app layer can provide)
* Able to combine geospatial data with tabular data
* Provides facilities to create/perform more advanced analysis (can be through libraries/plugins)
