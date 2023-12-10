
## Kubernetes Interview Q/A

#### 1. How do you  automate Kubernetes deployment? 

**Answer**. I automate Kubernetes deployments through Infrastructure as Code (IaC) tools like Terraform or AWS CloudFormation for cluster provisioning. For application deployment, I use Kubernetes manifests or Helm charts, and CI/CD pipelines with tools like Jenkins or GitLab CI. This allows for version-controlled, repeatable, and consistent deployments, ensuring efficiency and reducing manual errors.

#### 2. What is exactly self healing in Kubernetes?

**Answer**. Self-healing in Kubernetes refers to the platform's ability to automatically detect and recover from failures or disruptions within the cluster. Kubernetes continuously monitors the desired state of applications and infrastructure. If it detects a discrepancy between the desired state and the current state, it takes corrective actions to reconcile them. This includes restarting failed containers, rescheduling pods to healthy nodes, and maintaining the desired number of replicas. Self-healing mechanisms contribute to the platform's robustness and resilience by minimizing downtime and ensuring that applications run reliably.

#### 3. Is Kubernetes portable? How?

**Answer**.

#### 4. We have pods? Why we use them?

**Answer**.

#### 5. How Kubernetes ensure the availability of applications?

**Answer**. 

#### 6. About replicaset?

**Answer**.

#### 7. Do you have any experience of upgrading the cluster? 

**Answer**.

#### 8. Clusters you are managing is self-hosted cluster or managed Kubernetes cluster?

**Answer**. Explain this answer as per you worked on it - I have experience managing both self-hosted and managed Kubernetes clusters. In certain environments, I've set up and configured self-hosted clusters, providing more customization control. Additionally, I've worked with managed Kubernetes services, such as Amazon EKS, where operational aspects are handled by the cloud provider, allowing a focus on application deployment and scalability.

#### 9. Any scaling experience in kubernetes?

**Answer**. Yes, I have experience with scaling applications in Kubernetes. Kubernetes provides both manual and automatic scaling options. For manual scaling, I've used the 'kubectl scale' command to adjust the number of replicas in a deployment based on demand. Additionally, I've implemented Horizontal Pod Autoscaling (HPA), allowing Kubernetes to automatically adjust the number of replicas based on resource metrics or custom metrics. This ensures optimal resource utilization and responsiveness to changing workloads. Overall, my experience includes efficiently scaling applications in Kubernetes to meet performance and resource requirements.

#### 10. What is kubernetes namespace and why its useful?

**Answer**.

#### 11. What about persistent storage (PVC)?

**Answer**.

#### 12. What is config map?

**Answer**.

#### 13. Do you have any idea about kubernetes service account?

**Answer**.

#### 14. Rolling update on kubernetes and how will you update?

**Answer**.

#### 15. When do we use statefull set or statefull application?

**Answer**.

#### 16. As a kubernetes admin, if i ask to secure my kubernetes cluster and I do not have any information on it? How you will secure?

**Answer**. I will secure kubernetes cluster: 

        - By Role Based Access Control
        - By Network policies- it will control traffic between the pods.
        - By Secrets and conflicts - it will manage your sensitive information.

#### 17. What is minikube?

**Answer**. Minikube is a tool that enables developers to run a single-node Kubernetes cluster locally on their machines. It provides a lightweight and easy-to-set-up environment for testing and developing Kubernetes applications. Minikube allows you to experiment with Kubernetes features, deploy and manage applications in a local cluster, and gain hands-on experience with Kubernetes without the need for a full-scale, multi-node cluster. It's particularly useful for development, testing, and learning Kubernetes in a resource-constrained or offline environment.

#### 18. How to deploy a containerized application?

**Answer**.

#### 19. How to deploy cluster deployment?

**Answer**.

#### 20. How to deploy services?

**Answer**.

#### 21. What are Kubernetes commands? Give examples?

**Answer**.

#### 22. What is Cluster in Kubernetes?

**Answer**. A Kubernetes cluster is a set of machines, called nodes, that collectively run containerized applications orchestrated by Kubernetes. The cluster consists of a control plane that manages the cluster's state and a set of worker nodes where the actual application containers run. The control plane includes components such as the API server, controller manager, scheduler, and etcd, which store the cluster's configuration data. Worker nodes host the containers and run the kubelet, which communicates with the control plane. Kubernetes clusters provide scalability, fault tolerance, and ease of management for deploying and scaling containerized applications.

