## DevOps Interview Questions & Answers

#### 1. How do you handle issues at the production level?

**Answer.** At the production level, I prioritize proactive monitoring and alerting to catch issues early. I follow incident response procedures, involve relevant stakeholders promptly, leverage logging and metrics for diagnosis, and implement a robust rollback strategy. Continuous improvement through post-incident reviews ensures lessons are learned and applied to prevent future issues.

#### 2. How do you support/collaborate with various teams? 

**Answer.** I foster open communication, establish clear channels for collaboration, and regularly engage with cross-functional teams. I actively participate in meetings, utilize collaboration tools, and ensure that everyone is aligned on goals and timelines. Additionally, I proactively share information, offer assistance, and seek input to strengthen overall teamwork.

#### 3. How can our self-owned databases, infrastructure better than cloud migrated services?

**Answer.** Maintaining our own databases and infrastructure offers greater control over security, customization, performances. It allows for tailored solutions to specific needs, avoiding reliance on third party providers. However, Cloud migration provides scalability, cost-efficiency and automated maintenance. The choice depends on your organization's priorities, resources and long-term strategies.

#### 4. Write the grovy script for retry option in jenkins?
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
#### 5. What is shift Left concept?
**Answer.** Shift left is a concept in software development and DevOps that emphasizes moving tasks, processes, and responsibilities earlier in the software development lifecycle (SDLC). The goal of shifting left is to identify and address issues as early as possible, thereby reducing the cost and effort of fixing them later in the development process.

#### 6. How to find thread dump of java application?
**Answer.** To find a thread dump of a Java application:
- Identify the Java process ID (PID) using jps or ps -ef | grep java.
- Use jstack command: jstack <PID> > thread_dump.txt.
- The thread dump is saved in the specified file (thread_dump.txt), revealing the state of all threads in the Java application.

#### 7. Design the 3 tier architecture for your telecommunications project?
**Answer.** The 3-tier architecture for our telecommunications project comprises three layers: the presentation layer for user interface, the application layer for business logic, and the data layer for storage and retrieval. This design ensures modular scalability, separation of concerns, and efficient management of telecommunications services.

#### 8. Explain what DevOps is and its key principles?
**Answer.** DevOps is a cultural and collaborative approach to software development and IT operations, aiming to improve communication, collaboration, and automation across the entire software delivery lifecycle. Key principles include automation for efficiency, continuous integration/continuous deployment (CI/CD) for faster delivery, infrastructure as code (IaC) for consistent environments, and a culture of collaboration and shared responsibility between development and operations teams.

#### 9. What is the significance of microservices architecture in DevOps?
**Answer.** Microservices architecture in DevOps promotes the development of small, independent services that can be deployed, scaled, and updated individually. This fosters agility, allowing teams to release features faster, scale components independently, and improve fault isolation. It aligns well with DevOps practices, facilitating continuous integration, continuous delivery, and efficient collaboration between development and operations teams.

#### 10. How do containers differ from virtual machines, and what are the advantages of using containers in a DevOps environment?
**Answer.** Containers differ from virtual machines in that they share the host OS kernel, making them lightweight and faster to start. Virtual machines, on the other hand, emulate an entire OS. Container advantages in DevOps include faster deployment, efficient resource utilization, consistency across environments with Docker images, and easier scalability. Containers also promote isolation, facilitating microservices architecture, and enhance portability across various cloud and on-premises environments.

#### 11. What is the use of Jira tool?
**Answer.** Jira is a project management and issue tracking tool that helps teams plan, track, and manage their work. It provides features for tasks such as project management, bug tracking, and agile development. Jira facilitates collaboration among team members and enables them to organize and prioritize their work effectively.

#### 12. About pom.xml?
**Answer.** The pom.xml (Project Object Model) file is the configuration file used by Maven, a build automation and project management tool in Java. It defines the project's structure, dependencies, plugins, and various settings required for building, testing, and packaging Java applications.

#### 13. Maven lifecycle? 
**Answer.** Clean Lifecycle:
clean: Removes target directory, cleaning up artifacts from previous builds.

Default Lifecycle:
validate: Checks if the project is correct.
compile: Compiles the source code.
test: Runs tests.
package: Packages compiled code into a distributable format.
install: Installs the packaged artifact into the local repository.
deploy: Copies the final package to the remote repository.

