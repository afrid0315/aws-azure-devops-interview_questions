## DevOps Interview Questions & Answers

#### 1. How do you handle issues at the production level?

**Answer.** At the production level, I prioritize proactive monitoring and alerting to catch issues early. I follow incident response procedures, involve relevant stakeholders promptly, leverage logging and metrics for diagnosis, and implement a robust rollback strategy. Continuous improvement through post-incident reviews ensures lessons are learned and applied to prevent future issues.

#### 2. How do you support/collaborate with various teams? 

**Answer.** I foster open communication, establish clear channels for collaboration, and regularly engage with cross-functional teams. I actively participate in meetings, utilize collaboration tools, and ensure that everyone is aligned on goals and timelines. Additionally, I proactively share information, offer assistance, and seek input to strengthen overall teamwork.

#### 3. How can our self-owned databases, infrasturcture better than cloud migrated services?

**Answer.** Maintaining our own databases and infrastructure offers greater control over security, customization, performances. It allows for tailored solutions to specific needs, avoiding reliance on third party providers. However, Cloud migration provides scalability, cost-efficiency and automated maintenance. The choice depends on your organization's priorities, resources and long-term strategies.

#### 4. Write the grrovy script for retry option in jenkins?
**Answer.** 
```
  pipeline {
    agent any

    parameters {
        // Define your parameters here if needed
    }

    stages {
        stage('Retry Stage') {
            steps {
                script {
                    retry(3) {
                        // Your code to be retried goes here
                        echo "Trying something..."
                        
                        // Example: Simulating a failure on the first attempt
                        if (currentAttempt == 1) {
                            error "Simulated failure!"
                        }
                    }
                }
            }
        }
    }

    post {
        failure {
            echo "The job failed after retrying."
            // Additional failure handling steps if needed
        }
    }
}
```
#### 5. What is the port of Sonarkube?
**Answer.** Sonarkube starts with the port 9000.

#### 6. How to find thread dump of java application?
**Answer.** To find a thread dump of a Java application:
- Identify the Java process ID (PID) using jps or ps -ef | grep java.
- Use jstack command: jstack <PID> > thread_dump.txt.
- The thread dump is saved in the specified file (thread_dump.txt), revealing the state of all threads in the Java application.

#### 7. Design the 3 tier architecture for your telecommunications project?
**Answer.** The 3-tier architecture for our telecommunications project comprises three layers: the presentation layer for user interface, the application layer for business logic, and the data layer for storage and retrieval. This design ensures modular scalability, separation of concerns, and efficient management of telecommunications services.



Round4/5 [ Managerial ]

  


-Can you explain the ingress controller routing mechanism
-What will happen if you get no space left on device
- What are the RCA rule along with SRE 4 rules that you will apply while you create the alerts for your application
-How you will achieve the DB high availability and fault tolerance
-What is jenkins and security tools
-How docker is integrated in jenkins
-Write terraform code to have the AWS with1 VPC 2 Subnets and each having 1 ec2 instance
- Tell all the scenarios too implement the security in kubernetes
- Your Prod systems are down and being an SRE what are the Steps you are going to take to solve the issue


𝐑𝐨𝐮𝐧𝐝𝟑 - 𝐂𝐨𝐝𝐢𝐧𝐠

-What is DNS caching
-What is an i node
- The systems CPU and Memory are spiking up and at the same time PODs are in crashloop back what steps you would take to resolve the issue
-Write the Python code to hit the rest endpoint and take our all the urls from the json and again check if the status is 200 or not
- One more python code based on Leetcode

𝐑𝐨𝐮𝐧𝐝 𝟒 - 𝐒𝐲𝐬𝐭𝐞𝐦 𝐃𝐞𝐬𝐢𝐠𝐧

- Design a high availability 3 tier system where your deployments will happen on kubernetes

𝐑𝐨𝐮𝐧𝐝 𝟓 - 𝐌𝐚𝐧𝐚𝐠𝐞𝐫𝐢𝐚𝐥/𝐓𝐞𝐜𝐡𝐧𝐢𝐜𝐚𝐥

- Why would you be a good fit for a senior management position?
- What’s your most significant achievement so far?
- Tell me a scenario where you had critical issue and you went beyond and above to solve that issue

- Write a script

AWS experience

Database

Microservives artitectures

Upgrade activities

Automation and Deployment strategies

HTTP protocol

About SAAS

About Loginext

About cloud platforms

1. the installation and configuration part, troubleshooting skills(must have skills)

2. Hands-on with Database. (must have skills)

3. Hands-on with Microservices & HTTP. also how to increase disk space of running ec2.

4. understanding of cloud watch

5. Hands-on exp with AWS. know how to create replicas in RDS.

6. Scaling concepts and understanding of EC2, Subnet, VPC

7. Concepts on RDS.worked on a scalable environment

8. Worked on Infrastructure as a Code. Linux

9. 4.What is dif bw entry points and cmd??
5.What is the dif bw add and copy??
Open jdk 10 and 11 how u will configure in jenkins and ensure it is configured??

1)Explain what DevOps is and its key principles.

2)What is the purpose of version control, and which version control systems are you familiar with?

3)Describe the difference between continuous integration and continuous deployment.

4)Explain the concept of Infrastructure as Code (IaC) and provide examples of IaC tools.

5)How do containers differ from virtual machines, and what are the advantages of using containers in a DevOps environment?

6)What is the significance of microservices architecture in DevOps?

7)How would you set up a CI/CD pipeline? Describe the stages involved.

8)What is the role of Docker in DevOps, and how does it contribute to containerization?

9)Explain the importance of monitoring and logging in a DevOps environment. Which tools have you used for monitoring or logging?

10)How do you handle security in a DevOps pipeline, from code development to production deployment?

11)What is the purpose of configuration management, and which tools can be used for this purpose?

12)How do you ensure high availability and scalability in a DevOps setup?

13)Describe the concept of blue-green deployment and its advantages.

14)What is the role of automation in DevOps, and how have you used automation tools in your previous projects?

15)How do you approach collaboration between development and operations teams?

16)Explain the term "Infrastructure as Code" and provide a scenario where it can be beneficial.

17)Describe your experience with cloud platforms (AWS, Azure, or Google Cloud) and how you integrate them into your DevOps practices.

18)What is Jenkins, and how does it contribute to continuous integration and continuous deployment?

19)How do you manage secrets and sensitive information in a DevOps environment?

20)Can you share a challenging situation you faced in a DevOps role and how you resolved it?

