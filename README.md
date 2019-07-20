# az-900-exam-prep
AZ-900 Azure Fundamentals Exam Prep Repo

## Cloud Benefits

### High Availability
_High availability_ is an agreed upon characteristic to ensure level of operational performance (uptime)

_Availability_ itself refers to the ability of end users to actually access the system and to complete a task.

A _load balancer_ is one example of a resource that provides high availability.

_Azure Load Balancers_ provide high availability for services, support inbound and outbound scenarios, proivde low latency and throughput, and scale up to millions of flows for all TCP and UDP applications.

### Scalability
_Scalability refers to the idea oof a system in which every app or piece of infrastructure can be expanded to support increased workflows. i.e. a web application that goes from having a few users to a hundred thousand users.

There are four general areas that scalability can refer to:
1) Disk I/O
2) CPU
3) Memory
4) Network I/O

There are two main ways of scaling an application:
1) Horizontal (wide): adding more resources to an existing instance, i.e. adding a server and implementing a load balancer.  Scaling out is generally considered more difficult due to the maintenance of updates, secuirty settings, etc. for multiple hardware components.
2) Vertical (up): adding more power to an existing instance, i.e. adding more memory, faster storage, more powerful cpu, etc.

_Azure Virtual Machine Scale Sets_ are one example of scaling that Azure provides as part of the service offering.

### Elasticity
_Elasticity_ refers to the ability to scale up and then scale back down.  Elasticity helps ensure you are using the resources you need, and effective management of resources saves you money.

Azure allows you to autoscale resources by setting thresholds for traffic, what resources to provision, and how long to re-evalutate the thresholds.

### Agility
_Agility_ is the ability to rapidly change infrastructure requirements to meet operational needs.  With Azure and other cloud resources, companies can rapidly adjust their infrastructure to conceieve, plan, and deploy applications within days.

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
1) Eliminates captial expenditure and reduces ongoing cost by providing leased services and only what the company needs.
2) Improves business continuity and disaster recovery through use of recovery services and multiple regions.
3) Allows organizations to innovate rapidly by providing services immediately
4) Allows businesses to shift more quickly to emerging business conditions, and focus on core business.
5) Increases stability, reliability, and supportability

When to use IaaS:
1) You are a startup or small company
2) You are a large organization looking to move away from on-premise hardware
3) You are a rapidly growing company; unsure of infrastructure needs

### Platform-as-a-Service (PaaS)
Platform as a Service (Paas) is a complete development environment in the cloud.  It includes servers, storage, and networking, but also includes middleware such as OS's.

It is designed to support the complete web application lifecycle, avoid the expense of buying and managing software licenses, and gives you the ability to manage applications and services while the cloud provider manages the provisioning.

Common PaaS scenarios include:
1) Development Framework: provides framework developers can use to create cloud based applicaions.
2) Analytics and Business Intelligence: 
3) Additional Services

Advantages of PaaS:
1) Cuts coding time from built-in services
2) Add development capabilities without adding staff
3) Develop for multiple platforms more easily
4) Use sophisticated tools more affordablys
5) Can support geographically distributed development teams
6) Efficiently manage application lifecycle through built-in services

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
Used for resources exclusively by one business or organization.  Can be physically located at organization's on-site datacenter, or can be hosted by a third-party service provider. Private clouds are generally located on-premise.  Private cloud is more secure than public cloud since security requirements are defined by the organization.

### Hybrid Cloud
The hybrid cloud is the best of both worlds.  It utilizes both on-prem and public clouds.  Data and apps can move between private and public clouds.  _Cloud bursting_ allows applications to "burst" into public cloud when demand rises above a threshold.

## Core Azure Architectural Components

### Azure Regions
An _azure region_ is a set of data centers that are connected within a latency-defined perimeter network.  As of this tutorial, there are 42 regions aroudn the world with an additional 12 announced.  _Azure Geographies_ are areas of the world that contain at least one Azure Region.  _Regional Pairs_ are two regions that are connected in the same geography.  This allows Azure to provide updates that do not shut down a region.  At least one region in each pair will be prioritized for recovery.  

