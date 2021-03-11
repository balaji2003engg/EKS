# EKS

Create VPC for EKS

1. Create the VPC ,subnet, IGW and Route tables for EKS using cloudformation template

REference link: https://docs.aws.amazon.com/eks/latest/userguide/create-public-private-vpc.html

2. Go to the cloudformation and create the stack 

3. Provide the below Amazon S3 URL in the template session


https://amazon-eks.s3.us-west-2.amazonaws.com/cloudformation/2020-10-29/amazon-eks-vpc-private-subnets.yaml

4. Go to everything as defaut and it will create the VPC and other stuff

Create the Role for EKS cluster

5. Go to the create role and select the service as EKS_Cluster. Go remanining as default stuff and create the ekscluster role

 Create the EKS Cluster
 
 6. Go to the EKS and create the cluster with eks cluster and security group which we created using cloudformation

SetUP Machine to access EKS cluster and nodes



7. Install the aws-iam-authenticator. Download aws-iam-authenticator on linux machine using below command

ref link : https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html

      curl -o aws-iam-authenticator https://amazon-eks.s3.us-west-2.amazonaws.com/1.18.9/2020-11-02/bin/linux/amd64/aws-iam-authenticator


8.Apply execute permissions to the binary.

     chmod +x ./aws-iam-authenticator
     
9.Copy the binary to a folder in your $PATH. We recommend creating a $HOME/bin/aws-iam-authenticator and ensuring that $HOME/bin comes first in your $PATH.

     mkdir -p $HOME/bin && cp ./aws-iam-authenticator $HOME/bin/aws-iam-authenticator && export PATH=$PATH:$HOME/bin
     
10.Install the kubectl. Dowload the kubectl

Reference Link :https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html

     curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.18.9/2020-11-02/bin/linux/amd64/kubectl


11. Apply execute permissions to the binary.

        chmod +x ./kubectl
      
12.Copy the binary to a folder in your PATH. If you have already installed a version of kubectl , then we recommend creating a $HOME/bin/kubectl and ensuring that $HOME/bin comes first in your $PATH.


        mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin
