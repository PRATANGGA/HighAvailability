# High Availability

## What is High Availability?

High Availability (HA) refers to systems that are designed to be operational and accessible for a high percentage of time, minimizing downtime and ensuring continuous service availability. This is often achieved through redundancy, failover mechanisms, and load balancing.

## Key Components in this setup

- **Apache** (Web Server)
  Acts as the backend server that processes HTTP requests and serves web content. In this setup, multiple Apache web servers are used to serve the same content, ensuring that if one server fails, another can continue serving users without disruption.
- **Nginx** (Load Balancer)  
   Sits in front of the web servers and distributes incoming client requests across multiple backend Apache servers. This helps balance the load, prevent any single server from being overwhelmed, and improves the responsiveness of the web service
- **Keepalived** (Failover Management)
  Works together with Nginx to provide fault tolerance. It manages a Virtual IP Address (VIP) that floats between two Nginx instances (Master and Backup). If the master load balancer fails, Keepalived promotes the backup node to master and assigns the VIP to it, ensuring uninterrupted access for users.

## What Will Be Done in This Module?

In this module, we will implement a High Availability Web Server Architecture that ensures reliable and uninterrupted web service delivery through the combination of load balancing, redundancy, and failover mechanisms.

### Network Topology

![Topology](./topologi.jpg)
