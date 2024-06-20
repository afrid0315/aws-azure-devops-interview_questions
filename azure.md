## Azure Interview Q/A

#### 1. What exactly you have done in your current project?

Answer- 

#### 2. How many pipeline you have created?

Answer- I have experience creating and managing multiple CI/CD pipelines to automate the software delivery process. The exact number depends on the projects I've worked on. I've implemented pipelines using popular CI/CD tools like Jenkins. These pipelines typically include stages for building, testing, and deploying applications. I emphasize the importance of version control integration, automated testing, and deployment strategies to achieve efficient and reliable software delivery.

#### 3. How many environments do you have in your project?

Answer- In my current project, we have implemented a comprehensive environment strategy to support various stages of the development lifecycle. We typically maintain three main environments:

**Development Environment:**

Used by individual developers for coding and initial testing. It mirrors the production environment in terms of infrastructure and configuration.

**Testing Environment:**

A shared environment for integration testing, system testing, and user acceptance testing. It closely resembles the production environment to identify issues before deployment.

**Production Environment:**

The live environment where the application is accessible to end-users. We follow a robust deployment process, including automation and monitoring, to ensure smooth and reliable production releases.
Additionally, we may have specialized environments for specific purposes, such as staging for final pre-production environment.

#### 4. While deployment, how exactly you have maintained the approval process?

**Answer-** In our deployment process, maintaining a robust approval workflow is crucial for ensuring controlled and reliable releases. We have implemented the following strategies:

**Manual Approvals:**

For critical environments such as production, we incorporate manual approval gates. Before proceeding with the deployment, designated stakeholders or team leads review the proposed changes and explicitly approve or reject them.

**Automated Testing Gates:**

We integrate automated testing gates within the deployment pipeline. The deployment progresses only if all automated tests pass successfully. This ensures that the code meets quality standards before reaching production.

**Integration with Collaboration Tools:**

To streamline communication and approvals, we leverage collaboration tools such as Slack or Microsoft Teams. Deployment notifications are sent to relevant channels, allowing team members to stay informed and providing a platform for quick approval or discussions.

**Version Control Integration:**

Our deployment process is tightly integrated with version control systems. Changes are tracked, and the deployment pipeline automatically triggers approvals based on the configured criteria.

**Rollback Plans:**

Before each deployment, we define and communicate rollback plans. In case of unforeseen issues post-deployment, an immediate rollback can be executed with minimal impact.

#### 5. Do you know Azure board, or have you worked on Azure board?

**Answer** Azure Boards is a project management tool within Azure DevOps for Agile teams. It facilitates work item tracking, Agile planning (Scrum, Kanban), and integrates seamlessly with Azure Pipelines for CI/CD workflows. It supports collaboration, provides analytics, and is scalable for teams of all sizes. (similiar tool like jira)

#### 6. How is your team managing the assigned work?

**Answer**

#### 7. What is the way to analyze the static code?

**Answer** Analyzing static code involves using automated tools to review source code for potential bugs, security vulnerabilities, and adherence to coding standards without executing the code. This process helps identify issues early in development, ensuring code quality, security, and compliance with best practices.

#### 8. What is the process to deploy a .net core application in azure devops?

**Answer** To deploy a .NET Core application using Azure DevOps, follow these steps:

1. **Build Pipeline**:
   - Create a build pipeline in Azure DevOps using a YAML file or the visual editor.
   - Use a build agent with necessary SDKs installed for .NET Core.
   - Define steps to restore packages (`dotnet restore`), build (`dotnet build`), and publish (`dotnet publish`) your .NET Core application.

2. **Artifact Publishing**:
   - Publish build artifacts such as compiled binaries and necessary files using the `PublishBuildArtifacts` task.

3. **Release Pipeline**:
   - Create a release pipeline in Azure DevOps to deploy your application.
   - Add an artifact source linked to the build pipeline artifact.

4. **Environment Configuration**:
   - Define deployment stages and target environments (e.g., development, staging, production).
   - Configure environment-specific settings such as connection strings or environment variables.

