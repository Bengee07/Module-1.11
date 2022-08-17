## Brief

### Preparation

None.

### Lesson Overview

The terms scalability and high availability have never been more popular due to the rising requirement for dependable and effective infrastructures built to support important systems. Reducing downtime and removing single points of failure are equally crucial, even if managing increased system load is a regular worry. Scalable infrastructure designs that prioritize high availability take these latter factors into account.

This lesson will explore what exactly high availability means and how it can improve the infrastructure’s reliability.

---

## Part 1 - High Availability

![image](https://user-images.githubusercontent.com/106639884/185000669-9673d506-b2e2-47e0-bf84-ef2411e02e3c.png)


The term "availability" in computing refers to both the amount of time that a service is accessible and the amount of time it takes for a system to react to a user's request. High availability refers to a property of a system or component that guarantees a high level of operational performance for a specific amount of time.

An availability value of 100% would mean that the system never fails. Availability is frequently expressed as a percentage indicating how much uptime is expected from a specific system or component in a given period of time. For instance, a system that promises 99% uptime over the course of a year may have up to 3.65 days of outage (1%).

These figures are determined by a number of variables, such as planned and unforeseen maintenance intervals, as well as the amount of time needed to recover from a potential system failure.

**Why Is High Availability Important?**

Whatever the cause, downtimes can have negative impact on the health of your company, including missed productivity, lost business opportunities, lost data, and impaired brand reputation. As a result, IT staff continuously work to implement appropriate methods to reduce downtime and guarantee continual system availability.

As a result, the expenditures related to downtime might cause anything from a little budget imbalance to a significant hole in your wallet. High availability is necessary for a number of reasons, but one of them is to prevent downtime. Several additional factors include:


**1. Maintaining SLAs**

For MSPs (Managed Service Providers) to guarantee the delivery of high-quality services to their clients, maintaining uptime is a crucial requirement. High-availability systems enable MSPs to consistently meet their SLAs (Service Level Agreements) and guarantee that their clients' networks don't go down.

**2. Improve Customer Relations**

Customers that experience frequent business interruptions due to outages may get dissatisfied. High-availability environments minimize the possibility of future downtime and can assist MSPs in establishing enduring connections with clients by ensuring their satisfaction.


**3. Establish Company Reputation**

System availability is a crucial sign of how well services are delivered. Because of this, MSPs can use high-availability environments to preserve system uptime and establish a solid brand identity in the marketplace.

**4. Improve Data Security**

Having high availability can considerably lower the likelihood that crucial business data will be improperly accessed or stolen by decreasing the occurrence of system downtimes.

---

## Part 2 - What System Components Are Required for High Availability?

For the actual implementation of high availability, a number of factors need to be properly taken into account. High availability depends on elements other than just software implementation, including:

**Environment**: If all the servers are located in the same geographical area, an event such as an earthquake or flooding could take the whole system down. Having redundant servers in different datacenters and geographical areas will increase reliability.


**Hardware**: Highly available servers should be resilient to power outages and hardware failures, including hard disks and network interfaces.


**Software**: The whole software stack, including the operating system and the application itself, must be prepared for handling unexpected failure that could potentially require a system restart.


**Data**: Data loss and inconsistency can be caused by several factors, and it’s not restricted to hard disk failures. Highly available systems must account for data safety in the event of a failure.


**Network**: Unplanned network outages represent a possible point of failure for highly available systems. It is then important that a redundant network strategy is in place for possible failures.

---

## Part 3 - Availability Measures

Even while three nines, or 99.9%, is typically thought to be a respectable uptime, it still equates to 8 hours and 45 minutes of downtime annually. Let's look at the table showing how the different availability levels translate into downtime hours.

![image](https://user-images.githubusercontent.com/106639884/185001295-3564f063-572a-4dbf-bda4-62ac704a1bda.png)


**TO-DO: Lets Calculate The Downtime per month and The Downtime per week**


## Part 4 - How can HA be achieved?

A system cannot become more stable or attain high availability by adding additional components. In fact, it might have the reverse effect because adding more components can make failures more likely. Modern designs enable the distribution of workloads across numerous instances, such as a network or a cluster, which aids in **load balancing**. Load balancing is an approach to resource management that maximizes output, reduces reaction times, and avoids overloading any system. Failover systems, which include switching to a backup server, component, or network when a current one fails, is also another aspect of this process.

![image](https://user-images.githubusercontent.com/106639884/184999887-c0400ea2-0b92-42f5-80d0-f73d472229ce.png)


1. Use of Multiple Application Servers

Imagine that there is only a single server to provide the services, but then a sudden increase in demand causes it to fail (or crashes it). This results in a downtime because no new requests can be served until your server is restarted.

Deploying the application across numerous servers is the logical approach in this case. To ensure that no single server is overloaded and the production is at its best, the load must be balanced among all the servers. Parts of the application can also be deployed on various servers. For instance, there could be a separate server for processing static assets like photos or one for managing email (like a Content Delivery Network).


2. Scaling Databases

The most common and conceptually straightforward method of storing user data is though the use of databases. Databases are just as crucial to services as application servers, it is necessary to keep in mind. Databases operate on different servers and are also prone to failure. What's worse is that database crashes may result in user data loss, which may be expensive.

Redundancy is a process that achieves failure detectability and prevents common cause failures to provide systems with high levels of availability. Maintaining slave servers that can take over in the event that the primary server fails can help with this. Sharding is a fascinating idea for scaling databases. A shard is a horizontal database division where rows from the same table are run on different servers.

3. Diversified Geographical Locations

It's a huge step forward to scale up applications and databases, but what happens if all of the servers are housed in the same data center and an event like a natural disaster damages the data center where the servers are kept? This may result in lengthy downtimes.

Servers must be then spread out in different places. Choose the appropriate physical locations of the servers with the majority of contemporary web services by making intelligent decisions to ensure that the servers are spread out globally rather than localized in one place.


## Part 5 - Best Practices For High Availability

It is strongly advised, especially for mission-critical applications, to employ a High Availability (HA) design to reduce system failures and prevent both planned and unplanned downtimes. Experts in availability maintain that well-designed and thoroughly tested components are essential for any system to be highly available. A high availability architecture's design and subsequent implementation can be challenging given the numerous software, hardware, and deployment alternatives available. But a successful endeavor often begins with well defined and thoroughly comprehended business requirements. The architecture of choice must be capable of providing the appropriate levels of security, scalability, performance, and availability.

Compute environments must be designed with high availability if a desired level of operational continuity is to be ensured during production hours. Enterprises can maintain critical applications online in addition to properly building the architecture by adhering to the best practices for high availability.


![image](https://user-images.githubusercontent.com/106639884/184999839-d0590e24-da77-4006-a25f-c92cd8644eaf.png)


**1. Data Backups, Recovery and Replication**

A solid backup and recovery plan is the defining characteristic of a successful data security strategy that guards against system failure. Never save valuable data without adequate backups, replication, or the capacity to recreate the data. Every data center should make early preparations for data loss or corruption. Data inaccuracies may affect financial accounts, customer authentication, and ultimately the legitimacy of the corporate community. Making a complete backup of the primary database and then incrementally checking the source server for data corruptions is the suggested method for ensuring data integrity. The first step in recovering from a catastrophic system loss is to create comprehensive backups.

**2. Clustering**

Each and every application service will eventually fail, even with the best software engineering. The goal of high availability is to deliver application services notwithstanding errors. In the event of a problem, clustering can offer immediate failover application services. When a server goes down, a "cluster aware" application service can fall back to a backup server and still call resources from several servers. Multiple nodes that communicate information over shared data memory grids make up a high availability cluster. This means that as long as at least one node in the cluster is completely functional, any node can be unplugged from the network or shut down, and the cluster as a whole will continue to function normally.


**3. Network Load Balancing**

Critical web-based applications can be made more available by using load balancing. When instances of a server fail, the traffic is immediately transferred to servers that are still up and running, replacing the failed instances seamlessly. Load balancing not only promotes high availability but also progressive scalability. Either a "pull" or a "push" model can be used to balance network load. Higher levels of fault tolerance are made possible inside service applications. While the cluster is running, each node can be upgraded individually and rejoined. By establishing a virtualized cluster that makes use of the available hardware resources, the high cost of buying additional hardware to build a cluster can be reduced.


**4. Fail Over Solutions**

Traditionally, a high availability architecture consists of a collection of loosely coupled servers with failover features. In a nutshell, failover is a backup operational mode where a secondary system takes over a primary system's functions in the event that the original one goes down due to failure or planned downtime. When the backup server is only launched after the first one has been entirely shut down, this is known as a "cold failover." When all the servers are active at the same time and just one server is handling the whole load, this is known as a "hot failover." Tasks are automatically transferred from one scenario to the other to keep the end user's experience as fluid as possible. In a controlled setting, DNS can be used to manage failover.

**5. Geographic redundancy**

When it comes to preventing service failure in the face of catastrophic occurrences like natural disasters that cause system outages, geo-redundancy is the only line of defense. Multiple servers are installed at geographically distant places, just like in the case of geo-replication. The places ought to be dispersed internationally rather of being localized in one place. Running distinct application stacks in each site is essential so that if one location fails, the other can still function. These places ought to be totally independent of one another.


**6. Plan for failure**

There are further steps a company can take to improve its preparedness in the case of a system breakdown that causes downtime, despite the fact that using the best practices for high availability is essentially planning for failure. Data on resource usage or failure that can be utilized to identify issues and spot trends should be retained by organizations. Only by continuously monitoring operational workload can this data be gathered. To gather problem data, build problem history, and start right away solving problems, a recovery help desk can be set up. A recovery plan should be thoroughly written and periodically evaluated to guarantee that it will work when confronted with unforeseen interruptions. Staff training on availability engineering will improve their skills in designing, deploying, and maintaining high availability architectures. Security policies should also be put in place to curb incidences of system outages due to security breaches.


## Part 5 - Use Case on How To Achieve HA


You and your group will have further discussion on how to implement HA for different use cases:

- eCommerce
- Financial Institution
- Government
- Personal Static Website
- eHailing Application
