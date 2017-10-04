# Running Java EE on Google Cloud Platform

IaaS = Compute Engine

Google App Engine has two environments: [Standard](https://cloud.google.com/appengine/docs/standard/) and [Flexible](https://cloud.google.com/appengine/docs/flexible/java/). At a high level, the Standard environment is a sandbox that supports a specific Java version, intended to be a low cost or even free runtime that is highly scalable. The Flexible environment on the other hand is a better fit for dockerized applications with additional dependencies on the environment.

|Standard environment | Flexible environment|
|---------------------| --------------------|
|Limited free tier.	| No free tier.|
|Java 7 only.	| Java 8 only.|
|Sandboxed, supports a subset of Java libraries.| Docker-based, any Java package that works on Debian Linux.|


# References
* [Java on Google Cloud Platform](https://cloud.google.com/java/)
* [Choosing an App Engine Environment](https://cloud.google.com/appengine/docs/the-appengine-environments)
