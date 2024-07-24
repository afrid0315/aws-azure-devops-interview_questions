# Troubleshooting Scenario's Faced in daily tasks

#### 1. Tell me about a time when you spent a lot of time solving a problem.
**Answer.** I have faced few challanges that 
**Scenario 1:** During a critical period, our organization experienced email delivery failures. After an in-depth investigation, I discovered a misconfiguration in the Postfix service settings. Specifically, the relay server details were incorrect, causing mail to be stuck in the queue. By rectifying the configuration and implementing appropriate testing procedures, I successfully restored normal email functionality.

**Scenario 2 a:** Once in our Kubernetes cluster, a pod failed to start. Upon inspecting the logs and details, I found that the pod comprised two containers: a main container and a side-car container responsible for storing logs from the main container. It became apparent that the issue stemmed from an improperly specified image for the side-car container. After correcting the image name and version, the pod started successfully. (ImagePullBack error)

**Scenario 2 b:** Once in our Kubernetes cluster, a pod failed to start. While checking ``kubectl get pods`` got status is crashloopbackoff. This indicates the pod is not in running state. By checking kubectl describe got details in that I found due to insufficient resources on the node. Then manually, I scaled up the cluster to ensure more nodes available for pods. Or we can scale up replicas in deployment.yml file. (Sometimes there can be a sudden jump in load. You might be notified about this if you track your service's success rate.In this scenario, you have two choices: You can either increase the CPU, using the same steps as you used for memory allocation, or you can increase the number of instances for your pods. The recommended method is to increase the number of instances. For example, increase the number of replicas to five:

``kubectl scale deployment myDeployment –replicas=5``)

**Scenario 7 - this scenario related to scenario 2b:** In a previous role as a DevOps engineer, I encountered an issue where a Kubernetes cluster shared by multiple development teams was impacted by a pod experiencing memory leaks. This led to instability across the entire cluster, but it was unclear which pod or namespace was causing the problem.

To address this, I implemented 'resource quotas and limits' on the pods within each namespace. This allowed us to pinpoint the specific pod responsible for the issue and contain the impact to that particular component.

In a related scenario, after setting up these limits, I noticed that the problematic pod was frequently being terminated with an 'OOMKilled' (Out Of Memory) error, resulting in a 'CrashLoopBackOff' status. This status is not an error itself but indicates that the pod is repeatedly crashing and restarting. By using kubectl describe on the pod, I confirmed that the cause was indeed out of memory errors. This setup helped us quickly identify and address resource allocation issues, improving overall cluster stability. We were able to reduce and know where this issue occuring by using resource limits and quoatas but at the end when we find due to particular pod or microservices leakage was happening. So, we can take thread dump or heap dump and send to developers and solve and upgrade accordingly.

**Scenario 2 c:** If a recent deployment causes issues, one of the fastest and easiest ways to remedy this is by using rollbacks. To see the deployment history:

kubectl rollout history deployment myDeployment
The output looks similar to this:

kubectl rollout history deployment myDeployment
 deployment.extensions/myDeployment
REVISION CHANGE-CAUSE
1               <none>
2               <none>
3               <none>
4               <none>
The most recent deployment is the one with the highest number (4, in this example). Perform a rollback to the previous deployment (3):

kubectl rollout undo deployment myDeployment –-to-revision=3
You will see new pods created.

It's wise to set your deployment history to save a specific number of versions. Do so by setting revisionHistoryLimit.

For example:
spec:
replicas:2
revisionHistoryLimit:20

**Scenario 3:** In the context of our high-availability infrastructure, we implemented an HAProxy Load Balancer (LBR) on a dedicated server to ensure the availability and reliability of our application servers. Recently, I encountered a troubleshooting issue where the HAProxy service was not activating and running as expected. I found that the backend configuration was commented out in the '/etc/haproxy/haproxy.cfg' file. Removing the '#' enabled the backend, resolving the issue and allowing the service to start successfully, ensuring high availability for our application servers.

**Scenario 4.** Team identified that the application is unable to connect to the database. After digging into the issue, the team found that mariadb service is down on the database server.The MariaDB service failed to start due to an error during the ExecStartPre phase, specifically in the mysql-prepare-db-dir script. The script reported that the MariaDB directory /var/lib/mysql was not empty, preventing the initialization process. Despite creating an empty directory and validating its contents, the issue persisted, suggesting the need for further investigation to identify the root cause.

**Scenario 5.** The Apache HTTP Server on the system encountered a startup failure, as revealed by the output of systemctl status httpd.service. Apache service failed due to a syntax error in the DocumentRoot directive. Resolution involved correcting the directive, restarting Apache, and verifying the status. Log analysis was performed in case of persistent issues (systemctl status, config file, logs).

**Scenario 6. Kubernetes Pod Failed to Start Due to Image Name Mismatch**

The Kubernetes pod encountered a startup failure, as revealed by the output of kubectl describe pod <pod-name>. The pod failed due to an InvalidImageName error because the image name in the deployment configuration did not match the lowercase format required by the Azure Container Registry (ACR). The resolution involved correcting the image name in the deployment YAML to a lowercase format, updating the image pull secret to ensure access to ACR, reapplying the deployment pipeline, and verifying the pod status. Log analysis and configuration reviews were performed in case of persistent issues (kubectl logs, kubectl describe pod, deployment YAML).
