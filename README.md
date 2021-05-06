# ARGO VERSION 3.0.2

All the values are already configured for 3.0.2, if you want to change it, 
can change it throgh values.yaml

## Requirements

1) Openshift
2) Helm

-----------------------------------------------------------------------------------------

## Some Installation Command
Use the Install command of helm to install argo and argo-events.

## helm install <folder path> --generate-name

This would apply all the templates.
## kubectl apply -f <filename>

To create role binding , if service account is different then please change the service account

## kubectl create rolebinding default-admin --clusterrole=admin --serviceaccount=default:default

For the workflow to be working on the openshift , change the configmap from docker to pns with
command:
## kubectl get configmap

## kubectl edit configmap 

-------------------------------------------------------------------------------------------

## Registry Credentials
Please update the registry credentials and the github repo from the workflow 
template.

------------------------------------------------------------------------------------------

## Create a webhook on the repo

Go to your github account , select the repo and go to its settings.
Select webhook there and provide the details like URL secret etc.
Please make sure the name of secret is same as that of k8s secret template.
