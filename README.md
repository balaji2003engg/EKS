# EKS

1.Create the IAM role with adminacess

2. Install the eksctl 

curl --silent --location "https://github.com/weaveworks/eksctl/releases/download/latest_release/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp  

sudo mv /tmp/eksctl /usr/local/bin

  'Test the version
```eksctl version```
   
3.Install the kubectl. Dowload the kubectl

Reference Link :https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html

     curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.18.9/2020-11-02/bin/linux/amd64/kubectl


4. Apply execute permissions to the binary.

        chmod +x ./kubectl
      
5.Copy the binary to a folder in your PATH. If you have already installed a version of kubectl , then we recommend creating a $HOME/bin/kubectl and ensuring that $HOME/bin comes first in your $PATH.


        mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin
        
  #Create the EKS
  
  eksctl create cluster -f createcluster.yaml
        