### Availability Zones
_Azure Availability Zones_ are ne or more physical locations within an Azure Region that provides independent power, cooling, and networking.  There are a minimum of (3) separate zones in all enabled regions.  The purpose of this is to protect applications from datacenter failures.

### Resource Groups
An _Azure Resource Group_ holds related resources for an Azure solution.  Developers choose which resource group resources go into.  Each resource can only exist in one resource group.

Best practices for resource groups:
1) All resources should share the same lifecycle
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
8) Related reources (i.e. network requirements)

#### VM Scale Sets
Allow you to create and manage a group of identical, load balanced VMs.  Number of VM's can automatically increase or decrease on demand.  They provide high-availability since applications can be distributed across multiple instances.  Provide management capabilities for applications across VMs.

Benefits
1) Easy to create multiple VMs
2) High Availability and Resiliancy
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

#### Virtual Prive Network (VPN) Gateway
VPN Gateway allows you to send encrypted traffic between an Azure virtual network and an on-premise location over the public internet.  Only one VPN Gateway can be assigned to an azure virtual network, however you can create multiple connections to the same gateway.  A VPN Gateway is composed of two or more VMs that are deployed to a gateway subnet.  You can also create an IP SEC or VPN tunnel that connects two VPN gateways together (referred to a v-net to v-net connection).  You can also create a cross-prem IPSEC between an on-prem gateway referred to a _site-to-site_ vpn gateway.  In addition you can create a point to site VPN connection which is referred to a VPN over IPV2 or SSTP connection.

Support VPN Technologies
1) Site-to-site
2) Multi-site
3) Point-to-Site
4) VNet-to-VNet
5) ExpressRoute

#### Content Delivery Networks (CDNs)
The _Azure Content Delivery Network_ is a distributed network of servers that can efficiently deliver web content to users.  They store _cached_ content on edge serers in point-of-presence (POP) locations, thus minimizing latency.  

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

Azure blog storage is accessible through REST api, CLI, powershell, and Azure storage client library.

Resources:
_Storage account:_ provides unique namespace in Azure for data.
_Container:_ Organizes a set of blobs, similar to a directory in a file system (similar to a file directory)
_Blob:_ Block blob (text/binary data), append blob (optimized for append operations), page blob (store random access files up to 8TB in size)

#### Disk Storage
Virtual machines in Azure use disks as a place to store an OS, applications, and data.  All Azure VMs have at least two disks (A windows OS disk, and a temporary disk).  Both the OS disk and the image are virtual hard disks (VHDs) stored in an Azure storage account.

Types of disks
1) _Operating System Disk:_ every virtual machine has one that stores the OS. (C:)
2) _Temporary Disk:_ provides short term storage, may be lost when VM is redployed (D:)
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
3) Elastic Scalability of Throughpout and Storage: Elastically scale up from thousands to hundreds of millions of requests/second
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

### Other Azure Services

#### Internet of Things (IoT)

#### Big Data Analytics

#### Artifical Intelligence (AI)

#### Azure Logic Apps

#### Azure CLI

#### Azure Powershell

#### Azure Portal

#### Azure Advisor

### Securing Network Connectivity in Azure

#### Azure Firewall

#### Azure DDoS Protectin

#### Network Security Groups

### Azure Identity Services

#### Authentication and Authorization

#### Azure Active Directory

#### Azure Multi-Factor Authentication

### Azure Security Tools and Features

#### Azure Security

#### Azure Key Vault

#### Azure Information Protection

#### Azure Advanced Threat Protection

### Azure Governance Methodologies

#### Azure Policies

#### Initiatives

#### Role-Based Access Control (RBAC)

#### Locks

#### Azure Advisor Security Assistance

### Monitoring and Reporting

#### Azure Monitor

#### Azure Service Health

### Privacy, Compliance, and Data Protection Standards

#### GDPR

#### ISO

#### NIST

#### Trust Center

#### Service Turst Portal

#### Compliance Manager

#### Azure Government Services

### Azure Subscriptions

### Planning and Managment of Costs

#### Azure Free Accounts

#### Resource Pricing

#### Pricing Calculator

### Support Options

### Azure Service Level Agreements (SLAs)