# Project Name
Multi-Tier Web Application

## Brief description of the project
A web application running on a local machine. Using the lift & shift strategy, web application will be migrated to AWS Cloud.

1. Nginx => Web Service
2. Tomcat => Application Server
3. RabbitMQ => Broker/Queuing Agent
4. Memcache => DB Caching
5. MySQL => SQL Database

## Installation
Setup in AWS Services

1. EC2 Instances => VM for Tomcat, RabbitMQ, Memcache, MySQL
2. Elastic Load Balancer => Replacement for Nginx
3. Autoscaling => Automation for VM Scaling
4. S3/EFS Storage => Shared Storage
5. Route 53 => Private DNS Service

### Flow of Execution:
1. Login to AWS Account
2. Create Key Pairs
3. Create Security Groups
4. Launch Instances
5. Update IP to name mapping in Route 53
6. Build Application from source code
7. Upload to S3 bucket
8. Download artifact to Tomcat EC2 Instance
9. Setup ELB with HTTPS [Certificate from ACM]
10. Map ELB Endpoint to Website name in DNS provider
11. Verify
12. Build Autoscaling Group for Tomcat Instances.

## Credits
Special thanks to Sir Imran Teli from Udemy, He's the owner of this project.

## AWS Diagram
![Lift&Shift](Lift&Shift.png)
