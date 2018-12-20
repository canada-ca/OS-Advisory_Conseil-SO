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

## Business / Organization Requirements

* Consumes OGC services from the application layer
* Allow download of data in various formats (as much as the app layer can provide)
* Able to combine geospatial data with tabular data
* Provides facilities to create/perform more advanced analysis (can be through libraries/plugins)
* Web interfaces integrate with other systems (WET)
  * Note: WET includes [OpenLayers](http://openlayers.org/), but it is out of date

### Security and Audit Requirements

Client applications can be presented in many forms. Depending on the particular use case, some client application will be desktop based tools that allow GIS professionals to analyse and derive datasets that will be published on public systems. The desktop based tools run as the user doing the analysis, and as such merely need to be approved to run on government networks given their autonomous relationship to other systems.

Web based applications present a different risk, and often require more stringent monitoring and audit ability in order to detect and trace security concerns. In cases of public facing, non-authenticated applications, the security concerns are focused on making sure the tool is available and that no edits are being made to the data (purely consumption). Authenticated systems then need to provide greater assurances that users are not able to perform nefarious actions against other users, and a more complete audit trail that includes user tracing is necessary.

### Downtime Impact

Client facing applications are the most visible aspect of downtime associated with the system. If the client interface is not available the entire sys###tems is considered to be unavailable. In many cases the client interface is also what faces the highest demand as caching strategies in the database and application tier may not be appropriate at the client tier.

Loss of services will at least be an annoyance, but in some cases could result in the inability for a department to deliver a service to clients. If a data ingestion interface is down, then the government is unable to received new data that could impact decisions. Similarly, if client interfaces to data delivery are unavailable, external stakeholders are unable to access the information they may rely on to make informed decisions on their end, impacting other levels of government or corporations.

### Application Performance

If client interfaces to systems are under performing, this would likely be seen by end users as a reduced trust in the system, and could have an impact on the perceived value of the data itself. While a poorly performing system will certainly result in lost productivity, in some instances it could also result in the loss of users as people look for alternatives.

### Data Loss

Public facing systems will generally only be providing data through a read-only source, so the risk of data loss is minimal. Systems which can make edits to data, either through desktop editing or browser based interfaces, have a higher risk of introducing data loss. The data lost in these incidences is generally reproducable through some analysis technique, but would result in a loss of productivity and a loss of confidence in the system by end users.

### Speed / Efficiency of Innovation

### Scalability / Elasticity

Web based tools should be capable of scaling dynamically. Each application will have a different amount of load that they are required to handle, but all systems should be architected in a manner than can scale to a sufficiently large number of users through the dynamic provisioning of more servers to host the client interface.

### Regional / Data Sovereignty

Client interfaces are subject to the same data sovereignty requirements as the data itself. Publicly released data has the option to be hosted on any platform, but protected data needs to be more strictly controlled. Classified information needs to be hosted internally within a department, and will have the strictest controls applied to the client interface.

### Automation

Some client interfaces are actually just APIs/services meant to receive or transmit data. These interfaces are meant for automated tools to interact with them, and will perform the lookups or analysis request based on the parameters given. These types of services will need to be able to handle significant volumes of data, as it is likely that a service such as geocoding would be queried very often.

### Operations Model

Public data is a good candidate for being exposed through an external provider. Data that requires more protection or systems that operate solely on internal networks must be operated by internal staff. In order to make the operating environment as transparent as possible to end users, open standards and common interfaces should be employed to make the transition as transparent as possible.

### Delivery Model

The delivery model will most likely be dictated by the type of data being interacted with. Desktop based clients will be able to leverage a mix of data sources through the client interface, as most tools have the ability to ingest a mix of data sources. Web based interfaces necessarily operate through a web browser, and as such rely more on data that can be exposed through other services. These services can be operating through a variety of models (SaaS, IaaS, on-prem, etc) as long as they provide an accessible interface to the client application.

## Development Requirements

### Developer Tooling

### CI/CD Process

### APIs & Automation

### Application Cache Strategies

## Deployment and Operations Requirements

### Deployment and Life Cycle Management

### Logging, Monitoring, and Alerting

### Service Healing and Scaling

### Load and Disruption Testing

### Application Delivery Strategy

## Visibility & SLA Requirements

### Scalability, Resilience, and Availability

### Disaster Recovery Strategies

### Performance Monitoring (APM)

### Support and Service Levels

## Change Management

### Compliance, Security, and Access Control

### Platform Governance

### Multi-Cloud Portability
