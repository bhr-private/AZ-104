https://learn.microsoft.com/en-us/training/paths/az-104-administrator-prerequisites/

# Git
- gh repo create AZ-104 --public --source=. --remote=upstream

- git init -b main
- git add .
- git commit -m "first commit"
- git branch -M main
- git remote add origin https://github.com/bhr-private/AZ-104
- git push -u origin main

# 1

# 2

az group create -l westeurope -n AZ-104

az deployment group create --name AZ-104 --resource-group AZ-104 --template-file az104-07-vm-template.json --parameters '@az104-07-vm-parameters.json'

az storage account create --resource-group AZ-104 --name az104sa25102023 --sku Standard_LRS --encryption-services blob

# 3

Browse code samples
https://learn.microsoft.com/en-us/samples/browse/?expanded=azure&products=azure-resource-manager

Naming example : devusc-webvm01

## availability sets
An availability set is a logical feature you can use to ensure a group of related virtual machines are deployed together. The grouping helps to prevent a single point of failure from affecting all of your machines.

## update domains and fault domains
Each virtual machine in an availability set is placed in one update domain and one fault domain.
- An update domain is a group of nodes that are upgraded together during the process of a service upgrade
- A fault domain defines a group of virtual machines that share a common set of hardware (or switches) that share a single point of failure.

## Azure Virtual Machine Scale Sets
Azure Virtual Machine Scale Sets are an Azure Compute resource that you can use to deploy and manage a set of identical virtual machines. 

## Implement Azure App Service plans
In Azure App Service, an application runs in an Azure App Service plan. An App Service plan defines a set of compute resources for a web application to run.

## Configure virtual networks
- replicate  on-premises network in the cloud
- Subnets provide a way for you to implement logical divisions within your virtual network
- Azure Bastion protects  virtual machines by browser-based connectivity without the need to expose public IP addresses.
- Azure Virtual Network peering lets you connect virtual networks in the same or different regions, so resources in both networks can communicate with each other.
- Azure Private Link provides private connectivity from a virtual network to Azure platform as a service (PaaS), customer-owned, or Microsoft partner services. 

## Load Balancers
- The load balancer uses a five-tuple (source IP, source port, destination IP, destination port, and protocol type) hash to map traffic to available servers.
- Azure Application Gateway is a load balancer for web traffic.
