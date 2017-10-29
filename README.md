

# JavaOne 2017

## Session

**Taking Java EE to the Clouds CON3419**

This session is a fast-paced tour of the many options available for running Java EE applications in
the cloud. It covers bare metal IaaS options such as AWS; PaaS options that provide native support
for Java EE, such as Oracle Java Cloud Service/BlueMix; and everything in between. It also discusses
how to deploy Dockerized Java EE applications to options such as Jelastic as well as running Java EE
applications by using fat-jar solutions such as WildFly Swarm on bare JVM-based platforms such as Heroku.
The presentation includes plenty of code examples and demos along the way.

Track:  Java, Cloud, and Server-Side Development
Experience Level:  Introductory

Speakers:

* Rodrigo Bortoloto, [CapTech](www.captechconsulting.com)
* Ryan Cuprak, [Dassault Systemes](https://www.3ds.com/)
* Reza Rahman, [CapTech](www.captechconsulting.com)

Links:
* [JavaOne](https://events.rainfocus.com/catalog/oracle/oow17/catalogjavaone17?search=Con3419)
* [Slideshare](https://www.slideshare.net/reza_rahman/taking-java-ee-to-the-clouds)
* [YouTube](https://youtu.be/9H1EZ0SwKBM)

## Java EE Application

The goal of the demos is to deploy the Cargo Tracker application using different packaging styles targeting multiple Cloud Providers at different service levels.

The application used is a fork of the [Cargo Tracker](http://cargotracker.java.net) JEE Application available in [this git repository](https://github.com/rstrazza/cargotracker)

The deployment artifacts were manually built by following one or more of the steps below:

### The ``war`` file

Options for obtaining the war file used across the examples:

1. Check out the [code](https://github.com/rstrazza/cargotracker) and run:
```bash
mvn clean package
```

2. OR, use the war file available [here](https://github.com/rstrazza/cargotracker-war)

### The ``Dockerfile`` file

Creating the docker image used across the examples:

1. Check out the [code](https://github.com/rstrazza/cargotracker) and run:
```bash
mvn clean package
```
2. Build the docker image:
```bash
cd src/docker
./build.sh
```
3. Run the docker image:
```bash
./run.sh
```

Alternatively, just pull the docker image directly from [Docker Hub](https://hub.docker.com/r/rstrazza/cargotracker-payara-server/):
```bash
docker pull rstrazza/cargotracker-payara-server
```

## Cloud Providers

### Amazon Web Services

* [IaaS using EC2 Instances](aws/ec2/README.md)
* [IaaS using Docker on EC2 Container Service](aws/ecs/README.md)
* [PaaS using ElasticBeanstalk](aws/elasticbeanstalk/README.md)

### Jelastic

* [Jelatic PaaS](jelastic/README.md)

### Microsoft Azure

[Java on Azure](https://azure.microsoft.com/en-us/develop/java/) provides support to Java applications at two levels:

* PaaS:
  * [Web Apps](https://azure.microsoft.com/en-us/services/app-service/web/) support Tomcat and Jetty
* IaaS:
  * Build everything. Similar approach demonstrated in the [AWS EC2 Instances](aws/ec2/README.md) example
  * Preconfigure Virtual Machines with Oracle WebLogic Server and IBM WebSphere Application

***Given the similarity with other platforms and lack of Java EE support, evaluate Azure at a later time.***

[Azure Container Service](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft.acs) would be an option for deploying Java EE applications packaged in a Docker container.

**Reference**

* [Azure for Java developers](https://docs.microsoft.com/en-us/java/azure/)
* [Configure web apps in Azure App Service](https://docs.microsoft.com/en-us/azure/app-service-web/web-sites-java-custom-upload)

### Google Cloud Platform

* [Research](gcp/README.md)

### Oracle Cloud

* [Research](oracle/README.md)

## References

**Cargo Tracker**
* [Git](https://j3e.github.io/cargo-tracker/)
* [Documentation](https://sknitelius.gitbooks.io/cargo-tracker/content/overview/overview.html)
* [Running in NetBeans with GlassFish](http://git.delabassee.com/ct/NetBeansHowTo.html)
* [Running with WebLogic](http://git.delabassee.com/ct/WlsHowTo.html)
