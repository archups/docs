+++
title = "Manage a cluster"
date = 2018-04-28T12:07:15+02:00
weight = 10
pre = "<b></b>"
+++

## Manage a cluster

#### Cluster overview

Via the menu item "Manage Cluster" you can display your active clusters

![](/img/getting_started/manage_cluster/kubermatic_00.png)

#### Basic cluster information

The dashboard provides you with all important cluster information. You can check the status of your master components and worker nodes.

![](/img/getting_started/manage_cluster/kubermatic_01.png)

![](/img/getting_started/manage_cluster/kubermatic_02.png)

#### Adding new nodes to your cluster

You can easily extend your cluster with new worker nodes. Kubermatic will automatically configure them and interate them into your cluster.

![](/img/getting_started/manage_cluster/kubermatic_03.png)

#### Connect to the cluster

Kubermatic automatically creates your clusters `kubeconfig` file.

![](/img/getting_started/manage_cluster/kubermatic_04.png)

To connect to your cluster configure `kubectl` command line tool to use your `kubeconfig` file

```
$ export KUBECONFIG=$PWD/<your-config-file>
```

You are now able to proxy into your cluster and run your favorite `kubectl` commands!

```                                 
$ export KUBECONFIG=$(pwd)/<your-config-file>                                                
$ kubectl get nodes                               
NAME                          STATUS    ROLES     AGE       VERSION                                      
kubermatic-4js24fv79x-4cqsc   Ready     <none>    1h        v1.10.3                                      
kubermatic-4js24fv79x-r2b9r   Ready     <none>    1h        v1.10.3                                      
kubermatic-4js24fv79x-z2xn5   Ready     <none>    1h        v1.10.3
```