Deploying SAP Commerce Cloud patched version
==========================
This branch contains a patched version of KIE Server to use the patched Drools version required by SAP Commerce.

In order to be able to deploy it to your Maven remote repository :
* Deploy the Drools/jBMP BOMs using the patched Drools version for SAP Commerce : https://github.com/guiliguili/droolsjbpm-build-bootstrap/tree/feature/BIT-5925
* Deploy the patched Drools modules for SAP Commerce : https://github.com/guiliguili/drools/tree/feature/BIT-5925
* Update the `distributionManagement` management sections to use your Maven remote repository in [pom.xml](./pom.xml)
* Deploy the drools root module and [kie-server-parent](./kie-server-parent) individually by running `mvn clean deploy -N`
* Deploy the modules under [kie-server-parent/kie-server-wars](./kie-server-parent/kie-server-wars) by running `mvn clean deploy`

Developing Drools and jBPM
==========================

**If you want to build or contribute to a kiegroup project, [read this document](https://github.com/kiegroup/droolsjbpm-build-bootstrap/blob/master/README.md).**

**It will save you and us a lot of time by setting up your development environment correctly.**
It solves all known pitfalls that can disrupt your development.
It also describes all guidelines, tips and tricks.
If you want your pull requests (or patches) to be merged into master, please respect those guidelines.
