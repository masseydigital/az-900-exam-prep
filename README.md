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



