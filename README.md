# Overview

In this project, we build a Github repository and use the scaffolding that with help us with deploying Flask ML API and perform Continuous Integration and Continuous Delivery. 
* We perform continuous integration using Github Actions that performs linting, testing and dependencies installation. 
* We integrate our project with Azure Pipeline to allow Continuous delivery to Azure App Service.

## Project Plan
Trello board and spreadsheet for project planning and execution.

* A link to a Trello board for the project [link](https://trello.com/invite/b/0O5wVZPH/9804074e7757daa5e631d85b9bd6aa57/building-ci-cd-pipeline)
* Spreadsheet that includes the original and final project plan [link](https://docs.google.com/spreadsheets/d/1G2UlwSD3HVO32IbAr77t-I1oMyIP3ido7AKpit3aojg/edit#gid=0)

## Instructions

  
* Architectural Diagram
![Architectural Diagram](./pictures/Architectural_diagram.png "Architectural Diagram")

### Instructions for running the Python project

We need to create a self/hosted agent a new linux VM that will build and deploy the code

* Login to Azure Portal and Azure Devops. Set up the Azure DevOps account and create organization and project using the following links
    * https://portal.azure.com/
    * https://dev.azure.com/ 

* Set up a new service connection via Azure Resource Manager and Service principal (manual).

* Create a repository in Github and copy the starter code
* Enable Azure Pipeline in the project
* Launch an Azure Cloud Shell environment and create ssh-keys. Upload these keys to your Github account
* Login to Azure Cloud shell and clone the repository
![Cloned repo in Cloud Shell](./pictures/cloned_repo.png "Cloned repo in Cloud Shell")
* Enable Github Actions and copy the yml code with scaffolding
* Verify remote test pass in Github Actions
![Github Actions](./pictures/github_action.png "Github Actions")

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


