## Create and Seecure Azure Kubernetes Service Cluster
Azure Kubernetes Service (AKS) cluster using an Nginx ingress controller to lock it down with basic authentication and free [![Let's Encrypt]](https://letsencrypt.org/) TLS certificates.
### Using ARM Template
we need to create a static public IP in the node ressource groupe either using the Azure Portal or the Azure Cli as below 



'''
you might be tempted to create a DNS name label for this IP address so you can avoid using a custom domain name, but *.cloudapp.azure.com host names don't work with Let's Encrypt.
'''