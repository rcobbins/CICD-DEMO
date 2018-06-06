# Scalr CICD-DEMO

## Introduction

Enterprises use the Scalr enterprise-grade cloud management platform to build a standardized self-servicep process for consuming cloud resources. 

To deliver self-service, admins match end-users with the provisioning method that makes them most productive. Repetitive, cookie-cutter requests might go through a simplified Self-Service Catalog, while more advanced requests would go through the Power Console. 

This demo is designed as a conceptual example of how to leverage Scalr in a CI/CD workflow, using Scalr Farm Templates, API, and Power Console. 

## Workflow

 A user commits a change to GitHub, in this example a webpage, GitHub then sends a webhook to Jenkins, which initiates the build process by which Jenkis deploys the code to a devolpment Environment in Scalr. 

Jenkins then runs the necessary tests, if the test passes, the code is deployed to a staging Environment, and the dev stack is terminated. Whether you want to automate this next step is up to you, but typically this is where you’d perform any necessary manual testing or tasks. For the purpose of this demo - we are using a manual staging process - visially verifying the new code has been deployed.

Once the code has been verified in the staging Enviroment, we’ll fire a Scalr orchestration event that promotes the application from staging to a production Environment. 

It’s important remember that we’re using GitHub and Jenkins for this example, but you can use whichever code repository and build automation system you prefer. 


## Instructions
Need to add
