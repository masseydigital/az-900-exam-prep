# az-900-exam-prep
AZ-900 Azure Fundamentals Exam Prep Repository

## Cloud Benefits

### High Availability
_High availability_ is an agreed upon characteristic to ensure level of operational performance (uptime)

_Availability_ itself refers to the ability of end users to actually access the system and to complete a task.

A _load balancer_ is one example of a resource that provides high availability.

_Azure Load Balancers_ provide high availability for services, support inbound and outbound scenarios, provide low latency and throughput, and scale up to millions of flows for all TCP and UDP applications.

### Scalability
_Scalability refers to the idea oof a system in which every app or piece of infrastructure can be expanded to support increased workflows. i.e. a web application that goes from having a few users to a hundred thousand users.

There are four general areas that scalability can refer to:
1) Disk I/O
2) CPU
3) Memory
4) Network I/O

There are two main ways of scaling an application:
1) Horizontal (wide): adding more resources to an existing instance, i.e. adding a server and implementing a load balancer.  Scaling out is generally considered more difficult due to the maintenance of updates, security settings, etc. for multiple hardware components.
2) Vertical (up): adding more power to an existing instance, i.e. adding more memory, faster storage, more powerful cpu, etc.

_Azure Virtual Machine Scale Sets_ are one example of scaling that Azure provides as part of the service offering.

### Elasticity
_Elasticity_ refers to the ability to scale up and then scale back down.  Elasticity helps ensure you are using the resources you need, and effective management of resources saves you money.

Azure allows you to auto-scale resources by setting thresholds for traffic, what resources to provision, and how long to re-evaluate the thresholds.

### Agility
_Agility_ is the ability to rapidly change infrastructure requirements to meet operational needs.  With Azure and other cloud resources, companies can rapidly adjust their infrastructure to conceive, plan, and deploy applications within days.

### Fault Tolerance
_Fault Tolerance_ refers to the ability of an infrastructure to continue providing service after one or more of its components have failed.

Azure provides several _availability sets_ which allow the virtual machines and other resources to be distributed across different servers, computer racks, storage units, and network switches.

### Disaster Recovery
_Disaster Recovery_ refers to recovering from a catastrophic loss of application functionality.

Azure provides _resource groups_ across _regions_ which help with ensuring that natural disasters do not take down your application.

Azure provides the _Azure Site Recovery Service_ to ensure continuity of business apps and workloads running during outages.

### Capital Expenditures (CapEx) vs Operational Expenditures (OpEx)
_Capital Expenditures_ refers to money that a company spends towards fixed assets
i.e. Property, Plant, or Equipment (PP&E)
Generally one-time purchases

_Operational Expenditures_ refers to money that a company uses to run day to day operations.  They are usually used within the year of purchase.
Includes consumables such as printer cartridges, paper, and electricity.  Also maintenance agreements, web site hosting, and web domain registrations.

## As-a-Service Offerings

### Infrastructure-as-a-Service (IaaS)
Infrastructure as a service is having instant computing resources that can be scaled up or down depending on your requirements.  Infrastructure are servers, switches, and other computing resources that are needed to run some software.  IaaS is usually used in scenarios where you want to test and develop new methodologies since you can quickly gain necessary resources until you can figure out what you need.  It also helps with website hosting and storage backup, and recovery.  

Benefits of IaaS:
1) Eliminates capital expenditure and reduces ongoing cost by providing leased services and only what the company needs.
2) Improves business continuity and disaster recovery through use of recovery services and multiple regions.
3) Allows organizations to innovate rapidly by providing services immediately
4) Allows businesses to shift more quickly to emerging business conditions, and focus on core business.
5) Increases stability, reliability, and supportability

When to use IaaS:
1) You are a startup or small company
2) You are a large organization looking to move away from on-premise hardware
3) You are a rapidly growing company; unsure of infrastructure needs

### Platform-as-a-Service (PaaS)
Platform as a Service (PaaS) is a complete development environment in the cloud.  It includes servers, storage, and networking, but also includes middle-ware such as OS's.

It is designed to support the complete web application life cycle, avoid the expense of buying and managing software licenses, and gives you the ability to manage applications and services while the cloud provider manages the provisioning.

