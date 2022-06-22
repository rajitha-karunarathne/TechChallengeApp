Servian Technical Challenge.

Have implemented and tested out the following solution for this technical challenge.

I’m more preferring to use Amazon Web Services as the Cloud Service Provider and since this is a container-based application and have to consider the high availability, scalability and Infrastructure, network layer security factors and also to fully utilize the cloud capabilities thought to use the following AWS Services for this.

1.	Tech Stack Used for the Solution:

•	Cloud Service Provider: AWS
•	Container Orchestration Service: ECS Fargate
•	Data Base: RDS PostgreSQL 
•	Load Balancer: ALB
•	IaC : AWS CloudFormation
•	Version Control and Source Code Management + CI/CD : github.com
•	Repository URL: https://github.com/rajitha-karunarathne/TechChallengeApp

2.	CFT Template Sequence:

Following CFTs been used to deploy the above Infrastructure Setup in to an Empty AWS Account, which can be founded in the above mentioned repository path -> https://github.com/rajitha-karunarathne/TechChallengeApp/tree/master/infrastructure

I.	Servian-VPC.yml : To Deploy the VPC , Subnets , Internet Gateway , NAT Gateway , Route tables for the solution.
II.	Servian-IAM.yml : To Deploy the necessary policy permission to run the solution.
III.Servian-Cluster.yml : To Deploy the ECS cluster for the solution.
IV.	Servian-DB.yml : To Deploy the RDS PostgreSQL Database for the solution.
V.	Servian-Task-Service.yml: To Deploy the ECS Task and Service to run the Servian application container.


3.	Deployment Steps:

Prerequisite: 
•	Fork or clone the repo -> https://github.com/rajitha-karunarathne/TechChallengeApp
•	Fresh / Empty AWS account with Administrator / root user access.

1.	Crete an IAM User (Preferably with Admin access) and by allowing only the AWS programmatic access and download the credential file. (Do not share this with anyone else).

2.	Add the Access key ID and Secret access key to the Github secrets of the above repository settings. 
 Use the naming as, AWS_ACCESS_KEY_ID and AWS_SECRET_ACCESS_KEY

3.	Select the Github Actions and then “Deploy Servian Application Infrastructure” and Run the Workflow, Give some time to Deploy the full infrastructure setup.

4. If all goes well and application fully deployed you will be able to access the application by using the URL given in the "Print Servian Application URL" section.



 

