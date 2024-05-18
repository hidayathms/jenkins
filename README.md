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





