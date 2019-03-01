# PKS Commands

https://docs.pivotal.io/runtimes/pks/1-3/managing-clusters.html

### Authenticate to PKS API
pks login -a <pks-api-url> -u pksadmin —skip-ssl-validation

### Show Clusters
pks clusters

### Show Details for selected Cluster
pks cluster <clustername>

### Create Cluster (-n optional)
pks create-cluster <clustername> -e <external name fqdn> -p small -n <option node number otherwise plan default>

### Delete Cluster
pks delete-cluster <clustername>

### Get Credentials for Cluster (stored in .kube/config)
pks get-credentials <clustername>

### Resize Cluster
pks resize <clustername> --num-nodes 5