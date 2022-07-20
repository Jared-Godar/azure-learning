# Azure Fundamentals AZ-900

## Introduction

### Overview

- Proficiency
- Certification
- Credibility
- Networking
- Certification Portal

### Portal

- Personalize
  - Dashboards
  - Layouts
  - Workfloe
  - Colors
- Access Control
  - Management and government
- Cost management
  - Current and projected
- One stop shop
- Constantly updates
- Multi-platform

### CLI

- [Documentation](https://docs.microsoft.com/en-us/cli/azure/?view=a)
- [Commands](https://docs.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest)
- [Quickstart](https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart)
- Stable - tex commands don't change
- Structures - logical
- Cross-platform
- Automate commands
- Logging - keep task of who did once

### PowerShell

- [Documentation](https://docs.microsoft.com/en-us/powershell/azure/?view=azps-8.0.0&viewFallbackFrom=azps-1.6.0)
- [Quickstart](https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart-powershell)
- Another CLI
- Often pre-installed on windows
- Text-based CLI
- "Commandlets" scripts
  - "New-AzVM" creates new VM
- Uses Resource manger
- Versatile
  - Useful for many other tasks

### Cloud Shell

- Interactive
- Browser-accessible
- Shell
  - Bash - like CLI
  - Powershell
- Access from the web
- Dedicated storage persists between sessions
- Complete file editor

### Mobile Apps

- iOS and Android
- Quick information on the go
- Alerts
- Resources
- System Health
- Quickly diagnose and potentially fix resources
- Azure resource manager

### ARM Templates

- [Templates](https://azure.microsoft.com/en-us/resources/templates/?WT.mc_id=ACloudGuru_Learn_multiple-learn-wwl)
- Automate and replicate
  - Tasks
  - Actions
  - Processes
- Azure Resource Manager
  - Describe resource usage - create, delete alter
  - Common Syntax
  - Idempotent
  - JSON

### Azure Advisor

- Cost savings
- Security
- Availability
- Reliability
- Performance
- Operational Excellence
- Checks for little things you may not be aware of

### Summary

- Benefits of certification
- Azure Portal
- CLI
- PowerShell
- Cloud Shell
- Mobile Apps
- ARM templates

---

## 2: Core Cloud Knowledge

[Benefits of Cloud Computing](https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-cloud-computing/#benefits)

### Language of Cloud Computing

- On-demand availability of computer system resources
  - Compute
  - Networking
  - Storage
- Distributed data centers
- Low cost
- Ease of adoption
- Nearly unlimited resources
- High Availability
- Fault Tolerance
  - Mitigation automation
- Disaster Recovery
  - Related to HA/FT
  - Plans to recover critical systems and operations
  - Designated time to recovery and recovery point
- Scalability
  - Add more resources on as-needed basis
  - Deal with influx or surge of users
  - In/out - add more resources
  - Up/down - Change resource type to more powerful
  - Autoscaling automatically according to rules
    - Timing
    - CPU usage
- Elasticity
- Agility
  - Rapidly develop, test and launch

### Economy of Cloud Computing

- Capital Expenditure (Capex)
  - Acquire and maintain fixed assets
- Operational Expenses (Oped)
  - Ongoing cost for running a product
- Per second pricing for usage
- Consumption-based pricing, pay -as-you-go
- Not locked into any fixed monthly expense

### Cloud Service Models

- IaaS
  - Complete control of infrastructure
  - Dynamic and flexible
  - Highly scalable
  - VM, VNet, Storage
- PaaS
  - Resource virtualized
  - Service assist
  - App Services, Azure CDN, Cosmos DB
- SaaS
  - Managed
  - Users not responsible for hardware/software updates
  - Microsoft 365
- Serverless
  - Azure Functions
  - Extreme PaaS via abstraction

#### Shared Responsibility Model

- On premisis - you do it all
- Cloud - more responsibility shifts to service provider

### Azure Marketplace

- Certified and less maintenance
- Efficient
- New Markets
- Support
- Great shortcut for using or selling a service

### Cloud Architecture Models

#### Private

- Complete control
- High security and privacy
- Expensive
- Must maintain everything

#### Public

- AWS, Azure, GCP, etc
- No hardware purchase and maintenance of infrastructure
- Low monthly fees
- No control over features and versions

#### Hybrid

- Mix of private and public
- Tiered approach to cloud migration
- Some services must live on premesis for regulatory and governance reasons
- Alleviate large CapEx investments
- Complex infrastructure
  - More moving parts

---

## 3. Azure Architecture

### Regions

> " A region is a set of datacenters deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network."

- More than one physical data centers
- Latency: time it takes dat ato travel
- "two or more not too fat apart connected by fiber"
- COnsiderations in choosing region
  - Proximity to users
  - Features - not all available in all regions
  - Price - varies regionally (20-30%)
  - Find balance between three

### Paired Regions

- All regions paired with another within same geographic area
- Outage failover
- Planned updates - only one paired region updated at a time
- Replication CRR

### Availability Zones

- Unique physical locations within a region
- At least three zones per region
- Independent power, cooling, networking
- VMs - select how many zones it will be in 1-3+
- ZOne-redundant storage automatically replicated across zones
- High availability

### Resource Groups

- Everything in Azure is inside a resource group
  - Container for related resources for an azure solution
- Critical to manage resources
- Each resource can only exist in one group
- Can Add/remove
- Move resources from one group to another
- Resources from multiple regions can be in one resource group
- Access control at group level
- Can interact with different resources in different groups

### Azure Resource Manager (ARM)

- Create, manage, delete resources
- Portal, powershell, CLI, SDK, API - all use ARM
- Group Resource Handling
- Consistency
- Dependencies between resources
- Access control
- Tagging to logically organize resouces
- Billing by group by tag