# crossplane-compositions
### Pre-requisite
oc cli installed  
argocd cli installed

### Steps
1. Login to OpenShift using the below command
```
oc login --token=<your-token> --server=https://api.arcaroytxry.westus2.aroapp.io:6443
```   

2. Login to ArgoCD with OpenShift credential using the below command
```
argocd login --insecure --grpc-web openshift-gitops-server-openshift-gitops.apps.arcaroytxry.westus2.aroapp.io --sso
```  

3. Deploy the `CompositeResourceDefinition` and `Composition`
```
oc apply -f <resource>/<resource>-composite-deploy.yaml
```   

4. Deploy the `Claim`
```
oc apply -f <resource>/<resource>-claim-deploy.yaml
```
