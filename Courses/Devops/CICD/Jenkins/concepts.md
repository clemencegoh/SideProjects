# Jenkins Introduction and Concepts
* Reminder: Besides conceptual knowledge, practical application is *very important*.

## How does Jenkins work?
* Needs to be installed on a server where central build takes place.
* Needs to be downloaded into the server
    * website: `https://jenkins.io/`
* Install after with: ```Java –jar Jenkins.war```
* **Usually** able to access through `localhost:8080` after installation and setup.
    * Jenkins can also be hosted on another port by going into the Jenkins folder and changing `Jenkins.xml`. After that restart the service. It will run on new port.
* Install Tomcat thereafter:
    * `http://tomcat.apache.org/`

## Why does Jenkins need Tomcat?
* Tomcat is an open source web server and servlet container developped by the Apache Software Foundation. Apache Tomcat is an Open Source Java web driven web application server. It provides support for Java web application like Jenkins
* Tomcat therefore acts as a wrapper to host Jenkins on `localhost:8080/jenkins` instead of directly on `localhost:8080`

## Alright, what do I do from here?
* Integration with preferred version control (github):
    * `Manage Plugins -> Available -> Git Plugin -> Install`
    * On restarting Jenkins, git will be available.

## Installing Maven
* Another new thing to install?
    * So far we have:
        * **Jenkins**: CI/CD tool
        * **Apache Tomcat**: Webserver hosting for java apps
        * **Maven**: Build tool 

## 

## TODO: Stopped here for tonight
* https://www.tutorialspoint.com/jenkins/jenkins_configuration.htm
