# EKS

Create VPC for EKS

1. Create the VPC ,subnet, IGW and Route tables for EKS using cloudformation template

REference link: https://docs.aws.amazon.com/eks/latest/userguide/create-public-private-vpc.html

2. Go to the cloudformation and create the slack 

3. Provide the below Amazon S3 URL in the template session


https://amazon-eks.s3.us-west-2.amazonaws.com/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml

4. Go to everything as defaut and it will create the VPC and other stuff

Create the Role for EKS cluster

5. Go to the create role and select the service as EKS_Cluster. Go remanining as default stuff and create the ekscluster role

 Create the EKS Cluster
 
 6.
