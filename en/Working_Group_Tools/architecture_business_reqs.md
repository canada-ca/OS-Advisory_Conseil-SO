# Business Requirements for Reference Architectures

In order to ensure the Reference Architectures which the Tools Working Group produces are understood and relevant to a broader audience, it is important that the context and tradeoffs of the architecture be published with the architectural design.  Below we have outlined a variety of areas for consideration when producing an architecture.

Keep in mind that your recommended architecture is unlikely to address every category below, but they are worth reviewing to ensure the spirit of the design is effectively communicated and which areas have been focused on.


## Business / Organization Requirements

In this section we cover the high level business impact requirements.  What is the business case solving for and how critical are the different areas of potential impact? 

### Security and Audit Requirements

What is the business impact of being compromised?  Are there requirements for PCI, SOC, HIPPA/PHIPA, CSA, GDPR, or other security / audit requirements for this use case?

### Downtime Impact

What is the impact of downtime for this use case?  Will you lose users or is it simply an annoyance?

### Application Performance

What is the impact of the system being slow or suffering from congestion?  Will you lose users, revenue or productivity?

### Data Loss

What is the impact of losing data?  Will you lose users, revenue or productivity?  Are there fines for losing data?

### Speed / Efficiency of Innovation

Is there a feature velocity problem we need to address?  Is continued innovation and evolution of the design / use case a high priority?

### Scalability / Elasticity

Is the workload being addressed resource consistent or does it have highly variable resource requirements?  Is dynamic scaling based on load a requirement for this use case?

### Regional / Data Sovereignty

Is it important where the data lives?  Does it have to stay within a region?  Are there implications around which providers can be used based on where they are located or the country where the provider is headquartered from? 

### Automation

To what extend does the implementation need to be automated?  Will the infrastructure resources provisioning be automated?  Will the platform / application architecture be automated?  Is a CI/CD process required in order to provide consistent delivery?

### Operations Model

Who is operating the implementation?  Is it manage internally or by a provider?  What are the support implications and how are issues addressed when encountered by an; end user, operator or business owner?

### Delivery Model

How is this architecture being delivered to its users?  Is it a Software-as-a-Service (SaaS) model?  Is it an on-premises architecture delivered to a very targeted group?  Is multi-tenancy required?


## Development Requirements

In this section we cover details around the developer experience and the expectations around contribution and release management.

### Developer Tooling

Where is the code managed (code repository) and are there image repositories in scope?  What tooling is used for ensuring code quality, security scanning and CI/CD pipelines?

### CI/CD Process

What CI/CD process is used?  How are releases and maintenance plans managed?  What testing and sign-off requirements are in play?

### APIs & Automation

What integrations and automation is required / ideal for this use case?  For example, should SSL certs be automatically provisioned from LetsEncrypt for the deployment. 

### Application Cache Strategies

Does the implementation depend on application cache strategies?  Is their a CDN in play?  What layers of the architecture leverage caching and should they be called out for performance or troubleshooting reasons?


## Deployment and Operations Requirements

In this section we cover details around the operational model and how the architecture is managed over time.

### Deployment and Life Cycle Management

How is the life cycle of the deployment managed?  Does the architecture leverage rolling upgrades, blue/green deployments, canary testing, etc?  How can the architecture be scaled and which components can be scaled independently?

### Logging, Monitoring and Alerting

How is logging and monitoring managed?  Are logs centralized?  When monitoring probes produce alerts, who is responsible for investigating and escalating the alerts?  What infrastructure monitoring is being done?  What application monitoring is being done?

### Service Healing and Scaling

In the event of infrastructure failure, what is the process for service healing?  How are the different components of the architecture scaled and are there dependencies to consider when scaling different components?

### Load and Disruption Testing

What load characteristics do we expect the architecture to be able to handle?  If there is degradation or disruption of service, what controls are in place to mitigate the issue?  Are there tests in place to validate the expected load and service level requirements?

### Application Delivery Strategy

Is an Application Delivery Controller (ADC) required?  If multiple regions or clouds are leveraged, is a global load balancer in play?  If APIs are exposed, are they versioned?  If a service is being delivered, is there a backwards compatibility expectation?  If so, for how many releases or what period of time?  


## Visibility & SLA Requirements

In this section we cover details around managing SLAs and the visibility of the operational details in play.

### Scalability, Resilience and Availability

How is the architecture scaled?  What resiliency measures are provided by this architecture?  Are components deployed in an N+1 configuration so they can be updated without downtime?

### Disaster Recovery Strategies

Is a disaster recovery (DR) strategy defined for this architecture?  What is the expected recovery path if the event that components of the architecture are accidentally deleted?  What is the backup strategy?  Is there a process to validate the backups are working?  Reminder: Snapshots are not backups (they don't quiesce stateful and memory bound services).

### Performance Monitoring (APM)

Is application performance monitoring required?  If there are multiple infrastructure layers (IaaS, PaaS, App) then an APM can be very helpful to isolate which layer/team of the infra is responsible.  Are there end user performance SLAs in play that need to be accounted for?

### Support and Service Levels

Are there specific service availability levels which have to be maintained?  Who is responsible for supporting the operations?  Is there a vendor provided support contract in play?  What components are under vendor support and which are the responsibility of the internal operations team? 

### Change Management

What is the change management strategy?  Is there a Change Advisory Board (CAB) who manages all changes to the deployment?  What is the product / code release process?  Is there monitoring at the OS level to alert on security updates?  Who is responsible for managing these updates and what process must they follow?

### Compliance, Security and Access Control

Does this deployment have specific compliance and security requirements?  Is everything exposed over SSL?  How is access control to these environments managed?  Is there a requirement for penetration testing on this environment?  Is intrusion or anomaly detection required for this type of service?  What encryption requirements are need?  Encryption at rest?  Encryption in flight?  Is there a requirement for an asymmetrical key implementation in order to encrypt the data from the infrastructure operators and admins?

### Platform Governance

What roles are expected to be associated with this deployment and what permissions should they have?  Common roles to consider are; end user, system administrator, vendor support agent, etc...

### Multi-Cloud Portability

How dependant is this architecture on a specific cloud or infrastructure provider?  Is the automation to deploy the architecture only available for a specific provider?  Are there specific services that this architecture depends on which are cloud specific (eg: AWS Lambda)?  If a container platform is utilized, is it a platform which can be utilized across different providers (eg: Kubernetes)?