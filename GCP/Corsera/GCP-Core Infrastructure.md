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
  - [Google Cloud SQL and Google Cloud Spanner](#Google-Cloud-SQL-and-Google-Cloud-Spanner)
  - [Cloud Spanner](#Cloud-Spanner)
  - [Comparing Storage Options](#Comparing-Storage-Options)
  - [Course Labs](#Course-Labs)
  - [questions](#questions)
-[Containers, Kubernetes, and Kubernetes Engine](#Containers,-Kubernetes,-and-Kubernetes-Engine)
  - [Container](#Container)
  - [question](#question)
  - [Introduction to Kubernetes and GKE](#Introduction-to-Kubernetes-and-GKE)
  - [Course Labs](#Course-Labs)
  - [questions](#questions)


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

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/5-%20Cloud%20storage/7-access-pattern.png)

### Google Cloud SQL and Google Cloud Spanner
* CloudSQL
  * Is managed RDBMS
  * Offers MySQL and PostgresSQLBeta database as service
  * use data base schema for data consistent
  * transactions, changes as all or nothing. Either they all get made, or none do.

* benefits of using the Cloud SQL
  * Automation replication (read, failover, and external replicas)
  * backup your data with either on-demand or scheduled backups
  * vertically by changing the machine type(read and write)
  * horizontally replicas(read)
  * data is encrypted(google security)

  * CloudSQL connections
  ![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/5-%20Cloud%20storage/8-cloudSQl-connections.png)

* horizontal scaleability, consider using Cloud Spanner. It offers transactional consistency at a global scale, schemas, SQL, and automatic synchronous replication for high availability.
  * outgrown any relational database,
  * sharding your databases for throughput high performance
  * transactional consistency
  * global data and strong consistency,
  * financial applications, and inventory applications.

* Questions
  * Which database service can scale to higher database sizes? Cloud Spanner.
  * Which database service presents a MySQL or PostgreSQL interface to clients? Cloud SQL.
  * Which database service offers transactional consistency at global scale? Cloud Spanner.

### Google Cloud Datastore
* Is a horizontally scalable NoSQL DB
* Designed for application backend
* store structured data from App Engine apps
* automatically handles sharding and replication
* Unlike Cloud Bigtable, it also offers transactions that affect multiple database rows, and it lets you do SQL-like queries. 
* free daily quota that provides storage, reads, writes, deletes and small operations at no charge

* Questions
  * How are Cloud Datastore and Cloud Bigtable alike
    * They are both highly scalable
    * They are both NoSQL databases.

* Cloud Datastore databases CAN span App Engine and Compute Engine applications. 

### Comparing Storage Options
* Technical detail 1
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/5-%20Cloud%20storage/9-compare1.png)
* Cloud Datastore actually stores structured objects.
* Technical detail 2
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/5-%20Cloud%20storage/10-compare2.png)

### Course Labs
---------------

### Deploy a web server VM instance
```commandline
Compute Engine > VM instances.
Create Instance.
Create an Instance Name: 	bloghost
Region and Zone:            ${Zone}
Machine type: 				default
Boot disk:  				Debian GNU/Linux 9 (stretch).
Identity and API access : 	defaults
Firewall: 					Allow HTTP traffic.

Networking, disks, security, management, sole tenancy -> Management
Startup script: 
apt-get update
apt-get install apache2 php php-mysql -y
service apache2 restart

Create.
 
Copy: bloghost VM instance's internal and external IP
```
### Create a Cloud Storage bucket using the gsutil command line
```commandline
Google Cloud Platform -> Activate Cloud Shell ->  Continue.
gcloud config set project qwiklabs-gcp-03-ca3c8283cc51
export LOCATION=ASIA
gsutil mb -l $LOCATION gs://$DEVSHELL_PROJECT_ID
gsutil cp gs://cloud-training/gcpfci/my-excellent-blog.png my-excellent-blog.png
gsutil cp my-excellent-blog.png gs://$DEVSHELL_PROJECT_ID/my-excellent-blog.png
gsutil acl ch -u allUsers:R gs://$DEVSHELL_PROJECT_ID/my-excellent-blog.png
```

### Create the Cloud SQL instance
````commandline
Navigation menu -> SQL -> Create instance.
Choose a database engine: 			MySQL.
Instance ID,						blog-db
Root password						simplesimple
Single zone							region and zone assigned by Qwiklabs.

Create Instance.

click on blog-db
Copy  Public IP address 
Users -> ADD USER ACCOUNT
User name : blogdbuser
Password	: simplesimple
ADD

Connections -> Add network.
choose Public IP
Name: web front end
Network: external IP address of your bloghost /32 , 35.192.208.2/32
Done 
Save 
````

### Configure an application in a Compute Engine instance to use Cloud SQL
```commandline
 Navigation menu -> Compute Engine > VM instances.
 SSH: bloghost.
 cd /var/www/html
 sudo vim index.php
 <html>
<head><title>Welcome to my excellent blog</title></head>
<body>
<h1>Welcome to my excellent blog</h1>
<?php
 $dbserver = "CLOUDSQLIP";
$dbuser = "blogdbuser";
$dbpassword = "DBPASSWORD";
// In a production blog, we would not store the MySQL
// password in the document root. Instead, we would store it in a
// configuration file elsewhere on the web server VM instance.
$conn = new mysqli($dbserver, $dbuser, $dbpassword);
if (mysqli_connect_error()) {
        echo ("Database connection failed: " . mysqli_connect_error());
} else {
        echo ("Database connection succeeded.");
}
?>
</body></html>

sudo service apache2 restart

35.192.208.2/index.php
Database connection failed: ...

sudo vim index.php
replace CLOUDSQLIP: Cloud SQL instance Public IP
DBPASSWORD with the Cloud SQL database password

sudo service apache2 restart

Database connection succeeded.
```

### Configure an application in a Compute Engine instance to use a Cloud Storage object
```commandline
Cloud Storage > Browser.
bucket that is named after your GCP project.
my-excellent-blog.png opy the URL behind
Public access
 
 Return to your ssh session on your bloghost
cd /var/www/html
sudo vim index.php
<img src='https://storage.googleapis.com/qwiklabs-gcp-0005e186fa559a09/my-excellent-blog.png'>

sudo service apache2 restart
```

### questions
*You are developing an application that transcodes large video files. Which storage option is the best choice for your application?
  * Cloud Storage

* You manufacture devices with sensors and need to stream huge amounts of data from these devices to a storage option
in the cloud. Which Google Cloud Platform storage option is the best choice for your application? 
  * Cloud Bigtable

* Which statement is true about objects in Cloud Storage?
  * They are immutable, and new versions overwrite old unless you turn on versioning.

* You are building a small application. If possible, you'd like this application's data storage to be at no additional charge. Which service has a free daily quota, separate from any free trials?
  * Cloud Datastore

* How do the Nearline and Coldline storage classes differ from Multi-regional and Regional? Choose all that are
  * Nearline and Coldline assess lower storage fees.
  * Nearline and Coldline assess additional retrieval fees.

* Your application needs a relational database, and it expects to talk to MySQL. Which storage option is the best choice  for your application?
  * Cloud SQL

* Your application needs to store data with strong transactional consistency, and you want seamless scaling up. Which storage option is the best choice for your application?
  * Cloud Spanner

* Which GCP storage service is often the ingestion point for data being moved into the cloud, and is frequently the long-term storage location for data?
  * Cloud Storage
  
## Containers, Kubernetes, and Kubernetes Engine
------------------------------------------------

* IaaS
  * Offering let you share compute resources with others by virtualizing the hardware.
  * Each Virtual Machine has its own instance of an operating system, your choice, and you can build and run applications on it with access to memory, file systems, networking interfaces, and the other attributes that physical computers also have

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/1-IaaS.png)

* PaaS (App Engine)
  * Instead of getting a blank Virtual Machine, you get access to a family of services that applications need. 

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/3-services.png)

* So all you do is write your code and self-contained workloads that use these services and include any dependent libraries. 

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/4-self-contained-workloads.png)

* As demand for your application increases, the platform scales your applications seamlessly and independently by workload and infrastructure.

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/5-scales.png)

###  Container

* give you the independent scalability of workloads like you get in a PaaS environment, and an abstraction layer of the operating system and hardware, like you get in an Infrastructure as a Service environment.
* What do you get as an invisible box around your code and its dependencies with limited access to its own partition of the file system and hardware?

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/6-container.png)

* You can treat the operating system and hardware as a black box. So you can move your code from development, to staging, to production, or from your laptop to the Cloud without changing or rebuilding anything. 

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/7-os.png)

* Kubernetes
  * In microservice infrastructure, you can make applications modular. They deploy it easily and scale independently across a group of hosts. The host can scale up and down, and start and stop Containers as demand for your application changes, or even as hosts fail and are replaced.
 
![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/8-microservice.png)

* A tool that helps you do this well is Kubernetes. Kubernetes makes it easy to orchestrate many Containers on many hosts. Scale them, roll out new versions of them, and even roll back to the old version if things go wrong.

![alt text](https://github.com/hojat-gazestani/Cloud/blob/main/GCP/Corsera/6-kubernetes/9-kubernetes.png)

* Cloud Build
  * a managed service for building Containers. 

### question
* false: each container has its own instance of an operating system.

* Containers are loosely coupled to their environments
  * Deploying a containerized application consumes less resources and is less error-prone than deploying an application in virtual machines. ￼
  * Containers abstract away unimportant details of their environments.
  * Containers package your application into equally sized components.

### Introduction to Kubernetes and GKE


* kubernetes
  * Kubernetes offers an API that lets people, that is authorized people, not just anybody, control its operation through several utilities. 

![alt text](1)

* cluster
  * It's a set of master components that control the system as a whole and a set of nodes that run containers.

![alt text](2)

* Google cloud kubernetes
  * Google Cloud provides Kubernetes Engine, which is Kubernetes as a managed service in the cloud. 

![alt text](3)

* pod
  * A pod is the smallest deployable unit in Kubernetes. Think of a pod as if it were a running process on your cluster. It could be one component of your application or even an entire application.

![alt text](4)

  * One way to run a container in a pod in Kubernetes is to use the kubectl run command.
  ![alt text](5)

```commandline
kubectl run nginx --image=nginx:1.15.7
```

To see the running nginx pods, run the command 
```commandline
kubectl get pods
```

To make the pods in your deployment publicly available, you can connect a load balancer to it by running the kubectl expose command.
```commandline
kubectl expose deployments nginx --port=80 --type=LoadBalancer
```


* Kubernetes then creates a service with a fixed IP address for your pods. 

![alt text](6)

* A service is the fundamental way Kubernetes represents load balancing. To be specific, you requested Kubernetes to attach an external load balancer with a public IP address to your service so that others outside the cluster can access it.

* Any client that hits that IP address will be routed to a pod behind the service.

![alt text](7)


* The kubectl get services command shows you your service's public IP address

![alt text](8)

* To scale a deployment, run the kubectl scale command.
```commandline
kubectl scale nginx --replica=3
```

* You could also use auto scaling with all kinds of useful parameters. For example, here's how to auto scale a deployment based on CPU usage
*  Kubernetes will scale up the number of pods when CPU usage hits 80% of capacity. 
```commandline
kubectl autoscale nginx --min=10 --max=15 --cpu=80
```

* Instead of issuing commands, you provide a configuration file that tells Kubernetes what you want your desired state to look like and Kubernetes figures out how to do it.
![alt text](9)

* After change, run the kubectl apply command to use the updated config file. 
```
kubectl apply -f nginx-deployment.yml
```

use the kubectl get replicasets command to view your replicas and see their updated state. 
```commandline
kubectl get replicasets
```

to watch the pods come online
```commandline
kubectl get pods
```

let's check the deployments to make sure the proper number of replicas are running 
```commandline
kubectl get deployments
```

The kubectl get services command confirms that the external IP of the service is unaffected.
```commandline
kubectl get services
```

### Introduction to Hybrid and Multi-Cloud Computing (Anthos)

* Anthos is a hybrid and multi-cloud solution powered by the latest innovations in distributed systems, and service management software from Google. The Anthos framework rests on Kubernetes and Google Kubernetes engine deployed on-prem. 
* Anthos also provides a rich set of tools for 
  * monitoring and 
  * maintaining the consistency of your applications across all of your network, 
  * whether on-premises, in the Cloud, or in multiple clouds. 

##  Course Labs

Confirm that needed APIs are enabled
------------------------------------
* Navigation menu -> APIs & Services
* Kubernetes Engine API
* Container Registry API


Start a Kubernetes Engine cluster
----------------------------------
```commandline
gcloud container clusters create webfrontend --zone us-central1-a --num-nodes 2
kubectl version

```
Compute Engine > VM Instances.


Run and deploy a container
--------------------------
```commandline
kubectl create deploy nginx --image=nginx:1.17.10
kubectl get pods

kubectl expose deployment nginx --port 80 --type LoadBalancer
kubectl get services
Open a new web browser tab and paste your cluster's external IP

kubectl scale deployment nginx --replicas 3
kubectl get pods
kubectl get services
```

### questions

* Identify two reasons for deploying applications using containers.
  * Consistency across development, testing, production environments
  * Simpler to migrate workloads

* True : Kubernetes allows you to manage container clusters in multiple cloud providers. 

* True : Google Cloud Platform provides a secure, high-speed container image storage service for use with Kubernetes Engine.

* In Kubernetes, what does "pod" refer to?
  * A group of containers that work together
  
* Does Google Cloud Platform offer its own tool for building containers (other than the ordinary docker command)? 
  *Yes; the GCP-provided tool is an option, but customers may choose not use it.

* Where do your Kubernetes Engine workloads run?
  * In clusters built from Compute Engine virtual machines