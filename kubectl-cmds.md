# Kubectl Commands

`kubectl get all`

### Namespaces
* `kubectl get ns`
* `kubectl create ns <namespace>`
* `kubectl delete ns <namespace>`
* `kubectl get ns --show-labels`

### Use Cluster
* `kubectl config use-context <clustername>`

### Set Context
* `kubeclt config set-context <clustername> --namespace <namespace>`

### Assign dev context to development namespace
* `kubectl config set-context dev --namepsace=development --cluster=my-cluster`

### View PODS and Deployments
* `kubectl get pods`
* `kubectl get pods --namespace app`
* `kubectl get deployments`

### Create/Delete Apps
* `kubectl create -f app.yaml`
* `kubectl create -f app.yaml --namespace app`
* `kubectl delete -f app.yaml`

### Persistant Storage
* `kubectl get storageclass`
* `kubectl get pv`
* `kubectl get pvc`
* `kubectl create -f <storageclass.yaml>`
* `kubectl delete storageclasss <storageclass>`

### Scale Cluster
* `kubectl scale deployments/planspotter-frontend --replicas=x`
* `kubectl scale deployment.apps/planespotter-frontend --replicas=x`

### Interact with POD
* `kubect get pods`
* `kubectl exec -it pod-uuid /bin/bash --namespace default`