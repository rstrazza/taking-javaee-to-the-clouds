# JavaOne - DRAFT WORK IN PROGRESS

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
* [Slideshare?]() - TODO: ADD LINK

## Java EE Demo Application

**Cargo Tracker**

For additional information about the demo application, visit the Cargo Tracker [official page](http://cargotracker.java.net). The source code used for this demo was forked from [Cargo Tracker github](https://javaee.github.io/cargotracker/) and is available [here](https://github.com/rstrazza/cargotracker)

## Demos

The goal of the demos will be to deploy the Cargo Tracker application using different packaging styles targeting multiple Cloud Providers at different service levels.

The demos in this repo are organized by following folder structure:
&lt;platform&gt;-&lt;cloud-provider&gt;-&lt;service&gt;-&lt;deployment-type&gt;. Current demos:

* iaas-aws-ec2-war
* paas-aws-elasticbeanstalk-war
* iaas-aws-ecs-docker
* paas-jelastic-war
* paas-oraclecloud-war

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
