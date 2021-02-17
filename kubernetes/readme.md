Kubernetes Architecture

A Kubernetes master runs Control Plane responsible for maintaining the desired state of the cluster we discussed above. In its turn, the Kubernetes Control Plane consists of several components with unique roles (see the image below):

Component	Description :-
Etcd	This is a data store used by Kubernetes to store all information about the cluster. It’s critical for keeping everything up to date
kube-apiserver	This component exposes Kubernetes API to users allowing them to create API resources, run applications, and configure various parameters of the cluster.
kube-controller-manager	The component that manages API objects created by users. It makes sure that the actual state of the cluster always matches the desired state
kube-scheduler	This component is responsible for scheduling user workloads on the right infrastructure. When scheduling applications, kube-scheduler considers various factors such as available node resources, node health, and availability, as well as user-defined constraints.
cloud-controller-manager	This component embraces various controllers, all of which interact with the cloud providers’ APIs.
