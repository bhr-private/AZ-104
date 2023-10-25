https://learn.microsoft.com/en-us/training/paths/az-104-administrator-prerequisites/

gh repo create AZ-104 --public --source=. --remote=upstream

## push
git init -b main
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/bhr-private/AZ-104
git push -u origin main



#2

az group create -l westeurope -n AZ-104

az deployment group create --name AZ-104 --resource-group AZ-104 --template-file az104-07-vm-template.json --parameters '@az104-07-vm-parameters.json'

az storage account create --resource-group AZ-104 --name az104sa25102023 --sku Standard_LRS --encryption-services blob
