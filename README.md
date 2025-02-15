[![Build Status](https://travis-ci.org/mborges-pivotal/pcf-ers-demo1.svg?branch=master)](https://travis-ci.org/mborges-pivotal/pcf-ers-demo1)
[ ![Download](https://api.bintray.com/packages/mborges-pivotal/generic/pcf-ers-demo1/images/download.svg) ](https://bintray.com/mborges-pivotal/generic/pcf-ers-demo1/_latestVersion)

# TAS/PCF Base Demo
Base Spring Boot application to demonstrate TAS capabilities

## Credits and contributions
As you all know, we often transform other work into our own. This is all based from Andrew Ripka's [cf-workshop-spring-boot github repo](https://github.com/pivotal-cf-workshop/cf-workshop-spring-boot) with some basic modifications.

## Introduction
This base application is intended to demonstrate some of the basic functionality of TAS:

* TAS/PCF api, target, login, and push
* TAS/PCF environment variables
  * Spring Cloud Profiles
* Scaling, self-healing, router and load balancing
* RDBMS service and application auto-configuration
* Blue green deployments

## Getting Started

**Prerequisites**
- [Cloud Foundry CLI](http://info.pivotal.io/p0R00I0eYJ011dAUCN06lR2)
- [Git Client](https://git-scm.com/downloads)
- An IDE, like [Spring Tool Suite](https://spring.io/tools)
- [Java SE Development Kit](https://www.oracle.com/java/technologies/javase-downloads.html)

**Building**
```
$ git clone [REPO]
$ cd [REPO]
$ ./mvnw clean install
``` 

### To run the application locally
The application is set to use an embedded H2 database in non-PaaS environments, and to take advantage of Pivotal CF's auto-configuration for services. To use a MySQL Dev service in PCF, simply create and bind a service to the app and restart the app. No additional configuration is necessary when running locally or in Pivotal CF.

In Pivotal CF, it is assumed that a Pivotal MySQL service will be used.

```
$ ./mvnw spring-boot:run
```

Then go to the http://localhost:8080 in your browser

### Running on Cloud Foundry
Take a look at the manifest file for the recommended setting. Adjust them as per your environment.

## Labs/Demo Scripts summary
We have a [Labs](https://github.com/krishnaatpivotal/tas-springboot-demo/tree/master/Labs) folder to help you learn TAS/PCF. These labs can be used for workshops or self-training.    


