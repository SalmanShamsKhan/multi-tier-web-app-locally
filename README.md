![Project Architecture](vprofile%20projectsetup%20Automate.png)

**BOTH AUTOMATED AND MANUAL PROVISIONING- FOLLOW THE BASH SCRIPT FILES AND MANUAL**


Multi-Tier Application Setup using Bash Scripts
Project Overview
This project sets up a multi-tier application architecture locally using Bash scripts (.sh files) to automate the deployment of different components. The architecture follows a three-tier model, where each tier is responsible for a different function of the application.

This setup is ideal for DevOps engineers, system administrators, and developers who want to deploy a fully functional microservices-based web application using Nginx, Apache Tomcat, MySQL, Memcached, and RabbitMQ.

Architecture Breakdown
1️⃣ Load Balancer Tier (Nginx)
The Nginx load balancer distributes traffic among multiple application servers.
Ensures high availability and scalability of the application.
The nginx.sh script installs and configures Nginx to function as a reverse proxy.
2️⃣ Application Tier (Apache Tomcat)
The core of the application runs on Apache Tomcat, which serves the backend logic.
The tomcat.sh and tomcat_ubuntu.sh scripts automate the installation and configuration of Tomcat.
3️⃣ Caching Tier (Memcached)
Memcached speeds up response times by caching frequently accessed data.
The memcache.sh script installs and configures Memcached.
4️⃣ Database Tier (MySQL)
MySQL is the primary database for storing application data.
The mysql.sh script sets up MySQL with initial configurations.
5️⃣ Message Queue (RabbitMQ)
RabbitMQ is used as a message broker to enable asynchronous communication between different services.
The rabbitmq.sh script installs and configures RabbitMQ.
6️⃣ Backend Configuration
The backend.sh script configures backend dependencies, environment variables, and application settings.
application.properties contains necessary application configurations.
7️⃣ Infrastructure as Code (Vagrant)
Vagrant is used to create a virtualized environment for running the multi-tier application.
The Vagrantfile automates provisioning and manages VMs.


# Prerequisites
#
- JDK 17/21
- Maven 3.9
- MySQL 8

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- Tomcat
- MySQL
- Memcached
- Rabbitmq
- ElasticSearch
# Database
Here,we used Mysql DB 
sql dump file:
- /src/main/resources/db_backup.sql
- db_backup.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < db_backup.sql


