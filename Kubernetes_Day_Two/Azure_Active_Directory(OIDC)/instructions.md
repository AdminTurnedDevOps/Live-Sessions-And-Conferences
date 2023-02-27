1. Log into the Azure portal
2. Go to your AKS cluster
3. Go to access control/IAM
4. Click add -> Add Role Assignmnet
5. Choose a role and click "members"
6. Add a new person

You can also do this via the Azure CLI

1. Retrieve the ID of the AKS cluster and put it into a variable.
```
AKS_ID=$(az aks show \
    --resource-group myResourceGroup \
    --name myAKSCluster \
    --query id -o tsv)
```

2. Create an AD user.
```
az ad user create --display-name username\
                  --password \
                  --user-principal-name \
                  --force-change-password-next-sign-in true \
```

3. Add the role assignment to your AKS cluster.
```
az role assignment create \
  --assignee username \
  --role "Azure Kubernetes Service Cluster User Role" \
  --scope $AKS_ID
```