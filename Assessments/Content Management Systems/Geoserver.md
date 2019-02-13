# Geoserver

| Guideline                                                    | Assessment against guideline       | Met |
|--------------------------------------------------------------|---|---------------------------------|
|**Open Standard**|
|• Code base is available for re-use in a public common code repository under an open licence | Distributed under GPS v 2.0 | Y  |
|• Content can be exported in a non-proprietary format from current platform to another platform | Either accesses or stores data in common GIS formats that can be directly exported through the file system or standard APIs. Generally, data would also be directly exportable from the backing database as it is stored in common formats. | Y  |
|• Code is freely available (easy to access and available for no cost)| Hosted on GitHub | Y |
|**Strong and Robust Community**| |
|• Community is active and diverse | Maintained by an international community as funded as an OSGeo project. | Y  |
|• Community is present in more than one region | Community is spread across the globe. | Y |
|• There is a governance model publicly available for how changes are made | Project is managed by a steering committee and all processes are published openly. | Y |
|• Technical roadmap is publicly available | Roadmap and scheduling is available on project GitHub wiki. | Y |
|**Customizable** |   |
|• Tool can be adapted to be used with existing and custom extensions | Supports a plugin architecture to add additional features. | Y |
|• Tool's customizability is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Geoserver is the reference implementation for several open standards, and is consistently among the first major tools to adopt new standards/extensions. | Y |
|**Usability**|    |
|• Meets or has the capacity to meet the [Government of Canada Standard on Web Usability](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=24227) |  | Y |
|**Accessibility**|  |
|• Meets or has the capacity to meet the [Government of Canada Standard on Web Accessibility](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=23601) |  | Y |
|**Interoperability**|   |
|• Meets or has the capacity to meet the [Government of Canada Web Interoperability Standards](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=25875) |   | Y |
|**Mobile-optimized**|   |
|• Optimized for mobile devices (e.g., smartphones, tablets) or has the capacity to be optimized for mobile devices | The web interface works on mobile, as do layer preview functions. | Y |
|**Compatibility**|   |
|• Code base is compatible with security tools |   | Y |
|• Code base is compatible with analytics tools |  | Y |
|• Code base is compatible with search engines |   | Y |
|**Ease of use**|  |
|• Programming language and existing code base and extensions are easy to use | Primary project and many extensions are written in Java. Extension framework supports Python as a language as well. | Y |
|**Performance**|   |
|• Tool's performance (e.g., response time, display time, processing time) is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Geoserver runs some very heavily used geospatial websites around the globe. | Y |
|**Reliability**|   |
|• Tool's reliability (e.g., uptime, infrequency of significant issues) is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Geoserver is relied upon for many public facing systems and in corporate environments. | Y |
|**Scaleability**|   |
|• Tool's scaleability is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Geoserver can be scaled to many systems, and is out of the box ready for use in a container for quick cloud deployments. | Y |

Data Catalogue Extension

| Guideline                                                    | Assessment against guideline       | Met |
|--------------------------------------------------------------|---|---------------------------------|
|**Data Collection and distribution**|  |  |
|• Ability to collect large amounts of data in different formats | Geoserver will ingest a multitude of data formats and present them as open standards based services. Additional format support can be added through extensions. | Y |
|• Ability to distribute large amounts of data in different formats, including through an API | Output formats are configurable per data layer, with support for multiple concurrent output formats. | Y |
|• Ability to customize metadata schema| Each layer can have its own metadata, which can additionally be provided in multiple formats. | Y |