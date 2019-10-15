# Kubectl Commands

### View/set K8s context/clusters and namespaces
* `kubectl config view` - view output local ~/.kube/config file contents
* `kubectl config current-context` - view current context
* `kubectl config get-contexts` - view current context and see contexts
* `kubectl config use-context <context>` - change/use context specified
* `kubectl config set-context <context> --namespace <namespace>` - switch to specified namespace
* `kubectl config set-context $(kubectl config current-context) --namespace=monitoring` - switch to specified namespace using current context as variable 

### View Objects
* `kubectl get all` - displays pods, services, ingress, deploymentes etc

### Namespaces
* `kubectl get ns`
* `kubectl create ns <namespace>`
* `kubectl delete ns <namespace>`
* `kubectl get ns --show-labels`

### View PODS and Deployments
* `kubectl get pods`
* `kubectl get pods --namespace app`
* `kubectl get deployments`
* `kubectl describe deployment/pod <name>`

### View Logs
* `kubectl logs <name>`
* flags -f to stream logs or --previous to look at previous pod/container logs

### Create/Delete/Update Apps
* `kubectl apply -f app.yaml`
* `kubectl create -f app.yaml`
* `kubectl create -f app.yaml --namespace app`
* `kubectl delete -f app.yaml`
* `kubectl create/apply -f app.yaml --dry-run` 

### Persistant Storage
* `kubectl get storageclass`
* `kubectl get pv`
* `kubectl get pvc`
* `kubectl create -f <storageclass.yaml>`
* `kubectl delete storageclasss <storageclass>`

### Scale Cluster
* `kubectl scale deployments/planspotter-frontend --replicas=x`
* `kubectl scale deployment.apps/planespotter-frontend --replicas=x`
* `kubectl scale deployments planespotter-frontend --replicas=x`

### Interact with POD
* `kubect get pods`
* `kubectl exec -it pod-uuid /bin/bash --namespace default`

### Authorization
* `kubectl auth can-i {command}`
* `kubectl auth can-i create networkpolicy`
* `kubectl auth can-i --as system:serviceaccount:default:default list`
* `kubectl get clusterroles`
* `kubectl get clusterrolebindings`

### Misc
* `kubectl get virutalservice`
* `kubectl get servieentry` - (monitor using prometheus, etc)
* `kubectl get componentstatus` - check etcd, controller and scheduler status
* `kubectl cluster-info`