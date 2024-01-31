# Jenkins Interview Questions & Answers

#### 1. Jenkins design and integration with various tools? 
**Answer.** Jenkins is designed for continuous integration and supports integration with various tools through plugins. Its modular architecture allows seamless integration with version control systems, build tools, deployment tools, and testing frameworks. Jenkins pipelines can be configured to automate the entire software delivery process, from code commit to deployment, making it a versatile tool for DevOps practices.

#### 2. Write a Jenkinsfile for declararive pipeline
**Answer.** 
```
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
```

#### 3. Jenkins pipeline to build and run container nginx?
**Answer.** 
```
pipeline {
    agent any

    stages {
        stage('Build and Run Nginx Container') {
            steps {
                script {
                    // Build Nginx Docker image
                    sh 'docker build -t my-nginx-image .'
                    sh 'docker run -d -p 8080:80 --name my-nginx-container my-nginx-image'
                }
            }
         }
     }
}
```

#### 4. Jenkins piepline script to deploy nginx application?
**Answer.** 
```
pipeline {
    agent any

    environment {
        NGINX_CONTAINER_NAME = 'my-nginx-container'
        NGINX_IMAGE_NAME = 'my-nginx-image'
    }

    stages {
        stage('Build and Deploy Nginx Application') {
            steps {
                script {
                    // Build Nginx Docker image
                    sh 'docker build -t $NGINX_IMAGE_NAME .'

                    // Stop and remove existing Nginx container if running
                    sh "docker stop $NGINX_CONTAINER_NAME || true"
                    sh "docker rm $NGINX_CONTAINER_NAME || true"

                    // Run Nginx container
                    sh "docker run -d -p 8080:80 --name $NGINX_CONTAINER_NAME $NGINX_IMAGE_NAME"
                }
            }
        }
    }

    post {
        success {
            echo 'Nginx Application deployed successfully!'
        }
        failure {
            echo 'Failed to deploy Nginx Application. Check the pipeline logs for details.'
        }
    }
}
```

#### 5. Write a jenkins file to get the version of java in instance?
**Answer.** 
```
pipeline {
    agent any

    stages {
        stage('Get Java Version') {
            steps {
                script {
                    // Run command to get Java version
                    def javaVersion = sh(script: 'java -version 2>&1 | grep version | awk \'{print $3}\'', returnStdout: true).trim()

                    // Print Java version
                    echo "Java Version: $javaVersion"
                }
            }
        }
    }
} 
```

#### 6. Master and node concept in jenkins?
**Answer.** Master: The Jenkins master is the main server responsible for managing jobs, distributing builds to agent nodes, and coordinating the overall build process. It hosts the Jenkins web interface and handles the primary configuration.

Node: Nodes, also known as agents or slaves, are additional machines that perform the actual build jobs. They receive tasks from the master, execute the builds, and report the results back. Nodes can be set up on different environments, allowing parallel execution of builds and expanding Jenkins' capacity.

#### 7. About Jenkins Shared Library?
**Answer.** Jenkins Shared Library:

Definition: A reusable and centralized collection of Groovy scripts and functions that can be shared across multiple Jenkins pipelines.

Purpose: Promotes code reuse, standardization, and maintainability in Jenkins pipelines by encapsulating common logic and functionality.

Implementation: Typically stored in version control systems (e.g., Git) and loaded dynamically into Jenkins pipelines.

Benefits: Reduces duplication of code, enforces best practices, and facilitates updates across all pipelines using the shared library.

#### 8. How to save only last 5 builds of jenkins job?
**Answer.** In Jenkins, you can use the "Discard Old Builds" feature to limit the number of builds to keep. To save only the last 5 builds for a Jenkins job:

Open the Jenkins job configuration.
Under the "Build Triggers" section, find and enable the option "Discard Old Builds."
Set the "Max # of builds to keep" to 5.
This configuration ensures that only the last 5 builds are retained, and older builds are automatically discarded. Adjust the settings according to your requirements.

#### 9. If you forget Jenkins password, how would you login back?
**Answer.** To regain access to Jenkins if you forget the password:

Navigate to the Jenkins home directory.
Locate the secrets/initialAdminPassword file.
Retrieve the password from the file.
Access the Jenkins web UI and use the password for setup.
Follow on-screen instructions to complete the setup and create a new admin user.

#### 10. How to create slaves in jenkins?
**Answer.** Creating Slaves in Jenkins:

- Navigate to Jenkins Dashboard: Log in to the Jenkins web interface.
- Go to Manage Jenkins: Click on "Manage Jenkins" in the left-hand menu.
- Manage Nodes and Clouds: Select "Manage Nodes and Clouds."
- Click on "New Node": Click on the "New Node" or "New Agent" button.
- Configure Node Details: Enter a name, select the node type (Permanent or Dumb), and specify connection details.
- Save: Save the configuration, and Jenkins will now be able to use the newly created slave for distributed builds.

#### 11. How to create HA in jenkins?
**Answer.** Creating High Availability (HA) in Jenkins:

Master-Slave Architecture: Implement a master-slave architecture with Jenkins, where the master distributes builds to multiple slave nodes.

Load Balancing: Use load balancing techniques to distribute incoming traffic across multiple Jenkins masters for improved availability.

Database Replication: Employ database replication for Jenkins configuration data to avoid a single point of failure.

Artifact Repository: Use a distributed artifact repository to store build artifacts, ensuring redundancy and availability.

Backup and Restore Procedures: Implement regular backup and restore procedures to recover from failures quickly.

Containerization: Consider containerization (e.g., Docker) to encapsulate Jenkins components, making it easier to scale and deploy in a highly available manner.





