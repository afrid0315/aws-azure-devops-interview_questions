
## Kubernetes Interview Q/A

#### 1. How do you  automate Kubernetes deployment? 

**Answer**. I automate Kubernetes deployments through Infrastructure as Code (IaC) tools like Terraform or AWS CloudFormation for cluster provisioning. For application deployment, I use Kubernetes manifests or Helm charts, and CI/CD pipelines with tools like Jenkins or GitLab CI. This allows for version-controlled, repeatable, and consistent deployments, ensuring efficiency and reducing manual errors.

#### 2. What is exactly self healing in Kubernetes?

**Answer**. Self-healing in Kubernetes refers to the platform's ability to automatically detect and recover from failures or disruptions within the cluster. Kubernetes continuously monitors the desired state of applications and infrastructure. If it detects a discrepancy between the desired state and the current state, it takes corrective actions to reconcile them. This includes restarting failed containers, rescheduling pods to healthy nodes, and maintaining the desired number of replicas. Self-healing mechanisms contribute to the platform's robustness and resilience by minimizing downtime and ensuring that applications run reliably.

#### 3. Is Kubernetes portable? How?

**Answer**. Kubernetes is highly portable due to its architecture and design. It abstracts away infrastructure details, allowing applications to run consistently across different environments. Kubernetes achieves portability by using containerization (e.g., Docker) to encapsulate applications and their dependencies. Additionally, Kubernetes supports various cloud providers and on-premises environments, providing a consistent orchestration layer. This allows developers to build applications once and deploy them seamlessly across different infrastructures, promoting flexibility and reducing vendor lock-in

#### 4. We have pods? Why we use them?

**Answer**. We use pods in Kubernetes as the smallest deployable units that represent one or more containers closely coupled together. Containers within the same pod share the same network namespace and can communicate with each other using localhost. This allows for efficient communication and coordination between containers within a pod. However, for communication between different pods or services, companies typically use service discovery mechanisms provided by Kubernetes, and communication doesn't rely on localhost but rather on the ClusterIP service or other networking solutions

#### 5. How Kubernetes ensure the availability of applications?

**Answer**. Kubernetes ensures application availability through replication and scaling mechanisms, self-healing practices, and distribution of pod replicas across multiple nodes. Replication Controllers or Deployments maintain the desired number of pod replicas, allowing automatic recovery from failures. Kubernetes' self-healing continuously monitors and corrects discrepancies, while distribution across nodes and Horizontal Pod Autoscaling (HPA) further enhance resilience and scalability, ensuring applications are available and responsive.

#### 6. About replicaset?

**Answer**. A ReplicaSet in Kubernetes is a controller that ensures a specified number of identical replicas, or instances, of a pod are running at all times. It helps maintain the desired level of availability and scalability for applications. If a pod fails or needs to be scaled, the ReplicaSet automatically adjusts the number of replicas to match the specified configuration. ReplicaSets are a key component in achieving high availability and reliability within a Kubernetes cluster.(While we are going to use deployment.yml to actually create pod and in that yml file we give replicas, which is going to create that number of podes and if unfortunately pod deleted. This replicaset is going to auto-heal and create another pod.)

#### 7. Do you have any experience of upgrading the cluster? 

**Answer**. Yes, I have experience upgrading clusters. I follow a systematic approach, ensuring backups, checking compatibility, and performing rolling upgrades. I use tools like kubeadm or KOPS or Kubernetes-specific managed services to streamline the process. Continuous testing in non-production environments is a key practice to identify and address any potential issues before upgrading the production cluster.

#### 8. Clusters you are managing is self-hosted cluster or managed Kubernetes cluster?

**Answer**. Explain this answer as per you worked on it - I have experience managing both self-hosted and managed Kubernetes clusters. In certain environments, I've set up and configured self-hosted clusters, providing more customization control. Additionally, I've worked with managed Kubernetes services, such as Amazon EKS, where operational aspects are handled by the cloud provider, allowing a focus on application deployment and scalability.

#### 9. Any scaling experience in kubernetes?

**Answer**. Yes, I have experience with scaling applications in Kubernetes. Kubernetes provides both manual and automatic scaling options. For manual scaling, I've used the 'kubectl scale' command to adjust the number of replicas in a deployment based on demand. Additionally, I've implemented Horizontal Pod Autoscaling (HPA), allowing Kubernetes to automatically adjust the number of replicas based on resource metrics or custom metrics. This ensures optimal resource utilization and responsiveness to changing workloads. Overall, my experience includes efficiently scaling applications in Kubernetes to meet performance and resource requirements.

#### 10. Explain Kubernetes architecture?

