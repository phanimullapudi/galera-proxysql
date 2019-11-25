# galera-proxysql
Running Galera Cluster with ProxySQL

# Install the PXC Operator

```
$ cd galera-proxysql
$ cd pxc-operator
$ helm install .
```
Once the operator is installed - ensure operator is up and running. You can pass --namespace as parameter to helm to install the operator in custom namespace. But i would prefer to install operator and DB seperately. Proceed to the PXC Database Cluster only after the operator is up and running

# Install the PXC Database Cluster

```
$ cd galera-proxysql
$ cd pxc-db
$ helm install .
```
Once the helm chart is installed - it takes few minutes to bring all the pods and services up. If you need to shrink any resources - like disk, cpu or ram - you can modify them. You can also pass custom my.cnf variables too. Refer the helm chart for more details.
