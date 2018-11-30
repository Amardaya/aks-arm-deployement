# Create Azure Kubernetes Service Cluster
## Using ARM Template

This template deploys an AKS cluster with predefined parameters optimized for my openfaas usage.
to deploy this template we just need to hit the button below no need to install anything in your machine 

[![Deploy to Azure](https://azuredeploy.net/deploybutton.svg)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2FAmardaya%2Faks-arm-deployement%2Fmaster%2Fazuredeploy.json)


See https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough  for a walkthrough.


### Configuration via Environmental variables
the template was contain  set of parameters with default values that can be changed during the deployment such us the Ressource Name here is the list of some parameters that can be changed please need we will need to create a service principal for the Kubernetes Cluster to interact with Azure APIs see https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/aks/kubernetes-service-principal.md on how to do it 

| Option                 | Usage                                                                                           |
|------------------------|-------------------------------------------------------------------------------------------------|
| `Resource Name`            | string - The name of the Managed Cluster resource. Default: `openfaascluster`             |
| `Location`        | string - The location of AKS resource. Default: `the ressource group location`          |
| `Dns Prefix`         | string - DNS prefix to use with hosted Kubernetes API server FQDN. Default: `openfaascluster`        |
| `Agent Count`    | integer -The number of the nodes for the cluster the min is 3. Default: `3` |
| `Service Principal App ID`    | secure string - a service principal client ID (used by the cloud provider). |
| `Service Principal Secret`    | secure string - the service principal client secret.  |
| `Enable Oms Agent`    | boolean flag to turn on and off of omsagent addon (`true`, `false`.  Default: `true`|
| `Enable Http Routing Count`    | boolean flag to turn on and off of http application routing(`true`, `false`.  Default: `true` |
| `Max Pod`    | Maximum number of pods that can run on a node..  Default: `40` |
| `Enable RBAC Pod`    | boolean flag to enable RBAC (`true`, `false`.  Default: `true` |


## Create AKS Cluster using Azure Cli
the other way to create aks cluster is to use Azure Cli ,to be able to run this you need to make sure that you have the latest Azure Cli installed in your machine 

```azurecli
az aks create --resource-group $<Yourressourcegroup> --name <$Yourclustername> --node-count 3 -s Standard_E4s_v3 -p <$Yourdnsprefix> -m 30 -k 1.11.4 --enable-addons monitoring -a http_application_routing --generate-ssh-keys 
```
