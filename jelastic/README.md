# Java EE on PaaS: Jelastic Java

Java EE is a first class citizen in the Jelastic PaaS environment. The
first service released late 2011 was for the Java EE platform.

This demo is using Jelastic Stark v.5.2 to deploy the Java EE Cargo Tracker
application on GlassFish 4.1.2.

The platform currently supports multiple Application Servers, Web Servers and Servlet Containers such as [GlassFish](https://javaee.github.io/glassfish/),
[JBoss](https://developers.redhat.com/products/eap/overview/), [Jetty](http://www.eclipse.org/jetty/), [Tomcat](http://tomcat.apache.org/), [TomEE](http://tomee.apache.org/apache-tomee.html) and [Wildfly](http://wildfly.org/). For the full list check the [Jelastic documentation](https://docs.jelastic.com/setting-up-environment#app-serv).

Create a free trial Jelastic account. No credit card required.

## Provisioning GlassFish Server

After login, click on ``NEW ENVIRONMENT``. That will open a window with JAVA and
Tomcat as the selected options by default. Click on the Tomcat logo to expand the server options and Select GlassFish 4.1.2 as shown below:

![alt text](img/single-node-create-env-select-gf.png)

For this example, a single node of GlassFish will suffice. Define the vertical scaling configuration per node by selecting how much RAM and CPU will be *reserved* to each node. That is the computing capacity allocated and available at all times to the infrastructure (container) where the GlassFish server will be running. Still, as part of the vertical scaling configuration, define the *scaling limit* capacity that the server can grow to if the need arrives. For example, during peak times an application might require more memory to handle the load.

This configuration is based on Jelastic [Cloudlets](https://docs.jelastic.com/cloudlet). It is important to understand how it works and the billing model to avoid undesired billing surprises. The platform does a good job estimating the new environment initial cost as well as to how much it can grow based on scaling events.

On the right-hand side, enter the Environment Name or leave the default. Click Create.

![alt text](img/single-node-create-env-topology.png)

After a few minutes the new environment Status will be *Running* and the GlassFish server will be ready to use.

![alt text](img/single-node-env-running.png)

## Deploying the Cargo Tracker application

Jelastic has several options for deploying java applications, including building
directly. In this case, upload the

### Upload the war file to Jelastic

![alt text](img/upload-app-click-upload.png)

![alt text](img/upload-app-select-file.png)

![alt text](img/upload-app-done.png)

http://javaone.pb-us.jelastic.com/cargo-tracker



## References:

* [What is Jelastic PaaS & CaaS?](https://docs.jelastic.com/what-is-paas-and-caas)
* [How to Create your Jelastic Environment](https://docs.jelastic.com/setting-up-environment)

* [Endpoints: A Direct Connection to the Cloud](http://ops-docs.jelastic.com/endpoints)

* [How to Deploy Projects to Jelastic Cloud](https://docs.jelastic.com/deployment-guide)
* [What is a Cloudlet?](https://docs.jelastic.com/cloudlet)
* [Jelastic Usage-Based Pricing](https://docs.jelastic.com/pricing-model)

* [Marketplace](https://jelastic.com/marketplace/apps/)

* [How to Configure GlassFish Cluster with Automatic Load Balancing](https://blog.jelastic.com/2016/08/16/how-to-configure-glassfish-cluster-with-automatic-load-balancing/)

* [Jelastic Cloud API](https://docs.jelastic.com/api-overview)

* [Docker® Standard Support Overview](https://docs.jelastic.com/dockers-overview)
