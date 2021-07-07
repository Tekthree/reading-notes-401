# AWS: S3 and Lambda

## Review, Research, and Discussion


### Describe “The Cloud”
- The cloud is a term that refers to servers that are accessed over the internet, and the software and databases that run on those servers. By using cloud computing, users and companies don't have to manage physical servers themselves or run software applications on their own machines.

### What is a container (as it relates to computers and servers)?
- Like virtual machines, containers are a cloud virtualization technology. They are part of the PaaS (Platform-as-a-Service) cloud model. Virtualization for containers occurs one abstraction layer up from where it occurs for virtual machines, at the operating system level instead of at the kernel level (the kernel is the foundation of the operating system, and it interacts with the computer's hardware). Each virtual machine has its own operating system kernel, but containers on the same machine share the same kernel.

### What is auto-scaling?
- Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.

### What is bandwidth?
- The volume of information that can be sent over a connection in a measured amount of time – calculated in megabits per second (Mbps).

### How do cloud providers compute service costs?
  - Cost per Rack Unit
    * They start by calculating costs for network hardware, network infrastructure maintenance, and labor. These expenses are added together and then divided by the number of rack units a business will need for its IaaS cloud. Some of the factors that go into these costs include
   
  - Cost per GB of Virtual RAM
    * Most providers calculate the cost of CPU by determining the respective company’s cost per GB of virtual RAM,


## Document the following Vocabulary Terms

### Server Instances
- An Instance is a virtual machine which runs our workloads in the cloud. A node sever can be thought of as an instance.

### Containers
- A package of software that comes with all its code, dependencies and scripts detailing how to run it. I can normally run reliably on any computer.

### Cloud Services
- Remote computing power for helping business scale their products. 

### Cloud Architecture
- Cloud resources leveraged by business for solving problems. The Architecture lays out the all components and the relationship between them. 

### AWS
- Amazon Web Services, cloud computing services

### EC2/Beanstalk vs Heroku
- One big difference is that Heroku’s pricing takes exponential price jumps as one adds common additional features, e.g., auto-scaling, where-as AWS pricing is fairly linear. On the other hand, Heroku is generally simpler to get up and running as AWS has a fairly steep initial learning curve.

Info cited on https://www.cloudflare.com/ , https://aws.amazon.com/autoscaling/ , https://www.verizon.com/info/definitions/bandwidth/ , https://expedient.com/knowledgebase , https://codeburst.io/heroku-v-s-aws-elastic-beanstalk-1cc6f12ca3c7
