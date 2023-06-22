# learn-bicep-azure

This repo give a quick demo of using Bicep to deploy resource in Azure.

<h2>Overview:</h2>

- Bicep is a Domain Specific Language that uses declarative syntax to deploy Azure resources.

- Define infrastructure in Bicep file to deploy the resources in Azure.

- Deploy the resources in consistent manner using Bicep.

- Bicep is a transparent abstraction over ARM template JSON and doesn't lose any of the JSON template capabilities.

- Use Bicep instead of JSON to develop your Azure Resource Manager templates (ARM templates)

<h2>Benefits:</h2>

- No Cost and open source (supported by Microsoft Support)
- Supports all resource types and API Versions
- Simple Syntax
- Authoring experience using VSCode Bicep extension
- Repeatable Results
- Orchestration
- Modularity
- Preview Changes using what-if operation
- No state or state file to manage

<h2>Prerequisite</h2>

 - Azure Subscription https://azure.microsoft.com/en-us/free/
 - Azure cli https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli 
 - Install bicep using Azure cli :
   
   az bicep install
   

The main.bicep file contains the infrastructure details (vnet and storage account) that to be deployed.

<h2> Deploy the bicep file:</h2>

az group create --name demoRG --location eastus

az deployment group create --resource-group demoRG --template-file main.bicep --parameters storageName = myDemoStorage

<h2> To clean us the resource</h2>

az group delete --name demoRG
