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
