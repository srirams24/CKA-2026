### **Cluster Architecture Overview (1:03 - 2:09)**
* **Nodes:** A node is essentially a *virtual machine*. A Kubernetes cluster consists of a **Control Plane** (Master Node) for management and **Worker Nodes** for running applications.
* **Pods (3:30 - 5:16):** The smallest deployable unit in Kubernetes. They act as a 'sack' to encapsulate one or more containers, allowing them to share resources.

### **Control Plane Components (5:56 - 13:57)**
These components act as the cluster's management layer:
* **API Server:** The central entry point for all administrative requests and cluster communication.
* **Scheduler:** Determines the best worker node for a pod based on resource availability and constraints (6:35 - 7:40).
* **Controller Manager:** Ensures that the actual state of the cluster matches the desired state by monitoring various objects (7:44 - 8:46).
* **ETCD:** A distributed *key-value data store* that keeps all cluster configuration and state information (8:48 - 13:57).

### **Worker Node Components (13:57 - 16:03)**
* **Kubelet:** A node-based agent that watches for event from the *API Server* to execute tasks (like creating or deleting pods) on the worker node.
* **Kube-Proxy:** Manages network rules and communication between pods and services within the cluster.

### **Workflow Example (16:06 - 23:42)**
* The video details the lifecycle of a request, specifically using `kubectl` to create a pod. It walks through how the request is authenticated, validated, logged into *ETCD*, scheduled, and finally executed by the *Kubelet* on the appropriate worker node.
