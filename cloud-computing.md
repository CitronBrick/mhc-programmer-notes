# Cloud Computing



## Open Stack

* set of software tools  for building & managing cloud computing platforms for public & private clouds
* managed by Open Stack Foundation

### OpenStack components

* **Nova** : 
	* primary computing engine. 
	* Deploy & manage VMs 
* **Swift** : 
	* storage system for files & objects
	* use unique id to refer to file
	* OpenStack manages actual location & decides where files are saved
	* Developer only refers the id
* **Cinder**
	* block storage component
	* traditional way of accessing disk locations
	* needed for high speed retrieval
* **Neutron**
	* provides networking capability
	* inter component communication
* **Horizon**
	* dashboard
	* GUI
* **Keystone**
	* identity services
	* existing user access methods can be used against Keystone
	* central list of users mapped against all services
* **Glance**
	* image services
* **Celiometer**
	* telemetry services
	* billing
* **Heat**
	* orchestration compoentn
	* developer stores requirements in a file with necessary resources of app.


## Elasticity

* ability of computing system to adjust its resources to match current & future demands
* system can increase resources during high demand
* system can decrease resources during low demand

### Horizontal Elasticity

* adding/removing instances (VMs, containers)

### Vertical Elasticity

* increasing/decreasing capacity of single resource
* upgrade CPU/memory/storage
* useful when
	* scaling out is impossible
	* app requires more powerful individual instances

### Temporal Elasticity

* scheduling based on predictable usage patterns

### Workload Elasticity

* adjust resources specifically for heavy batch jobs

### Rapid Elasticity

* quickly scale up/down resources to match real time demand
* requires complete automation & real-time monitoring

### Elasticity components

* Virtualization : VMWare, Hyper-V
* Automation & Orchestration tools : Docker, Kubernetes
* Real-time monitoring : Prometheus, Datadog monitor CPU & memory usage
* Load balancer : Nginx, HAProxy
* Resource management policies : AWS Autoscaling, Azure AutoScale, Google Cloud Autoscaler 
