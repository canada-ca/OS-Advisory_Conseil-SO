# Geospatial Systems Reference Architectures - Application Services Tier

Geospatial data consumption and desktop based production and analysis. Both web and desktop clients are candidates for analysis. Web clients are for use by both internal and external clients. Desktop clients will be used by departmental GIS professionals for advanced analysis and data production/maintenance operations.

## Possible Technologies

* [Leaflet](https://leafletjs.com/)
* [OpenLayers](http://openlayers.org/)
* [QGIS](https://qgis.org/en/site/)
* [GeoNode](http://geonode.org/)
* [GDAL](https://www.gdal.org/)
  * [R Bindings](https://cran.r-project.org/web/packages/rgdal/index.html)
  * [Python Bindings](https://pypi.org/project/GDAL/)
* [proj4](https://proj4.org/)
* [Spatial R Libraries](https://cran.r-project.org/web/views/Spatial.html)
  * [sp](https://cran.r-project.org/web/packages/sp/index.html)
  * [spatstat](http://spatstat.org/)
  * [ggmap](https://cran.r-project.org/web/packages/ggmap/index.html)
  * [deldir](https://flowingdata.com/2016/04/12/voronoi-diagram-and-delaunay-triangulation-in-r/)

# Business / Organization Requirements

* Consumes OGC services from the application layer
* Allow download of data in various formats (as much as the app layer can provide)
* Able to combine geospatial data with tabular data
* Provides facilities to create/perform more advanced analysis (can be through libraries/plugins)
* Web interfaces integrate with other systems (WET)
  * Note: WET includes [OpenLayers](http://openlayers.org/), but it is out of date

## Security and Audit Requirements

## Downtime Impact

## Application Performance

## Data Loss

## Speed / Efficiency of Innovation

## Scalability / Elasticity

## Regional / Data Sovereignty

## Automation

## Operations Model

## Delivery Model

# Development Requirements

## Developer Tooling

## CI/CD Process

## APIs & Automation

## Application Cache Strategies

# Deployment and Operations Requirements

## Deployment and Life Cycle Management

## Logging, Monitoring, and Alerting

## Service Healing and Scaling

## Load and Disruption Testing

## Application Delivery Strategy

# Visibility & SLA Requirements

## Scalability, Resilience, and Availability

## Disaster Recovery Strategies

## Performance Monitoring (APM)

## Support and Service Levels

# Change Management

## Compliance, Security, and Access Control

## Platform Governance

## Multi-Cloud Portability
