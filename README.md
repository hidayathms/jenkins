# jenkins

This is a repo created to host and document all the learning reslated to jenkins starting from bacis to advanced.

We are going to write pipelines using both declarative and scripted pipelines.

## What is a pipeline?
---

Pipeline is nothing but flow that defines what to happen first and next, typically this a acronmyn used in Jenkins.

---

## Types of pipeline jobs?
---

Pipelines jobs can be written by using 2 ways:
 1.  Declartive approach ( using jenkins provided options: non-programatic)
 2.  Scripted pipeline approach ( This written by using Groovy  and it is a wrapper to java)

 ---

 ## Pipeline Clasifications

 --- 
 v0. FreeStyle ( UI)
 v1. Scriptied Pipelines
 v2. DSL/Declarative pipelines
 v3. YAML ( Still in the develpment phase)
 ---

 ## Naming Standard of a Jenkins pipeline.
---
Pipelines are enclosed in a file that ens with Jenskinsfile(J as in Caps)
---

## How to find which pipelines oraganization used
---

node{ }
Scripted pipeline are old way of doing pipelines, its more programatic and needs groovy skill set.

pipeline{ }
Declarative pipeline are new way of doing pipelines, its declarative and Jenkins recommends this

---

## How to use groovy based commands or options in a Jenkins declarative file?
---
script{
    write your goovy commands
}
----

## security scans
Scans are of 2 type:
1  SAST(Analysinng the code)
2  DAST (Analysing the application through the endpoint/ pen testing)

## Why do i need Static Code Analysis ( SAST - SonorQube)
1. Determine the overall code quality
2. Identifies the hotspots in the code( sensitive information in the code)
3. Code Standard and the package version to be userd can be controlled
4. Identifies the duplicate pattern in the code


## Sonar scanner building commands
sonar-scanner -Dsonar.host.url=http://172.31.41.5:9000 -Dsonar.soruces=. -Dsonar.projectKey=catalogue -Dsonar.login=admin -Dsonar.password=pass

# Maven Goals/Phases
A Maven phase represents a stage in the Maven build lifecycle. Each phase is responsible for a specific task.

Here are some of the most important phases in the default build lifecycle:

    validate: check if all information necessary for the build is available
    compile: compile the source code
    test-compile: compile the test source code
    test: run unit tests
    package: package compiled source code into the distributable format (jar, war, …)
    integration-test: process and deploy the package if needed to run integration tests
    install: install the package to a local repository
    deploy: copy the package to the remote repository

# Types of testing
1) Unit testing : means testing indiviual modules of an application in isolation (without any interaction with dependencies) to confirm that the code is doing things right.
2) Integration testing : means checking if different modules are working fine when combined together as a group
3) Functional testing : means testing a slice of functionality in the system(may interact with dependencies) to confirm that the code is doing the right things.

### How to do Unit Testing & Integration testing
---
Both these test case are typically placed in the code where your application is hosted.  and can be called by the same build tool using test or verify.
If you are node based project:
example : npm test [unit Testing]
          npm verify [Integraton Testing]
---

### How to add your Jenkis Job the ability to run the Job from a particular branch or Tag ?
---


---


### What is the Versioning Strategy we are going through?
---
We are going with Git Semantic Versioning
---

### How to create a Git Tag?
---
Tags are typically created against MAIN branch ONLY.

$git tag 0.0.0
$git push --tags
---

##  How to upload artifacts for nexus
example : curl -v -u admin:admin123 --upload-file pom.xml http://localhost:8081/repository/maven-releases/org/foo/1.0/foo-1.0.pom


## when Artifacts has to be prepared and when they are supposed to be uploaded?
---
1. Only when the TAG_NAME or version of the aritfact that you are trying to upload is not available on Nexus.
2. That means, even before you prepare that ARtifact, lets have a stage to validate against NEXUS on the availibility of that particular version.
3. We need to ensure that BUILD and UPLOAD 

