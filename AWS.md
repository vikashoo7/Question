VPC
---
       * How to Create the VPC?
           Follw the below staeps
               1. subnet
               2. create an interbet gateway
               3. Attach the internet gateway to VPC
               4. create the route table to connect with IGW
                 * create the saparate route table. Do not touch the existing route table
                 * Add the rules in the route table
               5. Add the subnet to the route table

       * How to define the subnet in VPC? By which formula?

       * What is subnet?
          it is a logical sub-division of network.

       * How to communicate between the subnet?
          we can use internal IP addrress to commicated between the subnet.

       * What is NAT gateway?
          Network Address Translation (NAT) Gateway, a highly available AWS managed service 
          that makes it easy to connect to the Internet from instances within a private subnet in an AWS.
          It Must be launched in a public subnet

       * How to connect AWS network to on your own premises data center?

       * If a server is in the private Network then how it will connect to internet?
           With the help of NAT gateways, we can connect from the private network to internet.

       * What is the VPC?
          it i a  logically isolated of virtual network.
          
       * If a server is in the private Network then how it will connect to internet?
            With the help of NAT, we will able to connect the private subnet server to the Internet.
            
       * How many ip addresses  will be there for 10.0.1.0/16?
            Total number of IP Address of "10.0.1.0/16" is 2^(32-16)-2
            one is for the gateway and other is for broadcast is reserveed.
            
       * How to configure NAT route in private subnet?
            Route for NAT gateway for private Subnet
                  Destination(0.0.0.0/0) ----> Target(NAT-Gateway-Name)
                  
       * How to configure 100 of VPC which are in different  region?
        
S3
---
       * Where is S3 logs stored?
         By default, S3 logs are not enabled.
         First we need to enable to logs and then we can see the logs in the in the S3 bucket in the same region.

       * Can we mount S3 on the server?
          Yes, we can. we can use the below comamnd to mount the s3 in the linux server.
            #s3fs -o use_cache=/tmp/cache mydbbackup /s3mnt

       * How to sync between between the two S3 across the zone?
          we can use the below command to sync the s3
           #aws s3 sync s3://DOC-EXAMPLE-BUCKET-SOURCE s3://DOC-EXAMPLE-BUCKET-TARGET
       * How to sync between between the two S3 across the zone?



Load Balancer
----
       * What is load balancer?
          It is used to distribute the traffice between the servers.

       * What are the different types of ELB?
          There are 3 types of ELB:
          1. Classic load balancer
          2. Network load balancer
          3. Application load balancer
       * What is ELB?
          It is used to distribute the traffice between the servers.
       * How to configure load balancing routing?
       * How to configure the application load balancing?
    
RDS
----
       * What is the RDS?
          This is the AWS relational database service.

       * What is the database you use in AWS?
       * What is the difference between Amazon RDS and stand alone MySQL database?

Security, Certificate
----
      * How to block a specific port in AWS?
          By default, all the ports is denied. So it is not possible to block a specific port in the AWS.
      * Where we can keep the ssl certificate in the AWS?
          we can use  AWS Certificate Manager (ACM) to impport or keep the certificate.

Route 53
---
    * What is route 53 does?
       Route53 is a AWS DNS service.
   
EC2, Autoscalling, EBS, CDN
---
    * How to create AWS ec2 instances using command line?
    * What is the EC2?
    * What are the autoscaling type?
    * How to not destroy a specific ec2 instance in automating?
    * What is the CDN?
    * Where to see the logs for EC2 instance?
    * What is EBS?
          it is hight performace block-storage service.
          
    * How to extend a EBS volume from 50 to 500G.
          we cannot extend the EBS diretly. 
          we can take the snapdort of 500G disk and 
          then provission 500G disk. 
          Extract the data from the snap sort then moont the 500G.

AMI
---
      * What type of images you use in AWS?
      * What is the difference in community and Market place AMI in AWS?

IAM
---
      * IaM block for Json block for giving the s3 permission to the user?

Monitoring
-----
      * What is the difference  between cloudwatch and cloudtrail?
      * What is log group in cloud watch?

Email Service
-----
      * What is SNS?
  
General
---
    * What is the difference in EBS and S3?
       EBS is block storage and S3 is Object storage

    * What is the difference between NAT and loadbalancer?
        NAT is used to connect with internet. Loadbalancer distribute the traffice between the servers.
        
    * Explain 3 tire architecture in AWS?
    * What are the AWS components you have worked on?
    * How to configure postfix in AWS?
    * What is the difference in later 7 and layer 5?






