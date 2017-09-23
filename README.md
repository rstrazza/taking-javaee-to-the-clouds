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

* Rodrigo Bortoloto, CapTech
* Ryan Cuprak, Dassault Systemes
* Reza Rahman, CapTech

Links:
* [JavaOne](https://events.rainfocus.com/catalog/oracle/oow17/catalogjavaone17?search=Con3419)
* [Slideshare: COMMING SOON]()

## Java EE Application

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

### IBM BlueMix

*TODO*

### Jelastic

Example using [Jelatic PaaS](jelastic/README.md) for Java applications.

### Heroku

*TODO*

### Microsoft Azure

[Java on Azure](https://azure.microsoft.com/en-us/develop/java/) provides support to Java applications at two levels:
1. PaaS: Web Apps only supports Tomcat and Jetty. For a full list, check

[Upload a custom Java web app to Azure](https://docs.microsoft.com/en-us/azure/app-service-web/web-sites-java-custom-upload)

2. IaaS: By leveraging pre configure Virtual Machines with Oracle WebLogic Server and IBM WebSphere Application.

### Oracle Cloud

TODO

## Demos

The goal of the demos is to deploy the Cargo Tracker application using different packaging styles targeting multiple Cloud Providers at different service levels.

The demos in this repo are organized by cloud provider followed by their specific service.

---

TODO: guide on how to build war / docker artifacts

== Jelastic ==
USE: https://github.com/m-reza-rahman/pragmatic-microservices-lab/blob/master/complex-concepts/cargo-tracker/src/docker/Dockerfile

### War Deployments

* AWS IaaS using Glassfish

    Fully automated provisioning of AWS resources via CloudFormation

* Oracle Java Cloud Services PaaS using Glassfish

    TODO: check Glassfish support / likely Weblogic?
    - http://git.delabassee.com/ct/WlsHowTo.html

* IBM BlueMix PaaS using Glassfish

    TODO: check Glassfish support / likely Websphere?

### Fat-Jar Deployments

* WildFly Swarm on bare JVM-based platforms such as Heroku
* ? Google Cloud Engine ?
* ? AWS ElasticBeanstalk ?

PURE JVM - PAYARA MICRO -> Heroku / GCE

### Docker Deployments - they already have the docker image/file?

https://github.com/m-reza-rahman/pragmatic-microservices-lab/tree/master/complex-concepts

Presentation considerations:
* Monitoring
* Clustering

Mental model:
* Use Jelastic for the docker demo
* Oracle Cloud - 30 day trial
* Explore Azure - Weblogic
* Explore BlueMix and/or OpenShift
* Heroku
* GCE

Likely demo sequence:
1 - AWS IaaS
2 - Jelastic
3 - PaaS - Oracle Cloud
4 - Heroku
