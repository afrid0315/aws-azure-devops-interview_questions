# These interview questions taken from multiple resources 
# Company-wise Interview Questions

## Google- Cloud Engineer, Technical Solution Specialist, Technical Solution developer
#### 1. Google HR Screening
- What are the HTTP method are? PUT POST DELETE GET
- What is the time complexity of merge sort?
- What are the status code are available?
- What is the difference between PUT and POST?
- What is the website cookies?
- How to check IO Usage for machine? SAR Utilities
- How to Capture and Analyze Network Traffic? Tcpdump
- How to check boot logs in linux? journalctl -b
- What is the significance of SIGKILL?
- Which single will be send to OS when you run kill -9 PID command in linux? SIGKILL
- Caching mechanism?
- How the TCP Handsheek work behind the screen?
- When you deploy web server what are the security measure you would take?
- How the internet work high level?
- Data Structure
- Code was given you need to understand flow and tell them the final output
- Tree Question (Left order traversal)
- String palindrome
- Bubble Sort (But it was wrong code and they told me I need to identify the
bug and correct it and tell the time complexity of the algorithm and any
better sorting algorithm apart form this).

#### 2. Google RRK1 Interview Question
- How would you check whether the user has to execute permission or not?
- How do you call the HTTP request method without a browser or curl?
- What are the parameter available in the curl command?
- A different alternative and flavor for curl command?
- What happen we you run the cat command on terminal internal workflow?
- What if I got an error cat command not found what could be the possible issue?
- What if I can’t able to SSH into the remote machine? What is the possible step would
you take to make it possible or check what is the issue?
- It is mandatory to use port 22 for ssh if any other port is possible? ->
https://www.quora.com/Is-it-really-a-bad-practice-to-open-port-22-and-SSH-to-the-produ
ction-server-directly
- Practical coding round java code snippet was given?

#### 3. Google RRK2 Interview Question
- Basic web technology.
- Type of Request
- What Type of status code?
- What is the HTTP method? PUT, POST, DELETE
- What is the difference between PUT & POST?
- Basics of networking, more about OSI model.
- OS Related concepts
- Shell commands for a particular situation.
- If a user wants to access the file in read mode. What command can use?
- Brief about all the HTTP error codes and their explanation.
- What is the possible way we can debug the website issues?
- Networking concepts any very basics of networking some of the questions were direct and some were twisted?
- Explain the OSI model and its protocol?
- Basic Networking commands like nslookup, dig, ping, traceroute.

#### 4. Google GCA + System Desgin
- System Design basic concepts.
- Design Caching Server?
- Design Netflix streaming engine?
- What is a load balancer what is it?

#### 5. Google Googleiness + Leadership
- They Check whether you are fit for the company or not.
- Some general questions and then he asked questions related to the role, basically he
wanted to know whether I know about the role.
- He started giving me hypothetical questions and scenarios and he asked about my
approach to them.
- Tell something about a situation that I faced in my file and how I dealt with it.
- There was a technical situation given and he asked me to solve it in both technical and
non-technical ways.



# Amazon - Cloud Support Engineer (deployment)

#### 1. Docker file to create image we need ls -lrth need to be executed 
#### 2. Dockerfile to create image ls -lrth in user1 and ls - la in user2 to executed how to do?
#### 3. ⁠kubernetes components
#### 4. ⁠kubernetes workflow (if we click kubectl run some pod, wat  the exact workflow or mechanism of kubernetes?
#### 5. ⁠wat is ur daily activities 
#### 6. ⁠about rbac
#### 7. ⁠docker drivers 
#### 8. ⁠docker networking
#### 9. ⁠wat u did automation in ur daily activities 
#### 10. ⁠pod is not deleting wat we do to delete 
#### 11. ⁠if we are having same name of containers with same port can we achieve this? How
#### 12. ⁠docker stages
#### 13. ⁠how docker created from kernel? What is the kernels which used to create docker
#### 14. ⁠can u tell me wat are other docker like tools we have.
#### 15. We are getting logs right from where it is getting path of logs in kubernetes
#### 16. How can I reduce docker size
#### 17. Difference between deployment and replicaset? If we mention replicas in deployment then wat is the purpose of replicaset file
#### 18. Booting process, dns query
#### 19. Dns recursive process, iterative process
#### 20. Different classes of private subnets can we connect
#### 21. Dhcp
#### 22. A time when u took on a task that was beyond your job ?
#### 23. Can two different private subnets with different clases can communicate ?

𝐑𝐨𝐮𝐧𝐝 𝟏- 𝐓𝐞𝐜𝐡𝐧𝐢𝐜𝐚𝐥

1) Can you explain the ingress controller routing mechanism
2) What will happen if you get no space left on device
3) What are the RCA rule along with SRE 4 rules that you will apply while you create the alerts for your application
4) How you will achieve the DB high availability and fault tolerance
5) What is jenkins and security tools
6) How docker is integrated in jenkins
7) Write terraform code to have the AWS with1 VPC 2 Subnets and each having 1 ec2 instance
8) Tell all the scenarios too implement the security in kubernetes
9) Your Prod systems are down and being an SRE what are the Steps you are going to take to solve the issue

𝐑𝐨𝐮𝐧𝐝 2- 𝐓𝐞𝐜𝐡𝐧𝐢𝐜𝐚𝐥

10) AWS application design in current organization
11) AWS Ec2 types volumes, difference between ALB and NLB(General Purpose SSD volumes (gp3), gp2,IO, throughput, load balancer)
13) why your application choose the above load balancer
14) How the CORS present in S3 (Select the bucket from the
list, and click Configure CORS. Paste the CORS configuration XML into the text box, and click Save. To modify the CORS setting for the bucket, update the CORS configuration XML in the text box, and click Save)
15) S3 types, R53 and the use in our application ()
16) Amazon certificate manager (ACM)
17) Kubernetes (pods managemet, memory and ram utilization check)
18) Types of Kubernetes services (loadbalancer, Ingress,clusterip, nodeport)


𝐑𝐨𝐮𝐧𝐝𝟑 - 𝐂𝐨𝐝𝐢𝐧𝐠

19) What is DNS caching
20) What is an i node
21) The systems CPU and Memory are spiking up and at the same time PODs are in crashloop back what steps you would take to resolve the issue
22) Write the Python code to hit the rest endpoint and take our all the urls from the json and again check if the status is 200 or not
23) One more python code based on Leetcode

𝐑𝐨𝐮𝐧𝐝 𝟒 - 𝐒𝐲𝐬𝐭𝐞𝐦 𝐃𝐞𝐬𝐢𝐠𝐧

24) Design a high availability 3 tier system where your deployments will happen on kubernetes

𝐑𝐨𝐮𝐧𝐝 𝟓 - 𝐌𝐚𝐧𝐚𝐠𝐞𝐫𝐢𝐚𝐥/𝐓𝐞𝐜𝐡𝐧𝐢𝐜𝐚𝐥

25) Why would you be a good fit for a senior management position?
26) What’s your most significant achievement so far?
27) Tell me a scenario where you had critical issue and you went beyond and above to solve that issue
