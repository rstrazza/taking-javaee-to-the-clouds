# AWS - Amazon Web Services

[AWS](https://aws.amazon.com) does not need introductions. It is a leader in cloud computing hundreds of services available across the globe for a wide selection of use cases. In the context of Java EE, AWS has a few options available:

## IaaS: EC2

Following the traditional on-premises paradigm to build, support and maintain infrastructure is the famously know AWS Virtual Machines service called [EC2](https://aws.amazon.com/ec2/). The options for Java EE would be installing an Application Server of choice in a pre-selected operating system or chose an [Amazon Machine Image](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html) or AMI. The AMI's are pre-configured, ready to run images that eliminate the original setup. For commercial Application Servers, the license is usually already included in the hourly price, which is obviously more expensive compared to a plain AMI running Ubuntu, for example. Explore the [AWS Marketplace](https://aws.amazon.com/marketplace/b/2649276011?page=1&searchTerms=) and compare with the [Amazon EC2 Instance Types](https://aws.amazon.com/ec2/instance-types/).

Another alternative for application deployment and infrastructure management is running [Docker](https://www.docker.com/what-docker) containers. [Amazon EC2 Container Service](http://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html) offers a container management service solution widely used in the industry.

Examples:

* [Running Java EE on EC2 Instances](aws/ec2/README.md)
* [Running Java EE in a Docker container on EC2 Container Service](aws/ecs/README.md)

# PaaS

[AWS Elastic Beanstalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/Welcome.html) aims at taking control of the underlying infrastructure necessary to run applications, offering to handle the details of capacity provisioning, load balancing, scaling, and application health monitoring.

Example:

* [Running Java EE on Elastic Beanstalk](aws/elasticbeanstalk/README.md)