Site Lifecycle:
site: Generates project documentation.

#### 14. Delivery vs deployment?
**Answer.** Delivery is the process of making a software application available for use or testing, while deployment is the actual installation and release of the software into a target environment for end-users. In simpler terms, delivery is about preparing the software for deployment, and deployment is about putting the software into production.

#### 15. About Sticky session?
**Answer.** Sticky sessions, also known as session affinity or session persistence, refer to a mechanism in load balancing where a server consistently handles requests from the same client. This is typically achieved by associating a user's session with a specific server, ensuring that subsequent requests from that user are directed to the same server. Sticky sessions are commonly used to maintain session-related data and stateful connections in web applications.

#### 15. Meta data vs user data?
**Answer. Metadata:** Describes and provides information about other data. It's data about data. For example, file metadata may include information like file size, creation date, or authorship.

**User Data:** The primary data generated or managed by users. For instance, the content of a document, the pixels in an image, or the entries in a database are considered user data.

#### 16. When i issue mvn install what all things happen in background?
**Answer.** 'mvn install' compiles, tests, packages, and installs the project artifacts into the local Maven repository, making them available for other projects.

#### 17. High level about DR.
**Answer. Disaster Recovery (DR):**

Definition: A set of strategies and procedures to recover and protect a business IT infrastructure in the event of a disaster.

Objectives: Minimize downtime, data loss, and ensure business continuity by having plans in place for potential disasters.

Components: Typically involves backup systems, offsite storage, replication, and procedures to restore critical systems and data.

Key Considerations: Identifying critical systems, defining recovery time objectives (RTO) and recovery point objectives (RPO), and regular testing to ensure effectiveness.

#### 18. Difference between Maven install package and maven clean package?
**Answer.** mvn clean package is used to firstly clean the existing build artifact and packages the project, create the distributable format like (jar, war..)
mvn install package is also going to do all the steps mvn clean package does. But, additionally it will also install the project artifacts into the local maven repository for use by other local projects.

#### 19. What is sonarqube? what exactly it will do can you explain how it will analyse the code?
**Answer.** SonarQube is an open-source platform for continuous inspection of code quality. It analyzes source code to detect code smells, bugs, and security vulnerabilities. SonarQube provides insights into the overall health of your codebase, helping teams maintain code quality standards. It employs static code analysis, checking for issues without executing the code. The analysis results are presented through a web interface, allowing teams to prioritize and address code quality issues.

#### 20. What is the difference between SonarQube and Checkmarx CxSAST & CxSCA?
**Answer.** SonarQube is used for ensuring code quality, and CheckMarx is used for ensuring the security of a system running that code.

SonarQube looks at several areas, including the code coverage percentage of unit tests of the code, duplication percentages, and also code quality issues found through static analysis of the code.

CheckMarx, on the other hand, just analyzes the flow of the code and the inputs and outputs. It looks for situations where inputs that could have been provided by an end user are used directly to control behavior, and other "attack vectors".


#### 21. Your company is planning to implement a disaster recovery (DR) strategy for its critical services hosted on AWS. Describe the steps you would take to design and implement a robust DR plan, including backup strategies, failover mechanisms, and testing procedures.
**Answer.** 
Assess Requirements: Identify critical services and risks.

Define Objectives: Determine RTO and RPO for each service.

Backup Strategies: Automate backups using AWS services (RDS, EBS, S3).

High Availability: Deploy services across multiple Availability Zones (Multi-AZ) and use auto-scaling.

Failover Mechanisms: Utilize AWS Route 53 for DNS failover and database replication across regions.

Testing: Schedule regular DR tests, simulate failures, and update the plan accordingly.

Monitoring and Training: Implement monitoring (CloudWatch), alerting, and ensure personnel are trained.

Documentation: Maintain updated documentation compliant with regulations (GDPR, HIPAA).

Continuous Improvement: Review and update the DR plan based on changes and lessons learned.

#### 22. When should we use EBS and EFS while mounting PVC in Kubernetes?
**Answer:** If your storage needs to be accessed by a single pod, then use AWS EBS or Azure Disks. EBS volumes can only be attached to a single EC2 instance at a time, which makes them suitable for single-pod access. On the other hand, if your storage needs to be accessed by multiple pods across different nodes or the same node, then use AWS EFS or Azure Files. EFS provides a shared file system that can be mounted simultaneously by multiple pods, making it ideal for distributed applications or shared storage use cases.

