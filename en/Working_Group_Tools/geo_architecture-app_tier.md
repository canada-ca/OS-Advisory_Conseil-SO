# Geospatial Systems Reference Architectures - Application Services Tier

Geospatial data publication and analysis services.

## Possible Technologies

* [GeoServer](http://geoserver.org/)
* [MapServer](https://mapserver.org/)

# Business / Organization Requirements

Data should be exposed through services that comply with common OGC services, such as:

* Support common OGC services
  * [Web Map Service (WMS)](http://www.opengeospatial.org/standards/wms) and [Web Map Tile Service (WMTS)](http://www.opengeospatial.org/standards/wmts)
  * [Web Feature Service (WFS)](http://www.opengeospatial.org/standards/wfs)
  * [Web Coverage Service (WCS)](http://www.opengeospatial.org/standards/wcs)
  * [Web Processing Service (WPS)](http://www.opengeospatial.org/standards/wps)
  * [Catalog Services for Web (CSW)](http://www.opengeospatial.org/standards/cat)

When data is exposed for download, services should either be capable of producing, or downloads should provide data in the following formats:

* Support for producing various output formats
  * [GeoPackage](http://www.geopackage.org/)
  * [GeoJSON](http://geojson.org/)
  * Vector Tiles ([mbtiles](https://github.com/mapbox/mbtiles-spec), for example)

Analytical services need to support operations that allow end users to restrict their analysis to specific areas, and perform efficiently by integrating with the data storate tier.

* Query features by bounding box
* Leverages DB level functions for analysis

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
