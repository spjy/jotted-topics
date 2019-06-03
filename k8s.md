# Kubernetes (K8s)

Kubernetes is a comprehensive system that handles the management and deployment of containerized applications (i.e. [Docker containers]()). It can handle aspects such as load balancing, networking, scaling and even CI/CD. 

## Kubernetes Jargon

#### Kubernetes Clusters

A Kubernetes Cluster is the collection of computers or virtual machines that Kubernetes controls such that the cluster can function in unison. 

It consists of:

* [A Master]()
* [Node(s)]()

#### Master

The master of a cluster is the central body that manages the cluster.

It is in charge of:
* Scheduling
* Maintaining application states
* Scaling applications
* Updating

#### Nodes

Nodes work for the master, and they run applications. They are able to communicate with the master through the Kubernetes API.

Nodes consist of:

* A Kubelet
* A container runtime
* Containerized application(s)

#### Kubernetes Deployment

When a cluster gets created, you can begin a deployment. A Kubernetes Deployment is a specified configuration telling Kubernetes how to create and update your application instances.

Additionally, scaling is handled here. You can create replicas of a pod and increase or decrease as needed.

#### Kubernetes Pods

A Kubernetes Pod is an instance of an application. It consists of at least one container and any associated containers/resources. In addition to including containers, Pods store:
* Networking information
* Configurations for the container

#### Kubernetes Service

A Kubernetes Service is a configuration that handles the networking portion of nodes. For instance, you can assign specific IP addresses, ports to a node and publicize it for the world to see.

#### CI/CD

Kubernetes is also capable of CI/CD. It is intelligent enough to implement "rolling updates" such that your services do not experience downtime if an update is needed. It does this by updating one pod at a time such that one is always available.

## Kube Control (kubectl)

To interface with a Kubernetes instance, download the Kubernetes CLI, aka kubectl.

### Common Commands

#### kubectl 

## Minikube

Minikube is a local instance of Kubernetes. It is **not** recommended for production!
