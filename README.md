# helm-pipelines

## ARGO helm package registry

> https://github.com/argoproj/argo-helm/tree/master/charts/argo

> https://github.com/argoproj/argo-helm/tree/master/charts/argo-events

## Changes from values.yaml of argo repository

> Values.images.tag = v3.0.2

If the server is using certs and running on HTTPS then set to true ( default is false )
> Values.server.secure = false/true

If you are having an forbidden issue while clicking on the eventsources and sensors
from the UI, then add eventsources and sensors under 

> Inside the template , open server-cluster-roles.yaml and add eventsources and sensors under
>  apiGroups.resources


If having an issue when the UI opens that its not able to access , so will have to create a role bind using below command.
Please change the namespaces if its different from default
> kubectl create rolebinding default-admin --clusterrole=admin --serviceaccount=default:default

## Event Templates

Please use the template and also change the access key and secret key from the template. Also change the repository from the 
template.
