# Kubernetes Components

## Control Plane

Is the main point of control of kubernetes configuration. It is composed of the components below which are also Kubernetes pods that runs in our cluster.

### api (kube-apiserver)

Is the frontend for cluster comunication
It is the single entrypoint for cluster management
kubectl connects to the api
It handles security concerns, authentication...

### etcd

It is responsible for storing configuration, application states and cluster metadata

### sched (kube-scheduler)

It is responsible for distributing pods based on resources
It takes the node the is most suitable for receiving new pods based on their capacities

### c-m (kube-controller-manager)

It is responsible for monitoring nodes and responds to changes in their state

### c-c-m (kube-cloud-controller-manager)

Handles cloud-specific monitoring

## Node

Is a physical machine that is responsible for hosting our pods and running our containers. The node must also had some components to perform their actions in a k8s environment which are:

### kubelet

It is responsible for running the pods containing our containers

### k-proxy (kube-proxy)

Implements the network rules for communications with the hosts and the pods of our cluster

### container runtime

Is the software responsible for running our containers inside our pods. The most common one is Docker but it is not the only one available. We also can use Rancher or ContainerD for instance