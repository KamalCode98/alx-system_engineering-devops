
![0-simple_web_stack](https://github.com/KamalCode98/alx-system_engineering-devops/assets/144700532/5100155e-30ac-4e05-891b-28a7da911fd1)


Components:

Server: A physical or virtual machine that hosts the website and its related services.

Web Server (Nginx): Software that serves web pages to users. It handles HTTP requests and serves the requested pages.

Application Server: Software that runs your application code. It processes the business logic and interacts with the database.

Application Files (Your Code Base): The actual code of your website or web application.

Database (MySQL): The database that stores your website's data. It could be user data, content, etc.

Domain Name (foobar.com): The human-readable address of your website. It's mapped to the server's IP address (e.g., 8.8.8.8) through a DNS record.


Explanation:

What is a server?: A machine that provides services to other computers or devices, in this case, hosting a website.

What is the role of the domain name?: It's a human-readable address that users enter in their browser to access the website.

What type of DNS record is 'www' in www.foobar.com?: It's typically an 'A' record that maps the 'www' subdomain to the server's IP address.

What is the role of the web server?: It serves web pages to users. It receives HTTP requests and responds with the requested pages.

What is the role of the application server?: It runs the application code and handles the business logic. It interacts with the database to fetch or store data.

What is the role of the database?: It stores all the data related to the website, like user information, content, etc.

How does the server communicate with the user's computer?: Through the internet, using the HTTP/HTTPS protocol.


Issues with this infrastructure:

SPOF (Single Point of Failure): If the server goes down, the entire website becomes inaccessible.

Downtime during maintenance: If the server needs to be restarted or updated, the website will be down.

Scalability: If the website receives a lot of traffic, this single-server setup might not be able to handle the load.

