https://learn.microsoft.com/en-us/training/paths/az-104-administrator-prerequisites/


#2

az group create -l westeurope -n AZ-104

az deployment group create --name AZ-104 --resource-group AZ-104 --template-file az104-07-vm-template.json --parameters '@az104-07-vm-parameters.json'

az storage account create --resource-group AZ-104 --name az104sa25102023 --sku Standard_LRS --encryption-services blob
