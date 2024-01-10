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

#### 10. Can I Vertically Scale An Amazon Instance? How?

**Answer.** Yes. Vertically scaling of an AWS instance can be done up or down when instance size changed, and then restarted because of moving the VM to a different piece of hardware with the available resources.

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
