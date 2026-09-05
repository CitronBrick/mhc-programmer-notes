# Virtualization & Cloud Computing

Helps create single hardware system -> multiple simulated environments.

## Virtualization benefits

* Better hardware utilization
* Reduced infra costs
* Easy scalability & flexibiltiy
* Improved isolation & security
* Faster server deployment
* Foundation for AWS EC2, Azure VM & Google Compute Engine

## Architecture

* Physical Hardware (**Host**) : actual server containing CPU, RAM & network resources
* **Hypervisor** : software creating & managing VMs by allocating hardware resources
* Virtual Machine (**Guest**) : software based computer running its own OS, applications & libraries independantly of other VMs.

## Hypervisor types

### Type 1 : Bare-Metal hypervisor

* installed directly on physical hardware. No host OS
* High Performance due to direct hardware access
* Enterprise Data Centers, Cloud Providers (AWS EC2, VMWare)

### Type 2 : Hosted Hypervisor

* installed as an application on top of an existing OS
* Lower performance as requests must pass via Host OS first
* Personal Use, testing labs (Oracle VirtualBox, VMWare Workstation)

## Virtualization types

* Application Virtualization
* Network Virtualization
* Desktop Virtualization
* Storage Virtualization
* Server Virtualization
* Data Virtualization

### Application Virtualization

* apps run independantly of underlying OS
* apps run on remote server
* no local installation
* access allowed to apps from multiple devices
* Use cases:
	* Citrix Apps / Microsoft App-V
	* BYOD environments

### Network Virtualization

* separates network services (routing, switching, firewall management) from physical network hardware.
* managed & configured via Software Defined Network (SDN)
* Use cases
	* AWS VPC helps creating virtual network, subnet, route table & security group

### Desktop Virtualization

* hosts user's desktop environment  on centralized server instead of local computer
* users access desktop via thin clients
* Use cases
	* AWS Workspaces

### Storage Virtualization

* combines physical storage resources from multiple devices into a single centrally managed virtual storage pool
* use cases
	* Storage Area Network (SAN) or AWS S3


### Server Virtualization

* divide single physical server into multiple virtual servers (VMs)
* each VM operates *independantly* with its own OS, apps & resources
* Use cases
	* Using VMWare vSphere, Linux web server, Windows DB server & Linux mail server can be run on the same physical machine

### Data Virtualization

* technology that creates abstract layer between users & data sources, allowing data from multiple systems to be accesses *as if it were* from single location. 
* The data remains in original source & is not physically copied.
* Use cases
	* Using Denodo or Oracle Data Service, sales data can be retrieved from both SQL database & Cloud data lake presenting *as if it were* a single dataset

## 5 levels of Virtualization

1. Instruction Set Architecture (ISA) = BIRD/Dynamo
2. Hardware Abstraction Layer (HAL) = VMWare / Virtual PC
3. Operating System Level = Virtual Environment / FVM
4. Library Level = WINE / vCUDA
5. Application Level = JVM / .NET CLR

### Instruction Set Architecture Level

* Virtualization runs through an ISA emulation
* helpful to run inherited code for different hardware configurations
* code can be run on VM via an ISA
* basic emulation requires an *Interpreter*.

### Hardware Abstraction Level

* Virtualization at hardware level
* Uses Bare Hypervisor
* Virtualization of hardware eg: IO devices, processors, memory etc.

### OS Level

* the Virtualization model creates an abstract layer between the apps & OS.
* isolated container on physical server & OS. 
* each container functions as OS
* when there are too many stingy users, OS level Virtualization is useful

### Library level

* OS system calls are lengthy & bulky
* Apps opt for user library APIs
* User library APIs control communication link

### Application level aka Process level

* virtualize only application (not enviroment or platform)
* useful when running VM with high level languages