Common PaaS scenarios include:
1) Development Framework: provides framework developers can use to create cloud based applications.
2) Analytics and Business Intelligence: 
3) Additional Services

Advantages of PaaS:
1) Cuts coding time from built-in services
2) Add development capabilities without adding staff
3) Develop for multiple platforms more easily
4) Use sophisticated tools more affordable
5) Can support geographically distributed development teams
6) Efficiently manage application life cycle through built-in services
 
When to use PaaS:
1) Multiple developers/teams working on the same project
2) Wish to be able to create your own customized applications
3) Rapidly prototyping or deploying an application

### Software-as-a-Service (SaaS)
Software as a Services (SaaS) allows users to connect to and use cloud based apps over the network.  SaaS provides a complete software solution that can be accessed over the internet.  i.e. Webmail, Calendars, Collaboration etc.

Advantages of using SaaS:
1) Gain access to sophisticated applications
2) Pay only for what you use
3) Use free client software
4) Mobilize workforce more easily
5) Access app data from anywhere

When to use SaaS:
1) Need to quickly launch and don't have time for server issues or software
2) Short term projects that require collaboration
3) Using applications that aren't in-demand very often
4) Applications that need both web and mobile access

## Cloud Models

### Public Cloud: 
Shared with other tenants
Access services and manage accounts with internet web browser
Used for web-based mail, storage, testing, and dev.

Advantages:
1) Lower costs
2) No need to purchase hardware or software
3) Pay only for the service you use
4) No maintenance
5) Near-unlimited scalability
6) High reliability

### Private Cloud
Used for resources exclusively by one business or organization.  Can be physically located at organization's on-site data center, or can be hosted by a third-party service provider. Private clouds are generally located on-premise.  Private cloud is more secure than public cloud since security requirements are defined by the organization.

### Hybrid Cloud
The hybrid cloud is the best of both worlds.  It utilizes both on-prem and public clouds.  Data and apps can move between private and public clouds.  _Cloud bursting_ allows applications to "burst" into public cloud when demand rises above a threshold.

## Core Azure Architectural Components

### Azure Regions
An _azure region_ is a set of data centers that are connected within a latency-defined perimeter network.  As of this tutorial, there are 42 regions around the world with an additional 12 announced.  _Azure Geographies_ are areas of the world that contain at least one Azure Region.  _Regional Pairs_ are two regions that are connected in the same geography.  This allows Azure to provide updates that do not shut down a region.  At least one region in each pair will be prioritized for recovery.  

### Availability Zones
_Azure Availability Zones_ are ne or more physical locations within an Azure Region that provides independent power, cooling, and networking.  There are a minimum of (3) separate zones in all enabled regions.  The purpose of this is to protect applications from datacenter failures.

### Resource Groups
An _Azure Resource Group_ holds related resources for an Azure solution.  Developers choose which resource group resources go into.  Each resource can only exist in one resource group.

Best practices for resource groups:
1) All resources should share the same life cycle
2) Use resource groups to scope access control

_Azure Resource Manager_ enables you to work with resources in a group. It provides security, auditing, and tagging features.

_Resource_ A single service provided by Azure.

_Resource Group_ A container of resources

_Resource Provider_ provide operations for working with resources that get deployed.  i.e. Microsoft.Compute

_Resource Manager Templates_ are JSON files that define deployment procedures for resources

_Declarative Syntax_ is easily understood terminology for deploying resources (not the code needed)

## Azure Products

### Azure Compute

#### Azure Virtual Machines
On-demand, scalable computing resources which allow for the flexibility of virtualization without having to buy and maintain physical hardware.  You still need to maintain VM's with security patches, updates, etc.

Considerations:
1) VM Names
2) Locations of VMs
3) Usage
4) Size of VM
5) Number that you want
6) Operating system
7) Configuration
8) Related resources (i.e. network requirements)

#### VM Scale Sets
Allow you to create and manage a group of identical, load balanced VMs.  Number of VM's can automatically increase or decrease on demand.  They provide high-availability since applications can be distributed across multiple instances.  Provide management capabilities for applications across VMs.

Benefits
1) Easy to create multiple VMs
2) High Availability and Resiliency
3) Scalability

