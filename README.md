## Spark-Jupyter-Kubernetes

Set up a spark cluster managed by kubernetes, and a jupyter notebook frontend. 

### How to set up

#### Notes:

1) You should do these steps in the order they are written. Make sure each process is complete before you move on to the other step. For example when you create the spark-master-controller, wait for the pod to pull the container image and become fully operational before you create the service for it. 

2) In all the `*-nfs.yaml` files, make sure you put in the ip address of your nfs server.

#### kubect commands:

- kubectl create -f namespace-spark-cluster.yaml
- kubectl create -f spark-master-nfs.yaml
- kuebctl create -f spark-master-controller.yaml
- kubectl create -f spark-master-service.yaml
- kubectl create -f spark-ui-controller.yaml
- kubectl create -f spark-ui-service.yaml
- kubectl create -f spark-worker-nfs.yaml
- kubectl create -f spark-worker-controller.yaml
- kubectl create -f notebook-nfs.yaml
- kubectl create -f notebook-controller.yaml
- kubectl create -f notebook-service.yaml


Good luck...
