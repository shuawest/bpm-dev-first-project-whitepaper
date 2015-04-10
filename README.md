# bpm-dev-first-project-whitepaper
JBoss BPM Suite technical tutorial for creating and deploying rule projects

## Summary

As an application developer with Red Hat JBoss BPM Suite, you have a number of options for how you initially create and package your rules and process assets, how you architecture your application, and how you manage the deployment lifecycle of your business rules and process deployments. Version 6.x added the ability to create, build, deploy, and execute BPM projects entirely through the web based KIE Workbench.  However, many real world application projects still prefer to use a developer first based approach.  This guide walk you through creating and deploying rule and process artifacts to the JBoss BPM Suite execution server using either Maven or Ant based projects.

## Rule and Process Packaging

JBoss BPM Suite 6.x adds new options for packaging your rule and process deployment.  Founded on ubiquitous java  technologies, you can package your rules and process assets in a standard Java Archive, build the project with Maven, and deploy the output archive directly to the JBoss BPM Suite server for execution.  
If you are still using Eclipse projects or Ant builds, that is ok. You can treat the Maven subsystem as a black box if you aren't a maven shop.  You will be able to build you standard way, and  this guide will walk you through the project structure. Upon upload your JAR file to the BPM executions server it will be Mavenized automatically. 