#### Azure App Service
Allows you to build and host web apps, mobile back-ends, and RESTful APIs.  Offers auto-scaling and high availability, supports both windows and linux, and enables automated deployments.  Allows you to build powerful web, mobile, and API apps in .Net, Java, Ruby, PHP, Python, and Docker.  It a fully managed platform that allows you to run and scale apps with maintenance, load balancing, etc.  It allows you to connect to enterprise apps within minutes.

#### Azure Functions
Are serverless computer services.  You can run code on-demand without having to provision infrastructure.  You can set trigger for function apps.  You can use many different back-end code such as node.js, C++, Java, etc.  These functions integrate with various other services which can provide triggers or pipe in/out data.

Key Features:
1) Choice of programming language
2) Pay-per-use pricing model
3) Bring your own dependencies
4) Integrated security
5) Simplified Integration
6) Flexible Development
7) Open-source

Examples of Uses:
1) Process data
2) Integrate systems
3) Work with Internet of Things (IoT)
4) Build simple APIs and microservices
5) File maintenance
6) Scheduled Tasks

### Azure Networking

#### Azure Virtual Networks
Allow many types of resources to communicate with each other.  They are scoped to a single region, but can be connected together.  They allow for isolation and segmentation.  They allow you to communicate to the Internet, and also communicate with on-prem resources.  You cna also filter network traffic through security groups.  

#### Azure Load Balancer
Allows you to scale application and create high availability.  They support inbound and outbound scenarios, provide low-latency and high throughput, and scales up to millions of flows.

Uses:
1) Load-balance incoming internet traffic to VMs
2) Load-balance traffic inside of a virtual network
3) Port forward traffic to a specific port
4) Provide outbound connectivity

Features:
1) Load balancing
2) Port forwarding
3) Application Agnostic
4) Automatic Reconfiguration
5) Health probing
6) Outbound connections

A _public load balancer_ maps the public ip address and port number of incoming traffic to the private ip address and port number of the VM, and vice versa for the rsponse traffic from the VM.

An _internal load balancer_ redirects traffic only to resources inside of a virtual network.  

#### Virtual Private Network (VPN) Gateway
VPN Gateway allows you to send encrypted traffic between an Azure virtual network and an on-premise location over the public internet.  Only one VPN Gateway can be assigned to an azure virtual network, however you can create multiple connections to the same gateway.  A VPN Gateway is composed of two or more VMs that are deployed to a gateway subnet.  You can also create an IP SEC or VPN tunnel that connects two VPN gateways together (referred to a v-net to v-net connection).  You can also create a cross-prem IPSEC between an on-prem gateway referred to a _site-to-site_ vpn gateway.  In addition you can create a point to site VPN connection which is referred to a VPN over IPV2 or SSTP connection.

Support VPN Technologies
1) Site-to-site
2) Multi-site
3) Point-to-Site
4) VNet-to-VNet
5) ExpressRoute

#### Content Delivery Networks (CDNs)
The _Azure Content Delivery Network_ is a distributed network of servers that can efficiently deliver web content to users.  They store _cached_ content on edge servers in point-of-presence (POP) locations, thus minimizing latency.  

Benefits: 
1) Better performance and improved user experience for end-to-end users.
2) Large scaling to better handle instantaneous high loads.
3) Distribution of user requests.

Key Features:
1) Dynamic Site Acceleration
2) CDN caching rules
3) HTTPS custom domain support
4) Azure diagnostic logs
5) File compression
6) Geo-filtering

### Azure Storage

#### Blob Storage
Microsoft's object storage (unstructured data) solution for cloud optimized storing of massive amounts of data.

Uses:
1) Serving images or documents directly to a browser
2) Storing files for distributed access
3) Streaming video and audio
4) Writing to log files
5) Storing data for backup and restore
6) Storing data for analysis

Azure blob storage is accessible through REST api, CLI, powershell, and Azure storage client library.

Resources:
_Storage account:_ provides unique namespace in Azure for data.
_Container:_ Organizes a set of blobs, similar to a directory in a file system (similar to a file directory)
_Blob:_ Block blob (text/binary data), append blob (optimized for append operations), page blob (store random access files up to 8TB in size)

#### Disk Storage
Virtual machines in Azure use disks as a place to store an OS, applications, and data.  All Azure VMs have at least two disks (A windows OS disk, and a temporary disk).  Both the OS disk and the image are virtual hard disks (VHDs) stored in an Azure storage account.

