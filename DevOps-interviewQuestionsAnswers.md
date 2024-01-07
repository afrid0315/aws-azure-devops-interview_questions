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

How to find thread dump of java application?
**Answer.** To find a thread dump of a Java application:
- Identify the Java process ID (PID) using jps or ps -ef | grep java.
- Use jstack command: jstack <PID> > thread_dump.txt.
- The thread dump is saved in the specified file (thread_dump.txt), revealing the state of all threads in the Java application.


- What is ctime and mtime in linux?
ctime (change time):

Represents the last time metadata of a file (permissions, ownership) was changed.
Altered when the file's metadata is modified.
mtime (modification time):

Indicates the last time the content of a file was modified.
Changes when the file's actual data is updated.
Both timestamps are part of a file's metadata and can be viewed using the stat command.


- Why nohup and & are used?
- nohup:

Prevents a command from being terminated when the terminal is closed.
Example: nohup command &
& (ampersand):

Runs a command in the background, allowing the terminal prompt to be used for other commands.
Example: command &
Together (nohup command &), they allow a command to run in the background and persist even if the terminal session is closed.


- Write a docker file to copy a file from the system to container with a volume mount?
**Answer.**
```
FROM ubuntu:latest
# Create a directory in the container
WORKDIR /app
# Copy a file from the host system to the container
COPY ./localfile.txt /app/
# Define a volume mount
VOLUME /app/data
# Set the working directory
WORKDIR /app/data
```

- What are ansible roles and what are its advantages?
Using roles enhances the readability, scalability, and maintainability of Ansible playbooks, making automation projects more efficient.

Round 3 [ Technical ]
- Write a shell script to seperate the number of alphabets, numbers, alpha numeric chars from a file
- What are the differenet grouping of ansible inventory files
- How the port forwading is done in docker
- What is docker compose and differenet types of docker networks
- What is the container life cycle in docker
- Write a ansible plabook to deploy an application and check whether the app url is up or not

Round4/5 [ Managerial ]
- Design the 3 tier architecture for your telecommunications project
- You are in the production oncall support and you get a alert where one of the system CPU is spiking up what measures would you take
-Your team mate is not coping up with tasks being a lead how will you support and guide him

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

