# Geospatial Systems Reference Architectures - Data Tier

Geospatial data persistence and backend analysis capabilities.

## Possible Technologies

* [PostgreSQL / PostGIS](https://postgis.net/)
* Cassandra
* Redis

# Business / Organization Requirements

Multiple GC departments have a requirement to produce and store authoritative geospatial data layers. These layers are both used internally, and distributed to the public through a variety of means to meet the mandate of the respective departments.

In general, data storage systems need to be capable of storing data compliant with the OGC [Simple Features](http://www.opengeospatial.org/standards/sfa) specification. They also need to support spatial analysis in the database tier through standard SQL [ST_* functions](http://www.opengeospatial.org/standards/sfs) to perform basic analysis (i.e.: distance calculations).

Depending on the purpose of the system (storage vs analysis), additional analytical capabilities (such as routing) would also be required. While some of the advanced analytical capabilities would potentially be implemented within the (Application Server)[geo_architecture-app_tier.md] tier, having the possibility to perform analysis in the database offers significant benefits.

## Security and Audit Requirements

In many cases, the geospatial layers that are produced and distributed represent a digital reference layer of physical infrastructure in Canada. They are not meant to provide an official legal boundary, and as such have a low - medium risk management profile.

Other layers do represent legal information though, or are used directly in the running of significant programs and services. Federal Electoral Districts are an example of this type of layer, although there are many others. These geospatial layers require a higher level of assurance that they are effectively stored and maintained. Their risk management profile would be elevated to a higher level and generalized reference layers.

## Downtime Impact

In most cases, short periods of downtime of geospatial data is acceptable. As systems move from a file based distribution into a more service oriented architecture, this becomes less acceptable as systems are likely to develop interdependencies and an outage of one system could have significant impacts on government operations. In areas where there is a significant reliance on data and services (i.e.: public safety), systems should be fully redundant.

## Application Performance

Slow database performance has a cascading effect on other systems, and results in reduced productivity for end users. In the case of public facing systems, congested or underpowered services may result in the loss of confidence in some government services and a tarnished reputation for the Government overall.

## Data Loss

Different systems will have varying requirements based on their intended purpose. In most cases, the loss of data would have a significant impact on operations. These systems require a simple and stable system to be implemented for producing regular backups.

Some services are meant to provide real-time or short lived analytics. Traffic reporting systems are an example of these types of services. In these instances, the data has little value beyond a short period of time. These types of systems are highly tolerant of data loss, as they do not try to keep the data for longer than a few hours anyway.

## Speed / Efficiency of Innovation

*-- Are there any requirements here? --*

## Scalability / Elasticity

Given the rate of change in most geospatial datasets, there is not commonly a high variability in resource requirements. The data is often pre-calculated and cached at the (Application Tier)[geo_architecture-app_tier.md] level, reducing the overall load on the database.

With the requirement to expose more analytical capabilities through web services, this is changing the paradigm of how geospatial data is managed. The analytical services require significant resources, and are often highly dynamic in nature, reducing the ability for caching services to be effective. Geocoding, for example, needs to be able to quickly answer questions relating an address to a location, but end users could ask for any location on earth, and as such caching has less benefit.

## Regional / Data Sovereignty

For any geospatial data that contains personal or protected attributes, the data must be controlled appropriately. In some instances this will require that data be housed within departmental infrastructure, while other systems can reside on cloud infrastructure.

## Automation

For systems with a high variability in consumption, there needs to be an automated an automated scaling solution in place to appropriately scale the solution to meet demand.

In instances of intense computation, such as when performing analysis or ingesting bulk data, the infrastructure can be scaled manually, although a more automated system will benefit end users.

## Operations Model

Departments have different requirements for when they can delegate the operations of their infrastructure. Other requirements will often dictate that databases be managed internally, with additional support services contracts in place for assistance, should it be required.

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
