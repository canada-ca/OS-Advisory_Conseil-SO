# Government of Canada Source Code Platform

## Objective

Analyse options for a Government of Canada source code version control system.

## Business Requirements

* Accessible to all departments and agencies
  * Sole source code repository for all departments and agencies
* Needs 24/7, 365 days support
* Identity and Access Management integrated to all departments
* Seamless and automated governance and policy implementation
  * E.g: Code repository scanning for known vulnerabilities, licence compliance, audits,
* DevSecOps functionalities available for all
  * E.g.: automated CI testing, build, deploy, etc.
* Configuration options per departments, per teams
  * Support multiple configuration options for the development ecosystem tools such as the OS development environments, IDEs, automated testing tools, deployment models, etc.
* Package Management (?)
  * Centralized version of package Management
  * Centralized security release mechanism

## Options Analysis

Primary question:   Internal only vs external access to GC instance?

* On premise (self-managed), open source
* On premise (managed), open source
* On premise (self-hosted), proprietary
* Software as a Service (cloud), open source **
* Software as a Service (cloud), proprietary
* Managed instance on Platform as a Service, open source

** Even if the SaaS is open source, the hosted nature of the instance means that the exit strategy may be as complex and costly as with a proprietary solution. Need to consider managed instance running on PaaS option.

All options must support use of additional tools and services configurations:

* CI testing
* Package/Dependency Management
  * Known security vulnerabilities
  * Licence compliance
  * Audits
  * Notices
* Governance and policies automated enforcement
  * Exception management
