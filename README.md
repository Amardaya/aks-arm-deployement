# Azure Kubernetes services ARM Template

This template deploys an AKS cluster.

[![Deploy to Azure](https://azuredeploy.net/deploybutton.svg)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2FAmardaya%2Faks-arm-deployement%2Fmaster%2Fazuredeploy.json)


See https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough  for a walkthrough.


### Configuration via Environmental variables
the template was contain  set of parameters with default values that can be changed during the deployement such us the Ressource Name

| Option                 | Usage                                                                                           |
|------------------------|-------------------------------------------------------------------------------------------------|
| `Resource Name`            | string - The name of the Managed Cluster resource. Default: `openfaascluster`             |
| `Location`        | string - The location of AKS resource. Default: `the ressource group location`          |
| `Dns Prefix`         | string - Optional DNS prefix to use with hosted Kubernetes API server FQDN. Default: `openfaascluster`        |
| `Agent Count`    | integer -The number of the nodes for the cluster the min is 3. Default: `3` |
| `Service Principal App ID`    | secure string - a service principal client ID (used by the cloud provider). Default: `Always` |
| `Service Principal Secret`    | Image pull policy for deployed functions (`Always`, `IfNotPresent`, `Never`.  Default: `Always` |
| `Enable Oms Agent`    | Image pull policy for deployed functions (`Always`, `IfNotPresent`, `Never`.  Default: `Always` |
| `Enable Http Routing Count`    | Image pull policy for deployed functions (`Always`, `IfNotPresent`, `Never`.  Default: `Always` |
| `Max Pod`    | Image pull policy for deployed functions (`Always`, `IfNotPresent`, `Never`.  Default: `Always` |
| `Enable RBAC Pod`    | Image pull policy for deployed functions (`Always`, `IfNotPresent`, `Never`.  Default: `Always` |
