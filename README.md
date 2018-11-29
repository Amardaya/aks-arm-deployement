# Azure Kubernetes services ARM Template

This template deploys an AKS cluster.

[![Deploy to Azure](https://azuredeploy.net/deploybutton.svg)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2FAmardaya%2Faks-arm-deployement%2Fmaster%2Fazuredeploy.json)

s

See https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough  for a walkthrough.


### Configuration via Environmental variables
the template was contain  set of parameters with default values that can be changed during the deployement such us the Ressource Name

| Option                 | Usage                                                                                           |
|------------------------|-------------------------------------------------------------------------------------------------|
| `Resource Name`            | Boolean - use http probe type for function readiness and liveness. Default: `false`             |
| `Location`        | HTTP timeout for writing a response body from your function (in seconds). Default: `60s`        |
| `Dns Prefix`         | HTTP timeout for reading the payload from the client caller (in seconds). Default: `60s`        |
| `Agent Count`    | Image pull policy for deployed functions (`Always`, `IfNotPresent`, `Never`.  Default: `Always` |