#### 23. What are container and components?

**Answer**.

#### 24. Why we use Kubernetes?

**Answer**.

#### 25. Explain ClusterIp, Nodeport, LoadBalancer and ExternalName?

**Answer**.

#### 26. What are the difference between Docker and Kubernetes?

**Answer**.

#### 27. Explain deploying application in Kubernetes?

**Answer**.

#### 28. Explain Kubernetes architecture?

**Answer**. Kubernetes architecture consists of a Master Node - which consists of API server, Controller Manager, and Scheduler. 
Worker Node - which consists of Kubelet, Kube Proxy, and Container Runtime), etcd (distributed key-value store), Pods (basic units), Services (network abstraction), and Controllers (manage desired state). These components collaborate to automate containerized application deployment, scaling, and management in a distributed and scalable environment. 

For more detailed explaination -
Master Node:
- API Server: Serves as the entry point for all administrative tasks and communication with the cluster. It validates and configures data for the API objects, such as pods, services, and replication controllers.
- Controller Manager: Monitors the state of the cluster and responds to changes. It includes controller processes for nodes, replication, endpoints, and service accounts.
- Scheduler: Assigns newly created pods to nodes based on resource requirements, policies, and other constraints.
- Etcd: A distributed key-value store that stores the configuration data of the cluster. This data represents the state of the cluster at any given point in time.

Worker Node:
- Kubelet: Ensures that containers are running on a node and communicates with the master to receive instructions.
- Kube Proxy: Maintains network rules on nodes. It manages network communication to and from a pod.
- Container Runtime: The software responsible for running containers. Common runtimes include Docker, containerd, and others.

Pod:
The smallest and simplest unit in the Kubernetes object model. It represents a single instance of a running process in a cluster and consists of one or more containers that share the same network namespace.

Service:
An abstraction that defines a logical set of pods and a policy by which to access them. Services enable communication between different sets of pods as if they were all part of a single application.

Namespace:
A way to divide cluster resources between multiple users, teams, or applications. It provides a scope for names within the cluster.

Volume:
A directory accessible to all containers in a pod. It can be used to share data between containers and to persist data beyond the lifecycle of a pod.

Label:
A key-value pair that is attached to objects, such as pods. Labels are used to organize and select subsets of objects for various purposes.

Controller:
A control loop that watches the desired state of an object in the cluster and takes steps to move the current state closer to the desired state. Examples include ReplicaSets, Deployments, and StatefulSets.

Kubernetes components communicate with each other via the API server, and the etcd cluster ensures consistent and reliable storage of configuration data. This distributed architecture enables high availability, scalability, and resilience in managing containerized applications.

#### 29. What is guestbook?

**Answer**.

#### 30. What is Kubectl?

**Answer**. kubectl is a command-line tool used to interact with Kubernetes clusters. It allows users to deploy, manage, and troubleshoot applications within a Kubernetes environment. With kubectl, you can perform tasks like deploying applications, managing pods and services, scaling deployments, and inspecting cluster resources. It's a crucial tool for Kubernetes administrators and developers working with containerized applications."

#### 31. Why should I go with kubernetes than Docker Swarm?

**Answer**. Kubernetes: Well-suited for large, complex, and multi-service applications. It provides a more extensive set of features, making it highly scalable and suitable for enterprise-level deployments.

Docker Swarm: Simpler and more lightweight, making it easier to set up and manage. It is suitable for smaller projects and environments with less complexity.

- Docker Swarm is not robust multicloud support as kubernetes.
- Kubernetes offers rolling updates, auto-scaling, sophisticated deployment strategies and advanced orchestration features compare to DockerSwarm.

#### 32. What is namespace?

**Answer**. 

#### 33. What is the purpose of operators?

**Answer**.

#### 34. How do you debug your pod or application or issues?

**Answer**. By using "kubectl describe pod <pod-name>". I get all the details of that pod and can debug accordingly. And also we have "kubectl logs <pod-name>" we get log details and can debug using those logs information.