Types of disks
1) _Operating System Disk:_ every virtual machine has one that stores the OS. (C:)
2) _Temporary Disk:_ provides short term storage, may be lost when VM is redeployed (D:)
3) _Data Disk:_ Stores application data (<Letter>:)

Performance Tiers:
1) Standard HDD Disks
2) Standard SSD Disks (Recommended for most workloads)
3) Premium SSD Disks

#### File Storage
Azure files provide a file share in the cloud that can be mounted concurrently by cloud or on-prem machines.  Azure file shares can be cached on windows servers with azure file sync.

Benefits:
1) Shared access
2) Fully Managed
3) Scripting and Tooling
4) Resiliency
5) Familiar Programmability

#### Archive Storage
Lowest files storage cost, but higher cost for accessing data.  Blobs that are in archive can't be read, copied, overwritten, or modified.  Typical usage scenarios include long-term backup, secondary backup, and archival datasets.  i.e. security camera footage, old xrays/mris, etc.

### Azure Databases

#### CosmosDB
Azure CosmosDB is a globally distributed, multi-model database service.  It allows you to elastically and independently scale throughput and storage.  It provides fast, single-digit millisecond data access through comprehensive service level agreements (SLAs).

Benefits:
1) Turnkey Global Distribution: Build highly responsive and highly available applications worldwide.
2) Always On: Provides 99.999% high availability for both reads and writes
3) Elastic Scalability of Throughput and Storage: Elastically scale up from thousands to hundreds of millions of requests/second
4) Guaranteed Low Latency: Less than 10-ms latencies for both reads and writes in the 99th Percentile.

#### Azure SQL Database
Azure SQL Database is a relational database-as-a-service (DBaaS) base don the Microsoft SQL service.  

Deployment Options:
1) Deploy as a single database
2) Deploy as a pooled database in an elastic pool
3) Deploy as part of a collection of databases known as a _managed instance_

#### Azure Database Migration Service
The _Azure Database Migration Service_ enables seamless migration of existing databases while minimizing downtime.  It integrates some of the functionality of existing tools into a highly available solution.  Any remediation must still be done by the user.  

#### Azure SQL Data Warehouse
SQL Data Warehouse is a _cloud-based enterprise data warehouse (EDW)_ that leverages _Massively Parallel Processing (MPP)_.  You can import data with a simple PolyBase T-SQL query and then run high-performance analytics.  It stores data into relational tables with columnar storage.  This reduces data storage costs, and improves query performance.  Once data is stored, you can run data analytics at massive scale.  

## Other Azure Services

### Internet of Things (IoT)
_IoT Hub_ is a managed service that serves as a central message hub between IoT devices.  You can connect virtually any device on IoT hub with communication from device to cloud and from cloud to device.  It also supports multiple messaging platforms.  IoT Hub allows you to scale solutions, secure communications, route device data, and integrate with other services.  It also allows you to configure your devices while making your solution highly available.  You can use the Azure IoT device SDK libraries to build applications that run on your devices.

_IoT Central_ is a fully managed IoT SaaS solution.  

### Big Data Analytics

_HDInsight_ enables clusters of managed Hadoop instances.  It deploys and provisions Apache Hadoop clusters in the cloud.  And allows you to manage, analyze, and report on big data with high reliability and availability.  It uses the Hortonworks data platform hadoop instance.

_Azure Data Lake Analytics_ is an on-demand analytics job service that simplifies big data.  It can handle jobs any scale instantly.

Benefits:
1) Dynamic Scaling
2) Integrates Seamlessly
3) Works with all Azure data

### Artificial Intelligence (AI)
_Azure Machine Learning Service_ allows you to train, deploy, automate, and manage machine learning models.  It is a cloud-based environment that you can use to develop, train, test, deploy, manage, and track machine learning models.  It supports open source technologies and has support for rich tools.

_Azure Machine Learning Studio_ is a drag and drop tool that you can use to build, test, and deploy predictive analytics solutions.  It publishes models as web services, and provides an interactive, visual workspace to easily build, test, and iterate on a predictive analysis model.  There is no programming required.

### Azure Logic Apps
Azure Logic Apps allow you to automate and orchestrate tasks, business process, and workflows.  Examples of workloads that can be automated with logic apps are processing & routing orders and moving files from an FTP server to Azure storage.

