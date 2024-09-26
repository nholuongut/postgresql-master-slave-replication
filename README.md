[Kubernetes Practice - Setup a database master-slave replication with PostgreSQL]
Introduction
Hello everyone, welcome to the practice series on kubernetes. In this article, we will learn about how to deploy a database system in master-slave replication mode on kubernetes.

Before talking about how to deploy the database system, let's talk about what a master-slave replication database is and why we need it?

Database Master-Slave Replication
This is a database system that includes a master DB, and many slave replication DBs. The master is used for writing data, and the replication DBs will be used for reading data. Data written to the master DB will be transferred to the replication DBs so that the data on our entire database system is synchronized with each other.

In an application, we usually only use one DB for both reading and writing. If the application is just a normal web application and has low traffic, using such a DB is enough to meet the requirements. But for applications with high traffic, using only one DB for both reading and writing will cause our application to not be able to meet all user accesses or our application will have very poor performance. Therefore, this master-slave replication DB system will help us increase the processing performance of the application a lot, by separating the data writing to be written to a DB called master, and when reading data, we will read from the DB read replicas => increase the performance and processing speed of the application.

### [Contact an Author]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com) 

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)
