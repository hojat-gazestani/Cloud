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
  - [GCP Projects ](#GCP-Projects)
  - [IP Addresses](#IP-Addresses)
  - [Routes](#Routes)
  - [Firewalls ](#Firewalls)
  - [DNS Resolution](#DNS-Resolution)
  - [Network Billing](#Network-Billing)
- [Google Compute engine and networking](#Google-Compute-engine-and-networking )
- [Cloud storage integration](#Cloud-storage-integration)
  - [Google Cloud Bigtable](#Google-Cloud-Bigtable)



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

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/4-disks-images.png)

### Virtual Private Cloud (VPC) 
* global private isolated virtual network partition that provides managed networking functionality for your GCP resources. 

* global, spanning all regions. 

* The instances within the VPC have internal IP addresses and can communicate privately with each other across the globe. 

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/5-routing-vpc.png)

### GCP Projects 
* an organizational construct used for billing and permissions. 
* Used for apps or various environments like Prod/Test/Dev. 
* Finance/HR/Marketing. 
* some use it to provide billing to customers based on their usage within a cloud-hosted environment. 

* it’s simply a way to organize resources from a billing and permissions perspective, and each project has its own VPC network(s) isolated from other projects in GCP. 


![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/12-projects.png)

* VPC Networks and Subnets
  * VPC network is like VRF 

 

* GCP Project
  *VPC Network
    * Subnets 
    * Routes
    * Firewall
    * Internal DNS

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/6-gcp-networks.png)

* VPC network called default is global, while each of the subnets within it is regional. 

* Even though subnets are regional, instances can communicate with other instances in the same VPC network using their private IP addresses. 

* Of course, you can isolate these subnets within the network if you wish using firewall policies. 
 
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/7-gcp-subnet-zones.png)

* If you want complete isolation between various applications, customers, etc., you could create multiple networks.

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/8-multiple-networks.png)

* You can have up to five networks per project, including the default network. Multiple networks within a single project can provide multi-tenancy, IP overlap, or isolation within the project itself. Just another option instead of having multiple projects. 

### IP Addresses
Each VM instance in GCP will have an internal IP address and typically an external IP address.  The internal IP address is used to communicate between instances in the same VPC network, while the external IP address is used to communicate with instances in other networks or the Internet. These IP addresses are ephemeral by default but can be statically assigned. 

### Routes
* All networks have routes in order to communicate with each other

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/9-gcp-routes.png)

* Routes are considered a “network resource” and cannot be shared between projects or networks. 

* If an instance tag is used, the route applies to that instance, and if an instance tag is not used, then the route applies to all instances in that network. 

* Even though there are no “routers” in the software-defined network, you can still think of each VM instance as connected to some core router, with all traffic passing through it based on the perspective of each node’s individual route table.

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/10-gcp-route-tables.png)

### Firewalls 

* Each VPC network has its own distributed firewall, 

* If you have a concept in your mind that all this traffic is flowing through some single firewall chokepoint device somewhere, you’re mistaken. GCP is a full SDN, with firewall policies applied at the instance-level, no matter where it resides. These checks are performed immediately without having to funnel traffic through dedicated security appliances.

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/3-network-components/11-gcp-firewalls.png)

* Firewall rules can match IP addresses or ranges, but can also match tags.  Tags are user-defined strings that help organize firewall policies for standards-based policy approach. For example, you could have a tag called web-server, and have a firewall policy that says any VM with the tag web-server should have ports HTTP, HTTPS, and SSH opened. 

* Firewall rules are at the network resource level and are not shared between projects are other networks. 

### DNS Resolution 

* DNS entries are automatically created resolving to a formatted hostname. 

* FQDN = <pre>[hostname].c.[project-id].internal</pre> 

* So, if I had an instance named “porcupine” in my project called “tree”, my DNS FQDN would be: 

* porcupine.c.tree.internal 

* Resolution of this name is handled by an internal metadata server that acts as a DNS resolver (169.254.169.254), provided as a part of Google Compute Engine (GCE). This resolver will answer both internal queries and external DNS queries using Google’s public DNS servers. 

* If an instance or service needs to be accessed publicly by FQDN, a public-facing DNS record will need to exist pointing to the external IP address of the instance or service. This can be done by publishing public DNS records. You have the option of using some external DNS service outside of GCP or using Google Cloud DNS. 

### Network Billing 

* GCP bills clients for egress traffic only.  Egress traffic is considered as traffic to the Internet, or from one region to another (in the same network), or between zones within a region. 

* You are not billed for ingress traffic. Ingress traffic includes VM-to-VM traffic in a single zone (same region, network), and traffic to most GCP services. 

* Some notes on caveats/limitations 
  * VPC networks only support IPv4 unicast traffic (No IPv6, or broadcast/multicast) 
  * Maximum of 7000 VM instances per VPC network 

## Google Compute engine and networking 

* For which of these interconnect options is a Service Level Agreement available 

* Google Cloud Load Balancing allows you to balance HTTP-based traffic across multiple Compute Engine regions. 

* Networks are global; subnets are regional 

* Local SSD is used for an application running in a Compute Engine virtual machine needs high-performance scratch space.  

* Choose an application that would be suitable for running in a Preemptible VM. 

* A batch job that can be checkpointed and restarted 

* Use big VMs for in-memory databases and CPU-intensive analytics; use many VMs for fault tolerance and elasticity 

* VPC routers and firewalls, They are managed by Google as a built-in feature. 

* A GCP customer wants to load-balance traffic among the back-end VMs that form part of a multi-tier application. Which load-balancing option should this customer choose? 

* The regional internal load balancer 

* For which of these interconnect options is a Service Level Agreement available? 

* Dedicated Interconnect 

## Cloud storage integration  

Ways to getting data into your cloud: 

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/5-%20Cloud%20storage/0-cloud-storage.png)

### Google Cloud Bigtable
* Is a big data database service

* relational database schema:
  * tables in which every row has the same set of columns,
  * and the database engine enforces that rule and other rules you specify for each table
  * 
* NoSQL
  * not all the rows might need to have the same columns
  * the database might be designed to take advantage of that by sparsely populating the rows.
  * Which brings us to Bigtable
  * It's ideal for data that has a single lookup key
  * persistent hash table.
  * Cloud Bigtable is ideal for storing large amounts of data with very low latency.
  * It supports high throughput, both read and write, so it's a great for operational, analytical(IoT,user analytics and financial data analysis.)
* Bigtable
  * scalability
  * administration tasks like upgrades and restarts transparently
  * encrypted data in both in-flight and at rest.
  * major application including  search, analytics, maps and Gmail

* Can interact with other GCP services

![alt text](# 7)