#### 23. About SAST & DAST?

#### 24. About Self introduction?
**Answer.** "Hello, my name is [Your Name], and I am a DevOps engineer with over [X] years of experience in the industry. I started my career as a system administrator, which gave me a strong foundation in managing and maintaining IT infrastructure. Over the years, I transitioned into DevOps because I am passionate about automation, continuous integration/continuous deployment (CI/CD), and improving the software development lifecycle.

In my previous roles, I have worked extensively with tools such as Docker, Kubernetes, Jenkins, Ansible, and Terraform. I am particularly skilled in setting up CI/CD pipelines, automating infrastructure provisioning, and managing container orchestration platforms.

One of my notable projects was at [Previous Company], where I led the migration of our monolithic applications to a microservices architecture using Kubernetes. This project not only improved our system's scalability and resilience but also reduced deployment times by 50%.

Currently, I am working at [Current Company], where I am responsible for maintaining our CI/CD pipeline, managing cloud infrastructure on AWS, and ensuring the overall reliability and performance of our systems.

I am excited about the opportunity at [Company You Are Applying To] because I admire your commitment to innovative solutions and continuous improvement. I believe my experience and skills align well with the requirements of this role, and I am eager to contribute to your team's success."

#### 25. On which product you worked for?
**Answer.** In my role as a DevOps engineer working on a healthcare project, I was involved in supporting the infrastructure and deployment pipelines for [insert the specific application or service here, such as a healthcare data platform, patient management system, or clinical trial management tool]. My responsibilities included automating CI/CD pipelines, ensuring compliance with healthcare regulations (like HIPAA), monitoring and optimizing the cloud infrastructure, and collaborating with the development team to ensure seamless and secure deployments. My work directly contributed to improving the efficiency and reliability of the product."

If you want to customize this further with the specific product details, you can insert the name or description of the application you worked on.

1) Could you Please Introduce yourself Briefly about your background and your project ?
2) What Does DevOps Means and how DevOps is Different from Other Department in IT Industry ?
3) What Happen when DevOps comes in IT Industry ?
4) Could you please Explain me About your last project have you worked on and what was you roles and responsibility ?

🚀 CI/CD & Pipeline Architecture
✅ How would you implement progressive delivery (canary + feature flag) in Azure DevOps?
✅ How do you ensure secure and auditable deployments in a multi-tenant CI/CD setup?
✅ What is pipeline templating in GitLab or Azure DevOps and how do you reuse it across teams?
✅ How do you trigger pipelines across repositories (cross-repo triggers) securely?

🚀 Containers & Runtime Security
✅ What steps would you take to harden a Docker image for production?
✅ Explain how to use Docker BuildKit for optimized builds.
✅ How do you prevent secret leakage during image builds or container execution?
✅ What’s the impact of running containers with --privileged and how do you mitigate it?

🚀 Kubernetes & Platform Operations
✅ How would you design a resilient multi-AZ AKS cluster with custom VNETs?
✅ What are PodDisruptionBudgets, and how do they affect high availability?
✅ Explain how to use Kyverno or OPA Gatekeeper for Kubernetes policy enforcement.

🚀 GitOps & Infra-as-Code
✅ How do you manage drift detection in ArgoCD or FluxCD?
✅ What’s the difference between kustomize and Helm, and when would you use each?
✅ How do you structure Terraform for scalable multi-team projects (modules vs workspaces)?

🚀 Azure & Cloud-Native Infrastructure
✅ How do you manage Azure Policy for compliance across subscriptions?
✅ What’s your approach to setting up private AKS clusters with secure ingress?
✅ How would you handle shared services (e.g., Key Vault, DNS, Monitoring) across projects in Azure?

🚀 Observability & Incident Response
✅ How would you detect and alert on memory leaks in Kubernetes pods?
✅ What are the key metrics you would monitor for a customer-facing API?
✅ How do you correlate logs, traces, and metrics using Azure Monitor or OpenTelemetry?

🚀 Automation & Scripting
✅ Write a Bash script to verify if Kubernetes pods are restarting frequently and alert if >5 restarts.
✅ How would you use Python to automate tagging and backup across multiple Azure resource groups?
