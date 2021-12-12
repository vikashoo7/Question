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
            How to peer the 2 VPC?
            How to design the VPC echo system?
            What is the difference between NACL and route table?
            How to connect 2 VPC?
            What is transite gateway?
            How to configure aws backup policy?
            How to configure VPN?
            How to connect 2 VPC with using peering?
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
            How to transfer 50tb Data in Aws?
            What are the different type of s3 bucket?
            How to access the S3 bucket in the difference account?
            How to set the permissions for S3 bucket. So that no one can delete file?




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
       How to configure url based routing in the lb?
            How to configure algorithm in the lb?
       What are different routing protocal in load balancer?

    
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
    How route53 route the traffic?
   
EC2, Autoscalling, EBS, CDN
---
    * How to create AWS ec2 instances using command line?
    How to copy a snapshot from one account to another in AWS?
      What are types of EBS in AWS?
      How to transfer 50tb Data in Aws?
      What is the rate of iops in G2?
      What is the life cycle of the instances in autoscaling?
            What are the autoscaling  type?
      What is target group?
      How to configure autoscalling?
      What spot instances? What is its advantages or disadvantages?
      When we are increasing the server resources,  do this required down time.?
      What is spot instances and reserved instances?
      How to access EC2 in a different VPC?

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
      * What is the difference  in AMI and snapsort
      How I can provide the access to the user for 100 account using IAM role?
      How I can provide the access to  s3 and ec2 instance using the IAM?
      What are the parameters in IAM when we are giving the access?
      What is the trust relationship in AWS?


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
    What is cloud trail?
    What is cloud endure?
    How to access EC2 in a different VPC?
How to access the S3 bucket in the difference account?
What are different routing protocal in load balancer?
How to set the permissions for S3 bucket. So that no one can delete file?
What is transite gateway?
How to configure aws backup policy?
How to configure VPN?
How to connect 2 VPC with using peering?
What is ngjnx controller?
How to connect different AWS account from the shared account?
How to configure load balancing?
How to restrict the S3 based on the geographical location?
What are the different routing policy in route 53?
What we need swap on the aws?
How to integrate lamda, s3 and redis?
What is ebs network enhance?
How RDS Endpoint will connect to the application?
What is S3 lifecyscle?
What are the permissions in S3?
What is instance profiling?
What is transit Gateway and how it works?
What are type vpc Endpoint?
What is KMS in aws?
What is TLS termination in load balancer?
How to encrypted the ebs in aws?
What is privatelink?
How to connect vpc Endpoint in AWS?
How to change the configuration in inodb?
What are the different routing in application load balancer?
How to stop deleting a specific node in autoscaling?
What are the s3 storage classes?
What is cloud front?
How to rotate the logs for every 10 days which store in S3?
How to copy a bucket from one bucket to another?
What is FSX?
Can we mount EFS in the linux and Window server?
What are the different type os storage?
What EFS?
How to establish between on premise to cloud in AWS?
What is connection draining in load balancer?
How to monitor VPC?
What are the security practices for ec2 instances?
How to get the logs for VPC?
AWS system manager?
Which is stateless and statefull in security group and NACL?
What is cloud trail?
What is cloud front?
Have you access private end point point in AWS?
How to connect VPC from on premise data center?Hint: there are the 3 ways to do it.
How many default VPC we can create in an account?
What are way to restrict S3? Hint- by iam policy, bucket policy, object policy.






