# Geospatial Systems Reference Architectures - Application Services Tier

Geospatial data publication and analysis services.

## Possible Technologies

* [GeoServer](http://geoserver.org/)
* [MapServer](https://mapserver.org/)
* [Nominatim](https://github.com/openstreetmap/Nominatim)
* [Pelias](https://pelias.io/)
* [Apache Spark](http://spark.apache.org/)
* [Apache Kafka](https://kafka.apache.org/)

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

Since the application tier is mostly just exposing data stored in the database to end users, a compromise in this system would appear as equivalent to a compromise to the data. This would be a serious incident that could have implications on the image of the department hosting the service.

## Downtime Impact

For internal facing systems, downtime would result in the loss of productivity for users, and would potentially have follow-on effects that result in delays to programs and processes. For external systems, downtime would mean the loss of access to external clients. While no SLA exists for the uptime of external systems, it is likely that some end users would be impacted. As long as downtime is kept to a minimum, external users will likely view it as an annoyance.

## Application Performance

When applications are unresponsive, for any reason, there will be reduced productivity. Public facing systems might see a loss of confidence that results in a loss of users, but internal systems could have follow on effects that result in problems processing data or delays in providing timely service to critical services and potentially create a risk to public safety.

## Data Loss

Data loss is a major concern for all systems, but for public facing systems that provide only read-only functionality, data loss would merely mean that a system needs to be re-initialized. These events would result in downtime, but are not generally seen as a significant impact as long as the problems are detected early.

Data loss in systems of record is a separate issue, and represents a major risk to the business. Systems need to be implemented with assurances that permissions are clearly and effectively implemented so as to avoid unintentional access, and all changes to the data should provide an audit trail.

## Speed / Efficiency of Innovation

## Scalability / Elasticity

## Regional / Data Sovereignty

Some geospatial data will have sensitive data attached to it, either as associated attributes or as the data itself (geometry). These types of data are subject to the security controls associated with their level of protection, but as a general rule will all require being housed within Canada either on public or government owned systems. Higher data restrictions will incur a more restrictive storage and processing framework.

Public data can be distributed through any appropriate means, although there is a requirement for departments to ensure the integrity of the data overall, residency requirements are significantly lower for public data.

## Automation

The publication of data to public systems should be automated as much as possible. Integration between systems should be validated through a CI process that can give assurances that the integrity of the data is meeting a minimal level of acceptability.

Data will be both ingested and exposed through multiple systems. In cases where this data transfer is expected to happen repeatedly, the interaction should be automated. Stakeholders require a reliable system through which they can send their data to the appropriate department, and departments need a reliable way to publish outputs to stakeholders and the public.

## Operations Model

Departments have different requirements for when they can delegate the operations of their infrastructure. Applications will be subject to the data protection provisions required of the data they serve, and as such there will be a mix of operating models required to be supported by the solution(s).

## Delivery Model

Public data services are good candidates for SaaS or PaaS implementations. Data with higher protection requirements will either have to be self-hosted or is are possible candidates for IaaS services in a protected cloud infrastructure.

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
