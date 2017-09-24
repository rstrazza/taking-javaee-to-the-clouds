# Running Java EE on Elastic Beanstalk

[AWS Elastic Beanstalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/Welcome.html) aims at taking control of the underlying infrastructure necessary to run applications, offering to handle the details of capacity provisioning, load balancing, scaling, and application health monitoring.

This PaaS offering supports [several platforms](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html) but might be considered somewhat limited to the Java ecosystem by offering Java SE (jar) and Tomcat. It has preconfigured Docker images with GlassFish 4 in addition to regular Docker support to bring your image.

The preconfigured images are available on [Docker Hub](https://hub.docker.com/r/amazon/aws-eb-glassfish/) which can be an option for [local testing](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_dockerpreconfig.walkthrough.html).

## Setup Preconfigured Container

* Open Elastic Beanstalk and click on Get Started to create a Web Application

![alt text](img/eb-get-started.png)

* Enter the Application name and select the GlassFish platform. Select the Upload your code radio button and click Upload

![alt text](img/eb-create-web-app.png)

* The Upload your code screen will open, select a local file or provide a S3 URL. Give a version label and click Upload

![alt text](img/eb-create-web-app-upl-war.png)

* Back to the Create a web app page, click Configure more options button

![alt text](img/eb-create-web-app-config.png)

* The configuration presets could move from a Low cost to High availability option. On the Instances section, click Modify to change the Instance type to t2.medium for higher Memory and CPU. Save the changes

![alt text](img/eb-create-web-app-config-instance.png)

* Take a moment to review all the available configuration and click Create app

![alt text](img/eb-create-web-app-config-custom.png)

![alt text](img/eb-create-web-app-config-create-app.png)

* After a few minutes the infrastructure will be provisioned and the application deployed

![alt text](img/eb-create-web-app-done.png)

* Click on the environment URL to open the Cargo Tracker application

![alt text](img/cargo-tracker.png)

## References

* [Creating and Deploying Java Applications on AWS Elastic Beanstalk](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_Java.html)
* [Deployment Policies and Settings](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/using-features.rolling-version-deploy.html?icmpid=docs_elasticbeanstalk_console)
