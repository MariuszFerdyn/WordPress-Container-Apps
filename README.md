# WordPress - High Performance, Autoscaling, Serverless, Container Apps

This repository contains resources to deploy WordPress in Azure Container Apps.

Azure Container Apps consumption plan can be very cost-effective, as it is billed based on per-second resource allocation and requests. The first 180,000 vCPU-seconds, 360,000 GiB-seconds, and 2 million requests each month are free.

On the other hand, it can scale to many instances to handle high traffic and operate more efficiently than WordPress on App Service.

## Fast Deploy form Azure Market Place

https://azuremarketplace.microsoft.com/en-us/marketplace/apps/fast-smsnet1696229509341.wordpress-containerapps-serverless?tab=Overview

## Deployment Guide - Azure CLI

Here are the step-by-step instructions to deploy WordPress on Azure Container Apps: [deploy.yml](https://github.com/MariuszFerdyn/WordPress-Container-Apps/blob/main/.github/workflows/deploy.yml)

This guide gives you an idea of how Azure Container Apps can be configured step by step with WordPress.

It can be used in a pipeline

## Easy Deployment Using ARM Template

You can easily deploy using a complete ARM template. Just copy it as a custom deployment in the [Azure Portal](https://portal.azure.com/#view/HubsExtension/TemplateEditorBladeV2/template/%7B%0A%20%20%20%20%22%24schema%22%3A%20%22https%3A%2F%2Fschema.management.azure.com%2Fschemas%2F2019-04-01%2FdeploymentTemplate.json%23%22%2C%0A%20%20%20%20%22contentVersion%22%3A%20%221.0.0.0%22%2C%0A%20%20%20%20%22parameters%22%3A%20%7B%7D%2C%0A%20%20%20%20%22resources%22%3A%20%5B%5D%0A%7D).

The ARM Template source: [mainTemplate.json](https://github.com/MariuszFerdyn/WordPress-Container-Apps/blob/main/ARM/mainTemplate.json)

## Build Managed Application

It can be used as an Azure Application to distribute it across your organization. Here is a [definition UI](https://github.com/MariuszFerdyn/WordPress-Container-Apps/blob/main/ARM/createUiDefinition.json) and here is a [pipeline that deploys it](https://github.com/MariuszFerdyn/WordPress-Container-Apps/blob/main/.github/workflows/CreateManagedApp.yml).

`app.zip` can be used as the source for an Azure Marketplace offer.
