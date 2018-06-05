# Scalr CICD-DEMO

## Introduction

Enterprises use the Scalr enterprise-grade cloud management platform to build a standardized self-servicep process for consuming cloud resources. 

To deliver self-service, admins match end-users with the provisioning method that makes them most productive. Repetitive, cookie-cutter requests might go through a simplified Self-Service Catalog, while more advanced requests would go through the Power Console. 

This demo is designed as a conceptual example of how to leverage Scalr in a CI/CD workflow, using Scalr Farm Templates, API, and Power Console. 

## Workflow

 A user commits a change to GitHub, in this example a webpage, GitHub then sends a webhook to Jenkins, which initiates the build process by which Jenkis and deploys the code to a Dev environment. The owner of the new dev stack is the user who originally committed to GitHub.

Jenkins then runs the necessary tests, if the test passes, the code is deployed to a staging environment, and the dev stack is terminated. Whether you want to automate this next step is up to you, but typically this is where you’d perform any necessary manual testing or tasks. 

Once the code is ready for production, we’ll fire Scalr orchestration event that promotes the application from staging to a production environment. 

It’s important remember that we’re using GitHub and Jenkins for this example, but you can use whichever repo and build automation system you prefer. 


## Instructions