Azure Logic Apps allow you to visually build workflows with easy to use tools, get started faster with logic app templates, connect disparate systems across different environments, and provide first-class support for enterprise integration and B2B scenarios.

### Azure CLI
Is Microsoft's cross-platform command-line experience for managing Azure resources.  You can use it in the browser with Azure Cloud Shell, or install it on MacOS, Linux, or Windows.  It is best used for building automation scripts that work against the Azure Resource Manager.

### Azure Powershell
Azure Powershell provides a set of cmdlets that use the Azure Resource Manager model for managing your Azure resources.  It uses the .Net standard, and ads a new Az module to work with Azure.

### Azure Portal
The Azure portal allows you to view all of your resources through one website.  You can personalize your Azure experience through the interface.  You can also use RBAC controls to provide users with need-to-use content.  It gives you visibility into billing.

### Azure Advisor
Azure Advisor is a personalized cloud consultant.  It analyzes resource configuration and usage telemetry, and then recommends solutions.  It improves the cost effectiveness, performance, high availability, and security of Azure resources.  It will give you proactive, actionable, and personalized recommendations for resources.

Four Recommendation Areas
1) High Availability
2) Security
3) Performance
4) Cost

## Securing Network Connectivity in Azure

### Azure Firewall
Azure Firewall is a cloud based network security service.  It's a fully stateful firewall as a service capability with high availability.  It uses a static ip address for resources.  

Features:
1) Application FQDN Filtering Rules
2) Network Traffic Filtering Rules
3) FQDN Tags
4) Outbound SNAT support
5) Inbound DNAT Support
6) Azure Monitor Logging

### Azure DDoS Protection
Distributed Denial of Service attacks are the most concerning attacks used by exhausting a system's resources.  This can be combined with application best practices to avoid DDoS attacks.  Azure DDoS protection can prevent Volumetric attacks, protocol attacks, and resource layer attacks.

### Network Security Groups (NSG)
Azure Network Security Groups allow you to filter network traffic by controlling inbound/outbound network traffic.  NSG will provide 3 outbound and 3 inbound rules by default.

## Azure Identity Services

### Authentication and Authorization
_Authentication:_ the act of validating that users are who they claim to be. i.e. entering a pin, username and password, biometrics
_Authorization:_ the process of providing the user specific permissions to access resources or functions

### Azure Active Directory
_Azure Active Directory_ is Azure's cloud-based Identity and Access Management (IAM) service.  It allows users to sign-in and access internal and external resources.  Azure AD is intended for IT Admins, App Developers, Office 365 subscribers, etc. Azure AD has free and paid pricing tiers.

### Azure Multi-Factor Authentication
_Multi-Factor Authentication (MFA)_ requires two or more authentication methods to gain access to a system.  They generally break down to having _Something you know_, _Something you have_, and _Something you are_.  

## Azure Security Tools and Features

### Azure Security
Containing many different operating systems, programming languages, frameworks, etc. Azure contains many different security methods to help ensure customers are developing secure apps.

Four Security Areas:
1) Secure Platform: Internal audits, mandatory security training, penetration testing
2) Compliance: Trust Center, Common Controls Hub, Cloud Services Due Diligence Checklist
3) Privacy & Controls: Stringent Privacy Standards, Law Enforcement, Control on data location
4) Transparency: How Microsoft secures customer data, how it manages data location, and who in Microsoft can access data.

Six Functional Areas:
1) Operations: Security & Audit Dashboard, Azure Resource Manager, Azure Security Center
2) Applications: Web Application Vulnerability Scanning, Penetration Testing, Web Application Firewall
3) Storage: Role-Based Access Control, Shared Access Signature, Encryption
4) Networking: Network Layer Controls, Network Security Groups
5) Compute: Antimalware & Antivirus, Hardware Security Modules, Virtual Machine Backup
6) Identity: Secure Identity, Secure Apps & Data

### Azure Key Vault
Cloud-hosted management service which allows users the ability to encrypt keys and small secrets.  Neither applications, nor Microsoft has access to keys stored in Azure Key Vault.  Azure Key Vault provides secrets, keys, and certificates management, and storage of secrets is backed by Hardware Security.

