![2-secured_and_monitored_web_infrastructure](https://github.com/KamalCode98/alx-system_engineering-devops/assets/144700532/2d1056b1-fedd-46a3-9175-f901106643df)


Task 2: Distributed Web Infrastructure


Objective: Design a web infrastructure with three servers, a load balancer, and a database cluster that hosts the website www.foobar.com.


Components:

2 Servers: Additional servers to handle more traffic and provide redundancy.

Web Server (Nginx): Continues to serve web pages to users.

Application Server: Continues to run your application code.

Load Balancer (HAproxy): Distributes incoming traffic across the two servers to balance the load and provide high availability.

Set of Application Files (Your Code Base): The code base replicated across both servers.

Database (MySQL): A database cluster with a Primary-Replica setup for data redundancy and backup.

Explanation:

Why add more servers?: To handle more traffic and provide redundancy in case one server fails.

Why add a load balancer?: To distribute traffic evenly across the servers and ensure high availability.

Distribution algorithm of the load balancer: Common algorithms include round-robin (distributes requests evenly), least connections (sends new requests to the server with the fewest active connections), and IP hash (distributes requests based on the client's IP address).

Active-Active vs. Active-Passive load balancer: In an Active-Active setup, all servers are actively handling traffic. In an Active-Passive setup, one server is active while the other is on standby, ready to take over if the active server fails.

Database Primary-Replica cluster: The Primary node handles read and write operations, while the Replica node(s) only handle read operations and replicate data from the Primary. This provides data redundancy and backup.


Issues with this infrastructure:

Single Points of Failure (SPOFs): If the load balancer or the Primary database server goes down, the entire system can be affected.

Security: No firewalls or encryption mentioned, so the infrastructure could be vulnerable to attacks.

Monitoring: No monitoring system in place to track the health and performance of the servers and services.
