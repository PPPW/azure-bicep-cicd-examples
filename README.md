# Azure Bicep CI/CD Pipeline Example

This repo provides some examples CI/CD Pipelines for infrastructure-as-code on Azure with Bicep. Although people are generally more familiar with testing frameworks for the application code, it is not very clear how to test the infrastructure code. As a result, the Bicep changes are sometimes deployed to production without any testing. We made this doc for the best practices with steps:

[Bicep CI/CD Handbook](https://azure.github.io/bicep-cicd-handbook/)

This repo has two example pipelines: 
- CI Pipeline: performs linting, template validation. You can also do unit test by [PSRule](https://github.com/microsoft/PSRule), which simulates ARM for validations.

![CI Pipeline](./figs/CI%20pipeline.png)


- CD Pipeline: deploys to different stages. Before deploying to prod, we run "what-if" and display the changes in the Pipeline web UI and wait for manual approval.

![CD Pipeline](./figs/CD%20pipeline.png)

Note: the code in this repo is now moved to [bicep-cicd-starter](https://github.com/Azure/bicep-cicd-starter).
