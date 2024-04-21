![1-distributed_web_infrastructure](https://github.com/KamalCode98/alx-system_engineering-devops/assets/144700532/e9d8b2d1-c525-48f6-8b5e-0152efddc1c5)



Task 2: Distributed Web Infrastructure


Objective: Expand the infrastructure to include three servers, a load balancer, and a database cluster.

Components:


2 Servers: Additional servers to handle more traffic and provide redundancy.

Web Server (Nginx): Same as before, but now you have it on multiple servers.

Application Server: Same as before, running on multiple servers.

Load Balancer (HAproxy): A device or software that distributes incoming traffic across multiple servers.

Application Files (Your Code Base): Same as before, but now replicated across servers.

Database (MySQL): Now set up in a Primary-Replica configuration for redundancy and scalability.


Explanation:

Why add more servers?: To handle more traffic and provide redundancy in case one server fails.

Why add a load balancer?: To distribute incoming traffic across multiple servers, ensuring no single server gets overloaded.

What distribution algorithm is used?: Common algorithms include round-robin, least connections, and IP hash. The choice depends on the specific requirements of the application.

Active-Active vs. Active-Passive: In an Active-Active setup, all servers are actively handling traffic. In an Active-Passive setup, one server is active while the others are on standby, ready to take over if the active server fails.

Primary-Replica Database Cluster: The primary node handles writes, while the replica nodes handle reads. This setup improves read performance and provides redundancy.


Issues with this infrastructure:

SPOF: If the load balancer fails, the entire website becomes inaccessible.

Security: No firewalls or encryption (HTTPS) are mentioned, which could expose the website to attacks.

Monitoring: Without monitoring, it's hard to detect and respond to issues in the infrastructure.
