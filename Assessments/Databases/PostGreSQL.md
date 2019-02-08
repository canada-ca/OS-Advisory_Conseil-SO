# PostgreSQL

| Guideline                                                    | Assessment against guideline       | Met |
|--------------------------------------------------------------|---|---------------------------------|
|**Open Standard**|
|• Code base is available for re-use in a public common code repository under an open licence | PostgreSQL license, similar to MIT | Y  |
|• Content can be exported in a non-proprietary format from current platform to another platform | Many importers and exporters exist, in addition to standard format support.  | Y  |
|• Code is freely available (easy to access and available for no cost)| Downloadable from https://postgresql.org/download/  | Y |
|**Strong and Robust Community**| |
|• Community is active and diverse | Community dates back to 1986, mixes vendors and general public.  | Y  |
|• Community is present in more than one region | There are local user groups all over the world. Core team covers multiple continents. | Y |
|• There is a governance model publicly available for how changes are made | Details are outlined in the develop FAQ | Y |
|• Technical roadmap is publicly available | Roadmap covers both minor and next major revision, and includes target dates for release. No formal feature list is available. | Y |
|**Customizable** |   |
|• Tool can be adapted to be used with existing and custom extensions | Many extensions exist, such as [PostGIS](http://postgis.org) for geography types. | Y |
|• Tool's customizability is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Listed as the 4th most popular database according to https://db-engines.com/en/ranking | Y |
|**Usability**|    |
|• Meets or has the capacity to meet the [Government of Canada Standard on Web Usability](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=24227) | Not meant for user facing systems, but interface is generally accessible through plain text, and a web GUI does exist. | Y |
|**Accessibility**|  |
|• Meets or has the capacity to meet the [Government of Canada Standard on Web Accessibility](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=23601) | Not meant for user facing systems, but interface is generally accessible through plain text, and a web GUI does exist.  | Y |
|**Interoperability**|   |
|• Meets or has the capacity to meet the [Government of Canada Web Interoperability Standards](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=25875) | Complies with standard SQL specification.  | Y |
|**Mobile-optimized**|   |
|• Optimized for mobile devices (e.g., smartphones, tablets) or has the capacity to be optimized for mobile devices | Not meant to run on a mobile device, but it could.  | N |
|**Compatibility**|   |
|• Code base is compatible with security tools |   | Y |
|• Code base is compatible with analytics tools |  | Y |
|• Code base is compatible with search engines |   | Y |
|**Ease of use**|  |
|• Programming language and existing code base and extensions are easy to use | Implemented as straight C  | Y |
|**Performance**|   |
|• Tool's performance (e.g., response time, display time, processing time) is competitive with market leaders in the same tool category (e.g., Web Content Management System) |   Fairly good out of the box, but includes performance optimization documentation based on host OS. | Y |
|**Reliability**|   |
|• Tool's reliability (e.g., uptime, infrequency of significant issues) is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Documentation includes an entire section covering reliability, and different configuration options. | Y |
|**Scaleability**|   |
|• Tool's scaleability is competitive with market leaders in the same tool category (e.g., Web Content Management System) | Multiple scalability options exist. Streaming replication is supported natively for horizontal scaling. Vertical scaling is well supported. | Y |

Data Catalogue Extension

| Guideline                                                    | Assessment against guideline       | Met |
|--------------------------------------------------------------|---|---------------------------------|
|**Data Collection and distribution**|  |  |
|• Ability to collect large amounts of data in different formats | Many tools exist to import a variety of formats, in addition to those included natively.  | Y |
|• Ability to distribute large amounts of data in different formats, including through an API | Supports export of many formats, including JSON. While it can do it, this should not likely be used as a direct API. | Y |
|• Ability to customize metadata schema| Metadata schema is defined by the user. | Y |