### Azure Information Protection (AIP)
Azure Information Protection (AIP) is a cloud based service which allows users to label/classify/protect documents and emails.  Labels ca be applied automatically by administrators, manually by users, or a combination of both.  Metadata is also attached to documents which allows other systems to work with labeled documents.  AIP uses Azure Rights Management to protect data.  You can use Right Management Templates to more easily apply labels to documents.

### Azure Advanced Threat Protection (ATP)
Azure Advanced Thread Protection is a cloud based security solution which allows admins to investigate advanced threats, compromised identities, and malicious insider actions as well as user activities across the network.  It uses adaptive baselining to detect advanced threats before they occur through use of learning based analytics.

## Azure Governance Methodologies
_Governance_ validates that an organization can achieve its goals through effective & efficient use of IT.

### Azure Policies
Azure Policy is a service which can be used to create, assign, and manage policies and enforces rules and effects over resources.  It ensures that resources remain compliant with corporate standards and SLAs.  

Policy differs from RBAC as RBAC focuses on user actions at different scopes.  Azure policies focus on resource properties during deployment such as types or locations of resources.  Azure policies default to Allow & Explicit Deny.

### Initiatives
An Initiative is a collection of policy definitions tailored towards achieving a singular overarching goal.  It simplifies managing & assigning policy definitions.  An _Initiative Assignment_ is an Initiative Definition assigned to a specific scope.  _Initiative Parameters_ are used by the policy definitions within the initiative.

### Role-Based Access Control (RBAC)
RBAC is an authorization system built on Azure Resource Manager, and provides fine-grained access management of resources in Azure.  i.e. a network administrator having access to network resources on Azure and a database administrator having access to databases on Azure.  RBAC can also apply to applications needing access to resource groups.

_Security Principal:_ is a user, group, service principal, or managed identity that is requesting access to Azure resources.

_Role Definition:_ is a collection of permissions, and lists the operations that can be performed.

_Scope:_ is the boundary that the access applies to, and can be specified at multiple levels.  In Azure, it is hierarchical.

_Role Assignment:_ are attaching a role definition to a user, group, service principal, or managed identity at a particular scope.

Four Default Roles:
1) Owner: Full access to resources
2) Contributor: Create / Manage all types of Azure resources, cannot grant access to other users
3) Reader: View existing resources
4) User Access Administrator: Manager users access to Azure resources

There are many other more specific roles that can be used, i.e. SQL Database Administrator.

### Locks
Locks are used to prevent other users from accidentally deleting or modifying critical resources.  You can set the lock level to CanNotDelete or ReadOnly.  Applying a lock in a parent scope applies it to all child resources.  Management locks apply to a user group or role.  Only Owner and User Access Administrator roles can provision locks.

### Azure Advisor Security Assistance
Azure Advisor Security Assistance is a consolidated list view of recommendations that is integrated with Azure Security Center.

## Monitoring and Reporting

### Azure Monitor
Azure Monitor is a service that maximizes availability and performance of applications by collecting, analyzing, and acting on telemetry.  The data that Azure monitor collects can be broken down into _Metrics_ and _Logs_.  Log data that is collected is stored in _Log Analytics_.  Log Analytics supports a rich query language to quickly retrieve, consolidate, and analyze collected data.

Azure Monitor Collects: 
1) Application Monitoring Data
2) Guest OS Monitoring Data
3) Azure Resource Monitoring Data
4) Azure Subscription Monitoring Data
5) Azure Tenant Data

### Azure Service Health
Provides a personalized guidance and support of Azure service resources.  

Areas:
1) Azure Status: A global view of the health of Azure resources
2) Service Health: A personalized view of the health of Azure
3) Resource Health: A deeper view of the health of individual resources provided.

Benefits:
1) Personalized Dashboard
2) Receive Guidance & Support
3) Targeted Notifications
4) Shared Details and Updates Easily

## Privacy, Compliance, and Data Protection Standards

### General Data Protection Regulation (GDPR)


### ISO


### NIST


### Trust Center


### Service Trust Portal


### Compliance Manager


### Azure Government Services


## Azure Subscriptions


## Planning and Management of Costs

### Azure Free Accounts


### Resource Pricing


### Pricing Calculator


## Support Options


## Azure Service Level Agreements (SLAs)
