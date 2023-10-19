# Re-architecting Web Application on cloud PAAS & SAAS
	
* Architecture of AWS Services for the project : EC2 instance, ELB, Autoscaling, EFS/S3 for storage, Elastic Cache, Active MQ, Route53, CloudFront. 

* Re-architecting web services of AWS cloud for multi-tier web application stack, to boost agility or improve business continuity.

* Flow of execution:

1. Login to aws account
2. Create Key pair for beanstalk instance login
3. Create Security Group for Elasticcache, RDS &ActiveMQ Create
4. RDS
5. Amazon Elastic Cache > Amazon Active MQ
6. Create Elastic Beanstalk Environment
7. Update SG of backend to alow traffic from Bean SG Update SG of backend to alow internal traffic
8. Launch Ec2-Instance for DB Initializing
9. Login to the instance and Inititialize RDS DB
10. Change healthcheck on beanstalk to /login Add 443 https Listner to ELB
11. Build Artifact with Backend Information
12. Deploy Artifact to Beanstalk Create CDN with ssl cert
13. Update Entry in GoDaddy DNS Zones Test the url
