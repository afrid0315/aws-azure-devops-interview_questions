# AWS Interview Questions & Answers


#### 1. Compare AWS with OpenStack

**Answer.** OpenStack and AWS help to upload images in which AWS has EC2, and EMR Hadoop based big data. On the other hand OpenStack is designed to scale on hardware without specific requirements.

#### 2. How will you access the data on EBS in AWS ?

**Answer.** The data on EBS in AWS can be accessed by seeing the EBS ID which is present in the EC2 Web Console in the root device .The EBS Volume ID show the view of the data list in the Elastic Block Store.

#### 3. What is the boot time for an instance store backed instance ?

**Answer.** The boot time for a store backed instance in Amazon EBS-backed AMI is less than 1 minute whereas for Amazon instances store backed AMI is less than 5 minutes usually.

#### 4. Differentiate between vertical and horizontal scaling in AWS.

**Answer. Horizontal scaling**, also known as scaling out, involves adding more machines to a network or system to distribute the load across multiple devices.

Instead of increasing the power of a single machine (as in vertical scaling), horizontal scaling adds more machines to handle the increased load. Each machine operates independently, and the workload is distributed among them.

**Vertical scaling**, also known as scaling up, involves increasing the power of a single machine, such as upgrading the CPU, adding more RAM, or expanding storage capacity.

In vertical scaling, the resources of a single machine are increased to handle a higher load. This could involve upgrading the hardware components or adjusting the configurations of the existing machine.

#### 5. What is the total number of buckets that can be created in AWS by default ?

**Answer.** 100 buckets can be created in AWS by default .Additional buckets can be added up to a maximum of 1,000 buckets with some limitations.

#### 6. Differentiate between Amazon RDS, Redshift and Dynamo DB.

**Answer.** Amazon Redshift is a completely managed data warehouse service whereas dynamo DB is a NoSQL database offered as a service and Amazon RDS focus on relational database.

#### 7. What Is Amazon Machine Image (ami)?

**Answer.** An Amazon Machine Image is a packaged environment containing a software configuration in which the machine images are like templates that are configured using an application servers and OS.

#### 8. Explain Storage For Amazon Ec2 Instance.?

**Answer.** An instance store provides temporary block-level storage for the instance located on disks that are attached to the host computer.

#### 9. What Are The Security Best Practices For Amazon Ec2?

**Answer.** The Best practices for Amazon EC2 can be done by managing secure access to resources using identity federation, IAM users along with implementing the least permissive rules for a secure operating system and applications on the instance.

#### 10. Can I Vertically Scale An Amazon Instance? How? Give me details about scaling?

**Answer.** Yes. Vertically scaling of an AWS instance can be done up or down when instance size changed, and then restarted because of moving the VM to a different piece of hardware with the available resources.

