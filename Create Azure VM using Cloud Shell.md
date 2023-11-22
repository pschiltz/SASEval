Open Cloud Shell from the Azure Portal
```
git clone https://github.com/pschiltz/SASEval.git
```
```
az deployment group ~~what-if~~ --resource-group "SAS_Trial" --template-file SASEval/azuredeploy.json --parameters SASEval/azuredeploy.parameters.json
```
```
az deployment group create --resource-group "SAS_Trial" --template-file SASEval/azuredeploy.json --parameters SASEval/azuredeploy.parameters.json
```