**Answer**. Kubernetes architecture consists of a Master Node - which consists of API server, Controller Manager, etcd (distributed key-value store) and Scheduler. 
Worker Node - which consists of Kubelet, Kube Proxy, and Container Runtime), Pods (basic units), Services (network abstraction), and Controllers (manage desired state). These components collaborate to automate containerized application deployment, scaling, and management in a distributed and scalable environment. 

For more detailed explaination -
Master Node:
- API Server: Serves as the entry point for all administrative tasks and communication with the cluster. It validates and configures data for the API objects, such as pods, services, and replication controllers.
- Controller Manager: Monitors the state of the cluster and responds to changes. It includes controller processes for nodes, replication, endpoints, and service accounts.
- Scheduler: Assigns newly created pods to nodes based on resource requirements, policies, and other constraints.
- Etcd: A distributed key-value store that stores the configuration data of the cluster. This data represents the state of the cluster at any given point in time.

Worker Node:
- Kubelet: Ensures that containers are running on a node and communicates with the master to receive instructions.(Kubelet manages the container that are scheduled to run on that node. It ensure that containers are running and healthy, and that resources they need are available. Kubelet communicates with API server to get information about the containers that are running on node, and then starts and stops the containers as needed to maintain the desired state. It also monitors the containers to ensure the containers running correctly, restarts them if necessary.
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

#### 11. About Network Policies?

**Answer**. Network Policies in Kubernetes are a set of rules that define how pods can communicate with each other and with other network endpoints. They provide a way to control the traffic flow at the pod level, allowing you to define ingress (incoming) and egress (outgoing) traffic rules. Network Policies are particularly useful in microservices architectures, where controlling and securing communication between services is essential for overall application security and performance.
#### 12. What is config map?

**Answer**. A ConfigMap in Kubernetes is a resource that allows you to decouple configuration artifacts from pod specifications. It stores key-value pairs of configuration data, which can be consumed by pods as environment variables, command-line arguments, or as configuration files mounted into the pod's filesystem. ConfigMaps facilitate the separation of configuration concerns from application logic, promoting flexibility and manageability.

For example: When you have sensitive data such as database credentials or user passwords, it's not advisable to put them directly into your application's configuration files or Docker images, as this can pose a security risk. Instead, you can use Kubernetes ConfigMaps to store this sensitive information securely. By using ConfigMaps, you separate the sensitive configuration from your application code and Docker images, which helps improve security. Additionally, Kubernetes provides features such as encryption at rest for secrets, further enhancing the security of sensitive data stored in ConfigMaps or secrets.

#### 13. Do you have any idea about kubernetes service account?

**Answer**. Yes, Kubernetes service accounts are used to control and manage permissions for applications running in a Kubernetes cluster. Each pod can be associated with a service account, allowing it to interact with the Kubernetes API and access resources. Service accounts help implement the principle of least privilege by granting only the necessary permissions to pods. They play a crucial role in securing and managing access within the Kubernetes environment.

#### 14. Rolling update on kubernetes and how will you update?

**Answer**. A rolling update in Kubernetes involves updating a deployment without downtime by gradually replacing old replicas with new ones. I achieve this by adjusting the deployment's replica set, allowing a controlled rollout. I typically use the kubectl set image command or update the deployment YAML with the new image version. Kubernetes ensures a smooth transition by gradually replacing old pods with new ones, maintaining application availability throughout the update process.
(or) 
- Use Deployments: Employ Kubernetes Deployments for managing your application's lifecycle.
- Update Image Version: Modify the Deployment configuration with the new image version.
- Apply Changes: Use kubectl apply to update the configuration and trigger the rolling update.
- Monitor Progress: Keep an eye on the update progress with kubectl rollout status.
- Rollback (if necessary): If issues arise, perform a rollback with kubectl rollout undo.

#### 15. Can you differentiate between Kubernetes Jobs and Cron Jobs, and when would you use each?

**Answer**. Kubernetes Jobs are used for running tasks to completion, ensuring a specified number of completions. Cron Jobs, on the other hand, are used for running repetitive tasks on a schedule. Use Jobs for one-time or batch tasks, and Cron Jobs for recurring tasks, similar to cron jobs in Unix-like systems.

#### 16. As a kubernetes admin, if i ask to secure my kubernetes cluster and I do not have any information on it? How you will secure?

**Answer**. I will secure kubernetes cluster: 

        - By Role Based Access Control
        - By Network policies- it will control traffic between the pods.
        - By Secrets and conflicts - it will manage your sensitive information. (Use Hashicorp Vault, AWS KMS)
        - By inspecting images by using tools like Snyk..
        - Run as a user not as Root(administrator)
        - etcd secure by firewalls

#### 17. What is minikube?

**Answer**. Minikube is a tool that enables developers to run a single-node Kubernetes cluster locally on their machines. It provides a lightweight and easy-to-set-up environment for testing and developing Kubernetes applications. Minikube allows you to experiment with Kubernetes features, deploy and manage applications in a local cluster, and gain hands-on experience with Kubernetes without the need for a full-scale, multi-node cluster. It's particularly useful for development, testing, and learning Kubernetes in a resource-constrained or offline environment.

#### 18. How to deploy a containerized application?

**Answer**. To deploy a containerized application:
- Create Docker Image: Package your application into a Docker image.
- Push Image to Registry: Push the Docker image to a container registry.
- Write Kubernetes Manifests: Create Kubernetes YAML files specifying deployment details.
- Apply Manifests: Use kubectl apply -f to deploy the application to the Kubernetes cluster.
- Monitor and Scale: Monitor the application, and scale as needed using Kubernetes features like replicas and Horizontal Pod Autoscaling.

#### 19. How to deploy cluster deployment?

**Answer**. Create a YAML file specifying the deployment details, including container image, replicas, and any necessary configuration.
Use kubectl apply -f deployment.yaml to deploy the defined resources to the cluster. Monitor the deployment status with kubectl get deployments and kubectl get pods to ensure the desired number of replicas are running.

#### 20. What are the types of services within kubernetes?

**Answer**. There are three types of services in kubernetes that user can create.
- ClusterIp Mode
- Nodeport Mode
- LoadBalancer Mode

#### 21. What are Kubernetes commands? Give examples?

**Answer**. kubectl get pods: List all pods.
kubectl get services: List all services.
kubectl get deployments: List all deployments.
kubectl create configmap <configmap-name> --from-file=<path-to-file>: Create a ConfigMap.
kubectl cluster-info: Display cluster information.
kubectl get nodes: List all nodes in the cluster.

#### 22. What is Cluster in Kubernetes?

**Answer**. A Kubernetes cluster is a set of machines, called nodes, that collectively run containerized applications orchestrated by Kubernetes. The cluster consists of a control plane that manages the cluster's state and a set of worker nodes where the actual application containers run. The control plane includes components such as the API server, controller manager, scheduler, and etcd, which store the cluster's configuration data. Worker nodes host the containers and run the kubelet, which communicates with the control plane. Kubernetes clusters provide scalability, fault tolerance, and ease of management for deploying and scaling containerized applications.

#### 23. What are container and components?

**Answer**. In the context of Kubernetes:
**Container**: A lightweight, standalone, and executable software package that includes everything needed to run a piece of software, including the code, runtime, libraries, and system tools.
**Components**: Refers to the various functional units within a Kubernetes cluster, such as the control plane components (API server, controller manager, scheduler), worker nodes, and add-ons like networking and storage plugins. These components collaborate to manage and run containerized applications.

#### 24. Why we use Kubernetes?

**Answer**. Kubernetes is used to automate and orchestrate containerized applications, providing a consistent and scalable platform. It simplifies deployment, scaling, and management tasks, ensuring high availability, fault tolerance, and efficient resource utilization. Kubernetes abstracts away infrastructure complexities, supports multi-cloud environments, and enhances developer productivity by promoting a declarative and self-healing approach to application deployment.
(kubernetes provides auto-healing, auto-scaling, managing multiple containers and having enterprise level support)
 
#### 25. Explain ClusterIp, Nodeport, LoadBalancer and ExternalName?

**Answer**. ClusterIP provides internal cluster communication, NodePort exposes on a static port for external access, LoadBalancer leverages cloud providers' load balancers for external traffic distribution, and ExternalName maps services to external DNS names. These service types cater to different use cases, ensuring flexibility and adaptability to various networking requirements

#### 26. What are the difference between Docker and Kubernetes?

**Answer**. Docker is a containerization platform that allows packaging and distributing applications along with their dependencies. It provides a standardized unit (container) for application deployment.

Kubernetes, on the other hand, is a container orchestration platform. It automates the deployment, scaling, and management of containerized applications. Kubernetes orchestrates multiple Docker containers, ensuring their efficient operation, high availability, and scalability.(Kubernetes provide auto-healing, auto scaling, clustering and enterprise level support like load balancing).

In summary, Docker is for containerization, while Kubernetes is for container orchestration, providing a robust solution for deploying and managing containerized applications at scale.

#### 27. Have you ever used multiple containers within a single pod in Kubernetes? Provide an example.

**Answer**. Yes, I've used multiple containers within a single pod in Kubernetes. For instance, in a web application pod, I might have both a main application container and a sidecar container for log shipping. The containers share the same network namespace and storage, facilitating coordination and enhancing application functionality.

**Scenario you can explain**. Consider a web application that generates logs. You want to ship these logs to an external service for analysis. In this scenario, you could have a pod with two containers:
- Main Application Container:
Contains the primary web application that generates logs.
- Sidecar Container:
A separate container running a log shipping agent (e.g., Fluentd, Filebeat).
The sidecar container reads logs from the main application container, processes them, and sends them to a centralized logging service. 

#### 28. What is the role of kube-proxy?

**Answer**. Kube-proxy works by maintaining a set of network rules on each node in the cluster, which are updated dynamically as services added or removed. When a client sends request to a service, the request is intercepted by Kube-proxy on the node where it was received. Kube-proxy then looks up the destination endpoint for the service and routes the request accordingly.
 Kube-proxy is the essential component of a kubernetes cluster, as it ensures that services can communicate with each other.

#### 29. What is guestbook?

**Answer**. Guestbook is a simple, classic example application often used in Kubernetes tutorials and demos. It consists of a front-end service where users can leave messages, and a back-end service storing those messages. Guestbook showcases the deployment of a multi-tier application in Kubernetes, illustrating concepts like service discovery, scaling, and persistence.

#### 30. What is Kubectl?

**Answer**. kubectl is a command-line tool used to interact with Kubernetes clusters. It allows users to deploy, manage, and troubleshoot applications within a Kubernetes environment. With kubectl, you can perform tasks like deploying applications, managing pods and services, scaling deployments, and inspecting cluster resources. It's a crucial tool for Kubernetes administrators and developers working with containerized applications."

#### 31. Why should I go with kubernetes than Docker Swarm?

**Answer**. Kubernetes: Well-suited for large, complex, and multi-service applications. It provides a more extensive set of features, making it highly scalable and suitable for enterprise-level deployments.

Docker Swarm: Simpler and more lightweight, making it easier to set up and manage. It is suitable for smaller projects and environments with less complexity.

- Docker Swarm is not robust multicloud support as kubernetes.
- Kubernetes offers rolling updates, auto-scaling, sophisticated deployment strategies and advanced orchestration features compare to DockerSwarm.

#### 32. What is namespace?

**Answer**. In a kubernetes namespace is a logical isolation of resources, network policies, rbac and everything. For example, there are two projects using same k8s cluster. One project can use namespace1 and other project can use namespace2 without any overlap and authentication problems.

#### 33. What is the purpose of operators?

**Answer**. The purpose of operators in Kubernetes is to automate the management and operation of applications by encoding operational knowledge into software. Operators extend Kubernetes functionality to handle complex, stateful applications, providing a way to deploy, scale, and manage them more effectively through the use of custom controllers and automation scripts.

#### 34. How do you debug your pod or application or issues?

**Answer**. By using "kubectl describe pod <pod-name>". I get all the details of that pod and can debug accordingly. And also we have "kubectl logs <pod-name>" we get log details and can debug using those logs information.

#### 35. What is the difference between Docker container and Kubernetes pod?

**Answer**. A pod in kubernetes is a runtime specification of a container in docker. A pod provides more declarative way of defining using YAML and you can run more than one container in pod.

#### 36. What is ingress?

**Answer**. In Kubernetes, Ingress is an API object that manages external access to services within the cluster. It acts as a layer 7 HTTP and HTTPS traffic router, providing rules for directing requests to the appropriate services based on paths, domains, and other criteria. Ingress enables more sophisticated routing and allows for centralized management of external access configurations.

#### 37. What is the difference between ingress and loadBalancer service type? Why they use ingress?

**Answer**. The key difference between Ingress and LoadBalancer service types in Kubernetes is that LoadBalancer provisions an external load balancer to expose a service, while Ingress is an API object that manages external access to services. Ingress provides additional capabilities such as path-based routing, SSL termination, and more, making it more versatile for managing HTTP and HTTPS traffic. It's preferred for complex routing scenarios and enables efficient use of resources by handling multiple services through a single external IP address.

#### 38. What about RBAC? 

**Answer**. RBAC, or Role-Based Access Control, in Kubernetes is a security mechanism to control access to resources. It defines roles and role bindings, allowing fine-grained permissions management. Roles specify what actions are allowed, and role bindings associate roles with users or groups. RBAC enhances security by restricting unauthorized access to sensitive operations and resources within the Kubernetes cluster.

#### 39. What is Helm?

**Answer**. Helm is a package manager for Kubernetes that simplifies the deployment and management of applications. It uses charts, which are packages of pre-configured Kubernetes resources, to define, install, and upgrade even complex applications. Helm streamlines the process of managing Kubernetes manifests, making it easier to share, version, and deploy applications consistently.

#### 40. When you create a new version of your Docker image, what steps do you follow?

**Answer**. Firstly, we create a docker file in that file we can make necessary code and enhancements. Add the version, build the image, test the image locally to ensure it works as expected then push it to Docker registry. Update Kubernetes manifests and deploy the updated application with the new image version to the target environment.

#### 41. Have you ever worked with horizontal pod autoscaling (HPA) in Kubernetes? If so, how do you set it up?

**Answer**. I ensure the Kubernetes Metrics Server is deployed in the cluster to collect resource usage metrics. For pods, I configure them to expose resource metrics, such as CPU or memory usage. I create an HPA (HorizontalPodAutoscaler) resource, specifying the target metrics (e.g., CPU) and scaling parameters, like the minimum and maximum number of replicas. For example hpa.yml is
```
apiVersion: autoscaling/v2beta2
kind: HorizontalPodAutoscaler
metadata:
  name: my-app-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: my-app
  minReplicas: 2
  maxReplicas: 10
  metrics:
  - type: Resource
    resource:
      name: cpu
      targetAverageUtilization: 70
```
After defining the HPA, I apply it to the cluster using kubectl apply -f hpa.yaml. This setup allows Kubernetes to automatically adjust the number of pod replicas based on resource metrics, ensuring optimal performance and resource utilization for the application.

#### 42. Explain the purpose of persistent storage in Kubernetes and why it's needed.

**Answer**. Persistent storage in Kubernetes is crucial for preserving data beyond the lifecycle of individual pods. It ensures that data persists even if a pod or node fails, enabling stateful applications. Persistent Volume Claims (PVCs) simplify storage management by abstracting underlying storage details, providing dynamic provisioning, and facilitating easier scaling and data persistence for applications.

#### 43. Describe a scenario where you would use Persistent Volumes (PVs) and Persistent Volume Claims (PVCs) in Kubernetes.

**Answer**. I would use Persistent Volumes (PVs) and Persistent Volume Claims (PVCs) in Kubernetes when deploying a stateful application, such as a database. PVs represent physical storage resources, and PVCs act as a request for storage by the application. This ensures data persistence and allows the application to retain state even if the underlying pods are rescheduled or restarted. PVs and PVCs provide a way to dynamically provision and manage storage for stateful workloads in a scalable and reliable manner.

#### 44. How do you manage secrets in your Kubernetes project, and what role does Kubernetes Secret play?

**Answer**. In my Kubernetes project, I manage secrets using Kubernetes Secrets, a built-in resource for securely storing sensitive information like API keys or passwords. Kubernetes Secrets encode and store these values, ensuring they are not exposed in plaintext within the cluster. I reference secrets in pod specifications, either mounting them as files or exposing them as environment variables, to securely provide confidential data to applications running in the cluster.

#### 45. Can you explain a scenario where you would use a service mesh in Kubernetes, especially in terms of authentication and authorization?

**Answer**. I would use a service mesh in Kubernetes, such as Istio, in scenarios where I need to enhance communication between microservices. Specifically, for authentication and authorization, a service mesh provides capabilities like mutual TLS for secure communication, fine-grained access control, and user identity propagation. This ensures that only authorized services can communicate securely within the cluster, improving overall security and governance."

#### 46. Why are Pod Security Policies important in Kubernetes, and how would you implement them to enhance security?

**Answer**. Pod Security Policies (PSPs) are crucial in Kubernetes to enforce security measures for pods. They define the security context under which pods run, mitigating risks. To implement PSPs, you define policies specifying allowed actions and restrictions, ensuring pods adhere to security standards. This enhances security by preventing unauthorized access, minimizing privileges, and promoting a secure container runtime environment.
- To enhance security with Pod Security Policies (PSPs) in Kubernetes, I would:
- Define PSPs: Specify security policies detailing pod behavior.
- Enable Admission Controller: Activate the PodSecurity admission controller to enforce PSPs.
- Create RoleBindings: Associate PSPs with Kubernetes roles to apply policies to namespaces or clusters.
- Review and Adjust: Regularly audit and adjust PSPs based on security requirements and application needs.
- Educate Users: Ensure users understand and follow security best practices when deploying pods to maintain a secure environment.
  
#### 47. Do you work with resource limits and resource quotas in your Kubernetes setup? If yes, how do you set them up?

**Answer**. Yes, in my Kubernetes setup, I utilize resource limits and quotas for effective resource management. To set them up, I define resource limits in pod specifications to restrict CPU and memory usage. For resource quotas, I create a ResourceQuota object in the desired namespace, specifying limits for CPU, memory, and other resources. This helps prevent resource overuse and ensures fair resource distribution among applications within the cluster.

#### 48. How would you implement horizontal pod scaling based on custom metrics specific to your application's performance indicators?

**Answer**. To implement horizontal pod scaling based on custom metrics in Kubernetes, I would follow these steps:
- Install a Metrics Provider: Deploy and configure a custom metrics provider like Prometheus or Datadog to collect application-specific metrics.
- Define a Custom Metrics API: Expose custom metrics in a format compatible with the Kubernetes Custom Metrics API.
- Set Up Horizontal Pod Autoscaler (HPA): Create an HPA resource, specifying the custom metric and target value for scaling.
```
apiVersion: autoscaling/v2beta2
kind: HorizontalPodAutoscaler
metadata:
  name: my-app-hpa
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: my-app
  metrics:
  - type: External
    external:
      metricName: custom.metric/name
      targetValue: 100
```
- Apply Configurations: Apply the configurations to the cluster using kubectl apply -f.
This setup allows Kubernetes to dynamically adjust the number of pod replicas based on your application-specific performance metrics.

#### 49. Explain a scenario where pod priority and premption in Kubernetes would be useful, and have you ever implemented this?

**Answer**. Pod priority and preemption in Kubernetes are useful in scenarios where certain pods, such as critical services, need preferential treatment during resource allocation. For example, a critical production service might be assigned a higher priority to ensure it gets resources over less critical background tasks. While I haven't implemented this directly, understanding the concept is crucial for optimizing resource allocation in Kubernetes.

#### 50. In what situations would you use StatefulSets in Kubernetes, and what benefits do they offer over Deployments?

**Answer**. I would use StatefulSets in Kubernetes for stateful applications that require stable network identities and persistent storage. StatefulSets provide ordered and unique pod identifiers, ensuring predictable hostnames and persistent volumes for each replica. This is beneficial for databases, distributed systems, or applications with specific node dependencies. StatefulSets offer stronger guarantees for stateful workload orchestration compared to Deployments.

#### 51. How can you change the number of replicas for a ReplicaSet in Kubernetes, and what should you check for if the replicas are not scaling as expected?

**Answer**. To change the number of replicas for a ReplicaSet in Kubernetes, you can edit the replicas field in the ReplicaSet's YAML or you can use the kubectl scale command. For example:.
```
kubectl scale replicasets my-replicaset --replicas=3
```
If replicas are not scaling as expected, check for issues such as resource constraints, unsatisfied PodDisruptionBudget, or problems with the underlying container runtime.

#### 52. Can you explain the ingress controller routing mechanism?

**Answer**. The Ingress controller manages external access to services in a Kubernetes cluster. It uses rules and configurations to route incoming traffic to the appropriate services based on criteria such as hostnames, paths, or other attributes. This routing mechanism allows for efficient and flexible traffic management, enabling the cluster to handle external requests and distribute them to the relevant services within.

#### 53. Kubernetes commands?
**Answer**. 
```
kubectl apply -f httpd-deploy 
kubectl get deployment
kubectl get namespace
kubectl apply -f httpd-deploy
kubectl apply -f httpd-service 
kubectl get service -n <namespace>
kubectl set image deployment/httpd-deploy httpd=httpd:2.4.43 --namespace=xfusion - to update image of existing deployment(rolling update)
kubectl rollout status deployment/httpd-deploy --namespace=xfusion - to check status of particular rollout deployment
kubectl rollout undo deployment/httpd-deploy --namespace=xfusion - to roll back to existing deployment.
kubectl get pods - to get pods
kubectl get pods -l app=httpd --namespace=xfusion - to get particular pods of namespace
kubectl get service httpd-service --namespace=xfusion
kubectl rollout history deployment/httpd-deploy --namespace=xfusion
```

#### 54. How to increase node in eks?
**Answer.** Increasing Nodes in EKS:

Auto Scaling Group (ASG): Adjust the desired capacity of the ASG associated with the EKS node group.

AWS Console: Navigate to the EKS console, select the node group, and modify the desired capacity.

AWS CLI: Use the eks update-nodegroup-version command to modify the node group capacity.

HCL Configuration: If using Terraform or other Infrastructure as Code tools, update the configuration file and apply the changes.

Verification: Ensure that the new nodes are added to the EKS cluster, and monitor cluster health after scaling.

#### 55. Why it’s using v1/apps in service file in kubernetes?
**Answer.** The use of v1/apps in a Kubernetes deployment file indicates the API version and resource type being used. In the context of Kubernetes definitions, v1 refers to the core API version, and apps refers to the resource type, which typically relates to applications.

#### 56. Can we have multiple conatiners in a pod? Can we have similar conatiners in a pod? Lets say i have 4 conatiners, one of them has failed how would you check which container has failed?
**Answer.** Yes, multiple containers can be in a single pod in Kubernetes. These containers share the same network namespace and can communicate with each other using localhost.

Yes, it is possible to have similar containers in a pod.

To check which container has failed in a pod with multiple containers, you can use the following command:
```
kubectl describe pod <pod_name>
```
Look for the Events section, and it will provide details about the status and events related to each container within the pod, helping you identify the one that has failed.

#### 57. What is liveness and readiness probe? Why we need them?
**Answer.** 
Liveness Probe:

Definition: A liveness probe is a mechanism to determine if a container is running and healthy.
Purpose: Ensures that the application inside the container is responsive and prevents routing traffic to unhealthy instances.
Readiness Probe:

Definition: A readiness probe checks if a container is ready to accept traffic.
Purpose: Ensures that the container is fully initialized and ready to serve requests before being included in the pool of service instances.
Why We Need Them:

Liveness Probe:

Prevents routing traffic to containers that are unresponsive or in a faulty state.
Ensures the continuous availability and health of the application.
Readiness Probe:

Ensures smooth traffic transitions during updates or scaling by letting Kubernetes know when a container is ready to serve requests.
Enhances the reliability and stability of a service by avoiding premature traffic to containers that might still be initializing.
Overall, liveness and readiness probes contribute to the robustness and reliability of applications in a containerized environment.

#### 58. Have you worked on kubernetes monitoring? Which tools you have used?
**Answer.** Yes, I have experience with Kubernetes monitoring. I have used tools such as:

Prometheus: For collecting and querying metrics from Kubernetes clusters.
Grafana: Used in conjunction with Prometheus for visualization and dashboard creation.
Kube-state-metrics: Provides additional Kubernetes-specific metrics for better insights.
Alertmanager: Integrated with Prometheus for alerting based on defined rules.
Kubernetes Dashboard: For a graphical interface to monitor cluster resources and activities.
These tools collectively offer comprehensive monitoring, alerting, and visualization capabilities for Kubernetes environments.

#### 59. Can we deploy a pod on particular node??
**Answer.** Yes, we can deploy a pod on a particular node in Kubernetes by using node affinity or node selectors. These mechanisms allow specifying constraints to influence pod placement, ensuring that the pod runs on a node with specific attributes or labels.

#### 60. Workload in Kubernetes?
**Answer.** Workload in Kubernetes:

- Definition: Refers to the application components or processes running on a Kubernetes cluster.

- Types: Common workloads include Deployments, StatefulSets, DaemonSets, and Jobs, each serving specific application requirements.

- Management: Kubernetes workloads are managed using declarative configurations, enabling scalability, resilience, and ease of deployment.

#### 61. Kuberntes cost optimisation?
**Answer.** Kubernetes Cost Optimization:

Right-sizing: Adjust resource requests and limits for pods to match actual usage.

Auto-scaling: Dynamically scale the number of pods based on demand to avoid overprovisioning.

Resource Quotas: Enforce limits on resources consumed by namespaces to prevent resource sprawl.

Node Pools: Use different node pools with varied instance types based on workload requirements.

Pod Disruption Budgets: Control the number of simultaneous pod disruptions during updates to maintain stability.

Monitoring and Alerts: Implement monitoring to identify inefficiencies and set up alerts for cost-related anomalies.

#### 62. What is Kubernetes networking, and how does it work?
**Answer. Kubernetes Networking:** 
Kubernetes networking is the set of principles and components enabling communication between pods, services, and external entities in a Kubernetes cluster.

#### 63. What is a pod IP, and how is it used in Kubernetes networking?
**Answer. Pod IP in Kubernetes Networking:**
A Pod IP is a unique internal IP address assigned to a pod, allowing communication within the cluster.

#### 64. What is a node port, and how is it used in Kubernetes networking?
**Answer.** Node Port is a Kubernetes service type that exposes a service on a static port on each node, enabling external access.

#### 65. How does Kubernetes handle load balancing for services?
**Answer.** Kubernetes uses kube-proxy to handle load balancing for services, distributing traffic across healthy pods.

#### 66. What is a network policy, and how is it used in Kubernetes networking?
**Answer.**  Network Policy is a Kubernetes resource defining rules for pod-to-pod communication, allowing or restricting traffic.

#### 67. What is the difference between a Kubernetes Service and a Kubernetes Ingress?
**Answer.** Service: Routes traffic within the cluster based on service IPs.
Ingress: Manages external access, handling HTTP and HTTPS traffic and allowing more advanced routing.

#### 68. What is a Kubernetes ExternalName service, and how is it used in networking?
**Answer.**  ExternalName service maps a Kubernetes service to a DNS name, facilitating external resource access.

#### 69. What is the difference between a Layer 4 load balancer and a Layer 7 load balancer, and which one is better for Kubernetes?
**Answer.** 
Layer 4: Operates at the transport layer, handling IP and port information.
Layer 7: Works at the application layer, considering content and making routing decisions based on HTTP attributes.

#### 70. How does Kubernetes integrate with cloud-based load balancers, such as AWS ELB or Google Cloud Load Balancing?
**Answer.** Integration: Kubernetes integrates with cloud-based load balancers, leveraging services like AWS ELB or Google Cloud Load Balancing for external access.

#### 71. What is the difference between a Kubernetes ClusterIP service and a Kubernetes NodePort service?
**Answer.** 
ClusterIP: Exposes a service only within the cluster.
NodePort: Exposes a service on a static port on each node, allowing external access.

#### 72. What is a Kubernetes Headless service, and how is it used in networking?
**Answer.** A Headless service in Kubernetes doesn't assign a Cluster IP, providing a stable network identity for pods but without load balancing. (or) A Kubernetes Headless Service is a type of Service that doesn't assign a ClusterIP to its Pods. Instead, it allows direct communication with individual Pods via their IP addresses. It's useful for scenarios such as StatefulSets, where stable network identities for Pods are required, or for enabling peer-to-peer communication. Clients resolve the Service's DNS name to a list of individual Pod IP addresses for direct communication.

#### 73. Difference between Node and Pod?
**Answer.** Node: A node is a physical or virtual machine within a Kubernetes cluster. It provides resources and runs Kubernetes services.

Pod: A pod is the smallest deployable unit in Kubernetes, containing one or more tightly coupled containers. Pods share resources and networking context. They run on nodes.

#### 74. What is pod, how many containers we can run in single pods, any limitations?
**Answer.** A Pod is the smallest deployable unit in Kubernetes, representing one or more containers that are deployed together on the same host.
- A single Pod can contain one or more containers, typically related and tightly coupled, that share networking and storage resources.
- While there is no strict limit on the number of containers within a single Pod, it's generally recommended to keep Pods focused on a single concern or tightly coupled set of concerns for better maintainability and scalability.

#### 75. Different deployment strategies one can take when they're deploying any application, or, you know, virtual machines or containers or anything like that?
**Answer.** Different deployment strategies include:

Blue-Green Deployment: Running two identical production environments, with one serving live traffic (blue) while the other is idle (green). The green environment is updated with new changes, tested, and then swapped with the blue environment to minimize downtime.

Canary Deployment: Gradually rolling out changes to a small subset of users or servers before deploying them to the entire infrastructure. This allows for testing in a real-world environment and mitigates the risk of widespread issues. (We have two identical environments v1 and v2-version2. We slowly test v2 by deploying few users like 10% and remaining 90% in v1, after v2 running fine all other 90% also we deploy in v2).

Rolling Deployment: Deploying changes gradually across a pool of servers or instances, one at a time, while ensuring the application remains available throughout the process. This strategy helps minimize downtime and allows for quick rollback if issues arise.

Immutable Deployment: Deploying changes by replacing the entire infrastructure with a new, immutable version. This ensures consistency and reproducibility but may involve longer deployment times and increased resource usage.

Feature Flags: Deploying changes but controlling their activation using feature flags. This allows for gradual feature rollout, testing, and experimentation without deploying multiple versions of the application.

Each deployment strategy has its own advantages and considerations, and the choice depends on factors such as the application's architecture, requirements, and risk tolerance.

#### 76. Kubectl means?
**Answer.** Kubecontrol.

#### 77. About taint and tolerations in kubernetes?
**Answer.** In Kubernetes, taints are used to repel pods from nodes, while tolerations allow pods to be scheduled on nodes with matching taints. They're mechanisms for controlling pod placement in the cluster.

#### 78. About static pod and normal pod?
**Answer.** Static pods are managed directly by the kubelet on a node, while normal pods are managed by the Kubernetes API server. Static pods are typically used for system components like kube-proxy or kubelet itself, whereas normal pods are deployed through Kubernetes manifests and managed by controllers like Deployments or StatefulSets.

#### 79. About daemonset?
**Answer.** DaemonSet ensures that all (or some) nodes run a copy of a pod. It's used for background tasks like log collection or node monitoring where each node in the cluster needs a copy of the pod.

#### 80. What is the path of directory holding static pod definition files?
**Answer.** path is cd /etc/kubernetes/manifests/

#### 81. From where are we retrieving logs in Kubernetes and where can we locate the log paths?
**Answer.** In Kubernetes, logs are typically retrieved directly from the containers running inside pods. The path to the logs depends on how the application inside the container is configured to output its logs. Generally, logs are accessed via the container runtime interface or through logging agents like Fluentd or Fluent Bit.

#### 82. kubernetes can we have backup?
**Answer.** Yes, Kubernetes supports backups. You can back up Kubernetes resources and persistent data using tools like:

1. **Velero**: A popular open-source tool for backing up and restoring Kubernetes cluster resources and persistent volumes.
2. **ETCD Backup**: For clusters using ETCD as the data store, you can back up ETCD directly.
3. **Persistent Volume Snapshots**: Use Kubernetes VolumeSnapshots to create snapshots of persistent volumes.

These methods ensure you can recover your Kubernetes cluster and data in case of failures or data loss.

#### 83. What is a DaemonSet, and how is it used?