About Scaling, we are having Horizontal scaling and Vertical scaling. Horizontal scaling will increase or decrease by no. of machines as  per workload requirement which is scale-in and scale-out(by using autoscaling we can automatically scale). Vertical scaling will increase or decrease its machines configurations like size, cpu, ram... It will increase or decrease its single machines configurations which is scale-up and scale-down(this done by manually by stopping machine and updating configuration as per workload and restarting machine.

#### 11. How To Use Amazon Sqs?

**Answer.** The Amazon Sqs can be used by creating a queue followed by sending message and can be used followed by deleting the queue.

#### 12. Name The Several Layers Of Cloud Computing?

**Answer.** The layers of Cloud Computing are Infrastructure as a Service (IaaS) which is the basic layer, Platform as a Service (PaaS), Software as a Service (SaaS), and Business Process Outsourcing (BPO).

#### 13. What is T-Class and M-Class in aws instance?

**Answer.** In Amazon Web Services (AWS), instance types are categorized into families, and each family is designed to meet specific use cases. The instance types are identified by letters and numbers that denote the characteristics of the instance. The most common families you mentioned are the "T-class" and "M-class" instance families:

**T-Class Instances:**
T-class instances are part of the "Burstable Performance Instances" family.
They are designed to provide a baseline level of CPU performance with the ability to burst above that baseline when needed.
These instances are suitable for applications with variable CPU usage that can benefit from the burstable performance model.
Example: T3, T3a

**M-Class Instances:**
M-class instances are part of the "General Purpose Instances" family.
They provide a balance of compute, memory, and networking resources.
M-class instances are versatile and can be used for a wide range of applications, making them a good choice for many workloads.
Example: M5, M5a, M5n, M5zn, M6g, M6gd

#### 14. How to increase disk space of running EC2?
**Answer.** To increase disk space on a running EC2 instance, you can either resize the existing EBS (Elastic Block Store) volume or attach a new EBS volume with additional capacity. After attaching or resizing, you need to extend the file system to make use of the added space. The specific steps may vary based on the operating system, but generally involve using commands like resize2fs for Linux or Disk Management for Windows.

#### 15. Why we need autoscaling?
**Answer.** Autoscaling is essential for dynamically adjusting computing resources based on demand. It ensures optimal performance, cost efficiency, and high availability by automatically scaling resources up or down in response to varying workloads. Autoscaling helps maintain a balance between resource utilization and cost effectiveness, providing scalability and resilience for applications and services in a dynamic and unpredictable environment.

#### 16. In S3 difference between public and private subnet?
**Answer.** In an Amazon S3 context, there is no distinction between public and private subnets, as S3 is a globally accessible storage service. Public and private subnets typically pertain to resources hosted in Amazon VPC (Virtual Private Cloud), and they don't directly impact the accessibility of S3 buckets. S3 buckets are accessible over the internet by default, but their access can be controlled using S3 bucket policies, IAM policies, and VPC endpoint policies. The concepts of public and private subnets are more relevant to EC2 instances and other resources within a VPC.

#### 17. VPC private linked points
**Answer.** The term "VPC Private Linked Endpoints" typically refers to AWS PrivateLink, a service that enables private connectivity between a Virtual Private Cloud (VPC) and supported AWS services or endpoints, without traversing the public internet. Private Linked Endpoints enhance security and reduce data transfer costs by allowing direct, private communication between your VPC and AWS services, such as S3, DynamoDB, or others. It enables access to these services with increased privacy and without exposing them to the public internet.

#### 18. S3 storage classes?
**Answer.** Amazon S3 offers multiple storage classes to suit different performance, durability, and cost requirements:

Standard: General-purpose storage with high durability and low latency.

Intelligent-Tiering: Automatically moves objects between two access tiers based on changing access patterns.

Standard-IA (Infrequent Access): Suitable for infrequently accessed data with lower storage costs and retrieval fees.

One Zone-IA: Similar to Standard-IA but stores data in a single availability zone for cost savings.

Glacier: Extremely low-cost archival storage with longer retrieval times.

Glacier Deep Archive: Lowest-cost archival storage for long-term retention with the longest retrieval times.

Reduced Redundancy Storage (RRS): Deprecated storage class, once commonly used for non-critical, reproducible data. It's recommended to use Standard or Intelligent-Tiering instead.

#### 19. Encryption in S3?
**Answer.** Amazon S3 provides server-side encryption options to secure data at rest:

SSE-S3 (Server-Side Encryption with S3): Amazon manages and protects keys.

SSE-KMS (Server-Side Encryption with AWS Key Management Service): Allows more control over encryption keys.

SSE-C (Server-Side Encryption with Customer-Provided Keys): Lets you manage and control encryption keys.

Encrypting data in transit is achieved through the use of SSL/TLS when accessing S3 over HTTPS.

#### 20. How to copy local file to s3 using cli?
**Answer.** To copy a local file to Amazon S3 using the AWS CLI, you can use the aws s3 cp command. 
```
aws s3 cp local-file.txt s3://your-bucket-name/
```

#### 21. About S3 bucket policy
**Answer.** An S3 bucket policy is a JSON document that defines permissions for an Amazon S3 bucket. It controls who can access the bucket and how they can access it. Key elements include specifying actions (e.g., s3:GetObject), resources (e.g., the bucket and objects), and the conditions under which the policy applies. Bucket policies are used for access control, allowing fine-grained control over who can perform specific actions on objects within the bucket.

#### 22. About S3 encryption policy
**Answer.** An S3 encryption policy refers to specifying rules within an S3 bucket policy that mandate encryption for objects stored in the bucket. This policy ensures that any data uploaded to the bucket is encrypted, either using server-side encryption provided by AWS S3 (SSE-S3, SSE-KMS, or SSE-C) or by enforcing client-side encryption before uploading to the bucket. The encryption policy enhances data security and compliance by enforcing encryption standards for data at rest in an S3 bucket.

#### 23. Write a yaml file to create a ec2 in cloud formation?
**Answer.** 
```
AWSTemplateFormatVersion: "2010-09-09"
Resources:
  MyEC2Instance:
    Type: "AWS::EC2::Instance"
    Properties:
      ImageId: "ami-xxxxxxxxxxxxxxxxx"  # Replace with your desired AMI ID
      InstanceType: "t2.micro"
      KeyName: "your-key-pair-name"     # Replace with your key pair name
```

#### 24. Difference between nginx and apache
**Answer.** Nginx and Apache are both popular web servers, but they have some key differences:

Architecture:

Apache: Processes requests using a multi-process, multi-threaded model.
Nginx: Uses an event-driven, asynchronous architecture to handle a large number of concurrent connections efficiently.
Resource Usage:

Apache: Generally consumes more memory per process.
Nginx: Typically has lower memory usage and can handle more concurrent connections with fewer resources.
Concurrency:

Apache: Uses a process-based model where each connection gets a dedicated process or thread.
Nginx: Uses an asynchronous, non-blocking model, making it more efficient in handling concurrent connections.
Modules:

Apache: Has a rich set of modules for various functionalities.
Nginx: Modules are more lightweight, and additional functionalities are often implemented as separate processes.
Configuration:

Apache: Configuration can be more complex with its .htaccess files and extensive configuration options.
Nginx: Configuration is generally simpler and more streamlined.
Use Cases:

Apache: Traditionally favored for dynamic content and shared hosting environments.
Nginx: Known for its performance in serving static content, acting as a reverse proxy, and handling high concurrency.
Choosing between Nginx and Apache depends on specific use cases and performance requirements. Often, they are used together in a complementary way, with Nginx handling static content and serving as a reverse proxy in front of Apache for dynamic content.

#### 25. Comparison between classic, network, application load balancing?
**Answer.** Load balancing in AWS offers different options, each suited for specific use cases:

Classic Load Balancer (CLB):

Operates at both the application and transport layers.
Well-suited for simple applications.
Supports HTTP, HTTPS, TCP, and SSL protocols.

Network Load Balancer (NLB):
Operates at the transport layer (Layer 4).
Designed for high-performance, low-latency, and scalable applications.
Ideal for TCP and UDP traffic.

Application Load Balancer (ALB)
Operates at the application layer (Layer 7).
Suited for modern, containerized, and microservices-based architectures.
Supports routing decisions based on content, enabling more advanced load balancing.
Key Considerations:

CLB: Basic and versatile. Suitable for general use but lacks advanced features.

NLB: Efficient for handling high-volume, low-latency traffic. Ideal for scenarios like gaming and IoT.

ALB: Provides advanced application-level routing and content-based routing. Well-suited for modern web applications and microservices architectures.

#### 26. About Amazon CloudFront?
**Answer.** Amazon CloudFront is a content delivery network (CDN) service by AWS that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, and a high level of security. It caches content at edge locations worldwide, reducing latency and providing a scalable solution for distributing content with a global reach.

#### 27. How to copy large zip file from local to s3 bucket?
**Answer.** For copying large files or directories to an S3 bucket efficiently, use the 'copy' command or aws s3 sync command. 
```
aws s3 cp yourfile.zip s3://your-bucket-name/
```
But, aws s3 sync command will be good to copy large files than copy command 
```
aws s3 sync /path/to/local/directory s3://your-bucket-name/
``` 

#### 28. What is the maximum limit of s3 storage?
**Answer.** The maximum limit for a single Amazon S3 bucket is 5 terabytes (TB) for both the total storage size and any individual object stored within the bucket. 

#### 29. Write python script for aws lambda?

#### 30. In autoscaling we have minimum capacity, max capacity and desired capacity. Is desired value is optional or mandatory to provide?
**Answer.** In Auto Scaling, the "desired capacity" value is optional to provide. If not specified, Auto Scaling will use the default desired capacity, which is often the minimum capacity. However, setting the desired capacity explicitly allows you to control the number of instances in the Auto Scaling group independently of the minimum or maximum capacities. If we specify desired value then it will defaultly start with desired value.
