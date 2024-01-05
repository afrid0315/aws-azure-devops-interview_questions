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

Round 1 [ Technical ]

- Jenkins design and integration with various tools
- Automation done in your projects as a devops engineer
- How to trobleshoot the linux server if there is any CPU or memory issue
- Write the ansible playbook the show the handlers
- What are logical volumes in linux and how to create
- What is swap and buffer in linux
- How do you change the root password in linux system
- How to monitor the linux fi;es for any changes

Round 2[ Technical ]
- What is ctime and mtime in linux
- Why nohup and & are used
- How to find thread dump of java application
- How the ansible variable precedence happens
- Write a docker file to copy a file from the system to container with a volume mount
- What are xargs in linux
- What are ansible roles and what are its advantages

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
