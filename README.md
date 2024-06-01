# Project Name
Multi-Tier Web Application (Re-Architecting)

## Brief description of the project
A web application running on a AWS EC2 Instances using the lift & shift strategy. This strategy will Re-Architecting using all AWS Services.

## AWS Services
1. Beanstalk => VM for Tomcat
2. Beanstalk => Nginx LB Replacement
3. Beanstalk => Automation for VM Scaling
4. S3/EFS => Storage
5. RDS Instance => Databases
6. ElastiCache => Memcached Replacement
7. ActiveMQ => RabbitMQ Replacement
8. Route 53 => DNS
9. CloudFront => Content Delivery Network

### Flow of Execution:
1. Login to AWS Account
2. Create Key Pairs
3. Create Security Groups
4. Launch RDS, ElastiCache, ActiveMQ
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
![LiftAndShift](LiftAndShift.png)
