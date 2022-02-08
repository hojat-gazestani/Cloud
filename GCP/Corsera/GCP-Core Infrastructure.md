Google Cloud Fundamentals: Core Infrastructure - Note
=====================================================
- [intro](#intro)
  - [GCP services](#GCP-services)
  - [cloud computing](#cloud-computing)
  - [fundamental characteristic of devices](#fundamental-characteristic-of-devices )
  - [PaaS](#PaaS)
  - [IaaS](#IaaS)
  - [qus](#qus)
- [resource hairarchy](#resource-hairarchy)
  - [todo](#todo)
- [Networking Fundamentals](#Networking-Fundamentals)
  - [compnents](#compnents)
  - [resources](#resources)
  - [Regions and Zones](#Regions-and-Zones)
  - [Virtual Private Cloud (VPC)](#Virtual-Private-Cloud-(VPC))



### GCP services
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/1-%20GCP%20resource%20hairearchy/1-services.png)

* Compute
  * Cupute engine
  * Kubernetes engine
  * App engine 
  * App engine 
  * Cloud foundation

* Storage 
  * Bigtable 
  * Cloud Storage 
  * Cloud SQL 
  * Cloud Spanner 
  * Cloud Datastore 

* Big Data 
  * Big Query 
  * Pub/Sub 
  * Data flow 
  * Data proc
  * Data lab

* Machine Learning 
  * Natural Language API 
  * Machine Learning 
  * Speech API 
  * Translate API 

### cloud computing
- Customers can scale their resource use up and down 
- Computing resources available on-demand and self-service 
- Customers pay only for what they use or reserve 
- Resources are available from anywhere over the network 

- Providers are NOT dedicating physical resources to each customer 

### fundamental characteristic of devices 
* Choose a fundamental characteristic of devices in a virtualized data center. 
* They are manageable separately from the underlying hardware. 

### PaaS
* Platform as a Service 
* let you bind your application code to libraries that give access to the infrastructure your application needs 

### IaaS
* Infrastructure as a Service
* provides raw compute, storage, and network, organized in ways that are familiar from physical data centers 

### qus
* qus1
  * What kind of customer benefits most from billing by the second for cloud resources such as virtual machines?
    * Customers who create and run many virtual machines 

* qus2
  * Services and APIs are enabled on a per project basis.

* qus3
  * Choose a fundamental characteristic of devices in a virtualized data center.
    * They are manageable separately from the underlying hardware. 
    * They use less resources than devices in a physical data center. 
    * They are more secure. 
    * They are available from anywhere on the Internet.

## resource hairarchy
### todo
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/1-%20GCP%20resource%20hairearchy/2-%20hierarchy.png)

* When would you choose to have an organization node?
  * When you want to apply organization-wide policies centrally. 
  * When you want to create folders 

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/1-%20GCP%20resource%20hairearchy/3-%20project%20attributes.png)

* Order these IAM role types from broadest to finest-grained.* 
  * Primitive roles, predefined roles, custom roles 

* Can NOT IAM policies that are implemented higher in the resource hierarchy take away access that is granted by lower-level policies

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/1-%20GCP%20resource%20hairearchy/4-%20folder.png)


![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/1-%20GCP%20resource%20hairearchy/5-iam%20hairarchy.png)


* When would you choose to have an organization node?  
  * 
  * When you want to apply organization-wide policies centrally. 
  * When you want to organize resources into projects. 

* Order these IAM role types from broadest to finest-grained. 
  * Primitive roles, predefined roles, custom roles 

* Can NOT IAM policies that are implemented higher in the resource hierarchy take away access that is granted by lower-level policies 

## Networking Fundamentals
### compnents
 
* Network components
  * VPCs 
  * Projects 
  * Networks 
  * Regions 
  * Zones 
  * Subnets 
  * Switching 
  * Routing 
  * Firewalls
  
* Essentially, we’ll be going over this diagram: 
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/1-diagram.png)

* GCP has 11 regions, 33 zones and over 100 points of presence throughout the globe. 
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/2-regions-zones.png)

### Regions and Zones
* When building an application for high availability and fault tolerance, it’s crucial to distribute your resources across multiple zones and regions. 


* Zones are independent of each other, with completely separate physical infrastructure, networking, and isolated control planes that ensure typical failure events only affect that zone. 


* Another design consideration is speed and latency.  Zones have high-bandwidth, low-latency connections to other zones in the same region. 


* A region is a specific geographical location that is sub-divided into zones. 
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/2-regions-zones.png)

* regions: 
  * To bring their applications closer to users around the world, and for improved fault tolerance


### resources
* Global Resources: 
  * 
  * Images 
  * Snapshots 
  * VPC Network 
  * Firewalls 
  * Routes 

* Regional Resources:
  * Static external IP addresses
  * Subnets 

* Zonal Resources:
  * Instances (VMs)
  * Persistent Disks

![alt text](#https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/4-disks-images.png)

### Virtual Private Cloud (VPC) 
* global private isolated virtual network partition that provides managed networking functionality for your GCP resources. 

* global, spanning all regions. 

* The instances within the VPC have internal IP addresses and can communicate privately with each other across the globe. 

![alt text](#https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/5-routing-vpc.png)

