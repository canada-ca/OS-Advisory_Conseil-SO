# Government of Canada Source Code Platform

## Context

Analyse options for Government of Canada source code version control system.

### Business Need

The latest updates to the Directive on Management of IT has clearly identified three main requirements changes related to source code management in the GoC:

1. If a custom-built application is the appropriate option, **by default any source code written by the government must be released in an open format via Government of Canada websites and services designated by the Treasury Board of Canada Secretariat** [(C.2.3.8.3)](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=15249#claC.2.3.8.3);
2. **All source code must be released under an appropriate open source software license** [(C.2.3.8.4)](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=15249#claC.2.3.8.4);
3. Share code publicly when appropriate, and when not, **share within the Government of Canada** [(C.2.3.9.5)](https://www.tbs-sct.gc.ca/pol/doc-eng.aspx?id=15249#claC.2.3.9.5).

Currently, each department manages its own source code independently and there may even be multiple methods and solutions to do so within a single organisation.

The only current option available for departments to collaborate and share source code internally is via an open source GitLab instance made available by a team at SSC. That service is offered as a best effort and there are no warranties offered for backups and support.

The current analysis has for objective to look at the options available for the GoC to manage source code based on the three high level requirements listed above while also considering the departments' specific technical and business needs.

#### Drivers

The drivers for this change are as follow:

* Policy:
  * The changes made to the directive have introduced new requirements for departments to work in the open and in collaboration. The current technical environment does not internally offer the services required to comply with this policy change.
* Efficiency:
  * There is an opportunity for increased efficiency and reuse of existing resources by reducing concurrent efforts to address similar problems and challenges as well as supporting greater collaboration across departments, thus limiting duplication of costs incurred (inner sourcing).

### Desired Outcomes

* Provide hosting options for Government of Canada software
  * GC developed/contracted open source code
  * GC developed/contracted unreleased source code
    * GC source code at the 'PROTECTED' level
    * GC source code at the classified (C/S/TS/++) levels
* Share as open source GC source code publicly.
* Share between departments code not released as OSS.

## Functional and Non-Functional Requirements

* The solution must be accessible to all departments and agencies of the GC
  * The non-private repositories and projects must be accessible and discoverable by any department or agency.
  * The non-private repositories and projects must provide the ability to other departments and agencies teams to collaborate with the project owners and maintainers (i.e. propose changes to source code similar to Pull Requests).
* Identity and Access Management must be supported by all departments
* The platform must able to be used as the primary source code repository for all departments and agencies
  * Needs 24/7, 365 days support
  * Backup of source code and repositories
  * 
* APIs and Hooks must be provided to:
  * Support departments specific SDLC environments (IDEs, OS, Network, etc.) and methodologies (traditional waterfall, DevSecOps, etc.)
  * Support departments specific CI/CD needs, e.g.:
    * Seamless and automated governance and policy implementation
    * Code repository scanning for known vulnerabilities, licence compliance, audits, reporting, etc.    
    * Automation/Orchestration: Build, Unit test, Deploy, Prod, etc.

#### Discoverability and Collaboration of projects

Below is a breakdown of the levels of discoverability and collaboration required for the type of GoC source code:

|Type of Source Code|Team|Department|Whole GC|Public|
|---|:---:|:---:|:---:|:---:|
|Open Source|X|X|X|X|
|Unreleased but unclassified|X|X|X||
|Protected|X|X|||
|Classified|X||||


#### Stakeholders

The requirements breakdown below attempts to explain which needs are associated to which stakeholder.

|Stakeholder/Requirements|Policy|Business|Technical|
|---|:---:|:---:|:---:|
|TBS|X|||
|Departments CIO|X|X||
|Team Managers||X|X|
|Developers|||X|

## Options Analysis

From an architecture standpoint, there are multiple options.

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

## Known Technology Options

* On premise (self-managed), open source
  * CVS
  * Fossil
  * Git
  * GitLab
  * Mercurial
  * Phabricator
  * SVN
* On premise (managed), open source
* On premise (self-hosted), proprietary
  * Atlasian BitBucket
  * GitHub Enterprise
  * IBM ClearCase
  * Microsoft Azure DevOps Server
  * Perforce
* Software as a Service (cloud), open source **
  * FramGit.org
  * GitLab.com
* Software as a Service (cloud), proprietary
  * Assembla
  * Azure Repos
  * BitBucket.org
  * GitHub.com
  * sourceforge.net
* Managed instance on Platform as a Service, open source
  * Azure Repos
  * GitLab.com