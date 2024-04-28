# Project-1: Multi Tier Web Application Setup Locally

This project provides resources to set up a multi-tier web application stack both manually and automatically. It's crucial to understand the manual process before automating it, as it helps in identifying potential issues and optimizing the process.

In this project, I have given all the resources to setup Multi Tier Web Application stack:
  1. Manually
  2. Automated

** Prerequisites
  - Oracle VM Virtual Box
  - Git bash
  - Vagrant
  - JDK 11 
  - Maven 3 
  - MySQL 8
  - Tomcat
  - MySQL
  - Memcached
  - Rabbitmq

*** Database - Here, we used Mysql DB 
  - /src/main/resources/db_backup.sql
  - db_backup.sql file is a mysql dump file. We have to import this dump to mysql db server
  - > mysql -u <user_name> -p<password> accounts < db_backup.sql

# Application Stack Architecture
![Architecture](images/Vprofile%20projectsetup%20Manual.png)
  - Tomcat: Serves as the web server to host the Java-based application.
  - MySQL: A relational database for storing user data securely.
  - Nginx: Acts as a load balancer to distribute traffic across multiple application instances.
  - Memcached: Provides caching capabilities for improved performance.
  - RabbitMQ: Used for queuing and messaging between various application components.
--------------------------------------------------
# Manual Setup
--------------------------------------------------
* Application stack setup
- The detailed setup steps are provided in the AppStackSetup.txt file located at vagrant/Manual_provisioning/AppStackSetup.txt. Follow the steps and execute them one by one to set up the application stack manually.


--------------------------------------------------
# Automated Setup
--------------------------------------------------

* VM SETUP
  1. Clone source code.
  2. cd into the repository.
  3. cd into vagrant/Automated_provisioning
  4. Bring up vm’s - $ vagrant up
  5. VALIDATION 
      - Login to web01 vm - $ vagrant ssh web01
      - Get the IP address - $ ip addr show
  6. copy the ip address and paste it in browser
  7. Login as admin_vp (username and password both) check the services
-----------------------------------------------

* Credits
- https://github.com/hkhcoder/vprofile-project