5. **Deployment Tasks**:
   - Use deployment tasks like Azure App Service Deploy task to deploy your .NET Core application to Azure App Service.
   - Configure task parameters like Azure subscription, App Service name, and package or folder path to deploy.

6. **Trigger and Approvals**:
   - Set triggers for automatic deployments triggered by artifact updates.
   - Optionally, configure approval gates for manual validations before deployments to production environments.

7. **Monitoring and Validation**:
   - Monitor deployment progress and logs in Azure DevOps.
   - Validate application functionality post-deployment to ensure successful deployment.

By following these steps, you can automate the deployment of your .NET Core application using Azure DevOps, ensuring efficient and consistent deployment processes.

#### 9. What is the process to deploy a angular application in azure devops?

**Answer** To deploy an Angular application using Azure DevOps, follow these steps:

1. **Build Pipeline**:
   - Create a build pipeline in Azure DevOps using YAML or the visual editor.
   - Use a build agent with Node.js installed.
   - Define steps to install dependencies (`npm install`), build the Angular app (`ng build --prod`), and archive artifacts (`publish`).

2. **Artifact Publishing**:
   - Publish build artifacts such as compiled Angular application files (`dist` folder) using the `PublishBuildArtifacts` task.

3. **Release Pipeline**:
   - Create a release pipeline in Azure DevOps to deploy your Angular application.
   - Add an artifact source linked to the build pipeline artifact.

4. **Environment Configuration**:
   - Define deployment stages (e.g., development, staging, production).
   - Configure environment-specific settings like API endpoints or environment variables.

5. **Deployment Tasks**:
   - Use deployment tasks like Azure App Service Deploy task to deploy the Angular application to Azure App Service.
   - Configure task parameters such as Azure subscription, App Service name, and package or folder path (`$(System.DefaultWorkingDirectory)/<ArtifactName>`).

6. **Trigger and Approvals**:
   - Set triggers for automatic deployments triggered by artifact updates.
   - Optionally, configure approval gates for manual validations before deployments to production environments.

7. **Monitoring and Validation**:
   - Monitor deployment progress and logs in Azure DevOps.
   - Validate application functionality post-deployment to ensure successful deployment.

By following these steps, you can automate the deployment of your Angular application using Azure DevOps, ensuring efficient and consistent deployment processes.

#### 10. What is the service connection? And how do we create that?

**Answer** Service Connection: In Azure DevOps, a service connection is a secure link that allows pipelines and releases to connect with external services or Azure resources. It securely stores credentials and authentication details for seamless integration.

Creating a Service Connection:

Navigate to Project Settings in Azure DevOps.
Go to Service connections under Pipelines.
Click New service connection and select the type (e.g., Azure, GitHub).
Follow the prompts to authenticate and configure the connection.
Save the service connection for use in your pipelines and releases.


#### 11. What is the difference between service connection and service principal?

**Answer** Service Connection (Azure DevOps):

Purpose: Used in Azure DevOps for securely integrating with external services or Azure resources within CI/CD pipelines.
Functionality: Stores credentials and authentication details for pipeline tasks like deploying to Azure or interacting with GitHub.

Service Principal (Azure / AWS):

Purpose: Represents an identity used for authentication and access management across Azure or AWS environments.
Functionality: Manages permissions (RBAC) for applications or services to access resources within Azure subscriptions or AWS accounts.
Key Difference:

Scope: Service connections are specific to Azure DevOps for pipeline integration. Service principals are broader, managing identities and access across Azure or AWS.

#### 12. Are you aware with Azure resources for example App services and Functional Apps?

**Answer** 
**App Services**: Azure App Service is a platform-as-a-service (PaaS) offering for hosting web applications, RESTful APIs, and mobile backends. It provides automatic scaling, high availability, and easy integration with Azure services.

**Azure Functions**: Azure Functions is a serverless compute service that lets you run event-triggered code without managing infrastructure. It scales automatically and integrates with various Azure services and third-party services.

