# Service-Mesh-Istio
Pre-requisite is the have a EKS Cluster
Below are the steps you can follow to create your managed K8s cluster on AWS using EKS.
#########
EKS Setup
#########
1) Create IAM Role For EKS Cluster.
      EKS – Cluster (assume role will be attached to it . You don't need to add any policy)
2) Create Dedicated VPC For EKS Cluster. Using CloudFormation. 
     https://amazon-eks.s3.us-west-2.amazonaws.com/cloudformation/2020-08-12/amazon-eks-vpc-private-subnets.yaml 
3) Create EKS Cluster.(##youtube link)
4) Create IAM Role For EKS Worker Nodes.
       -  AmazonEKSWorkerNodePolicy
       -  AmazonEKS_CNI_Policy
       -  AmazonEC2ContainerRegistryReadOnly 
5) Create Worker Nodes.
6) Create An Instance (If Not Exists) Install AWS CLI , IAM Authenticator And kubectl. Configure AWS CLI using Root or IAM User Access Key & Secret Key. Or Attach IAM With Required       Policies.
      aws eks update-kubeconfig --name <ClusterName> --region <RegionName>
   Below are the steps for point 6.

####Setup K8s Client Machine #####

### Install Kubectl In Linux====

1) Install Download the latest kubectl release with the command:

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

2) Make the kubectl binary executable. 

     chmod +x ./kubectl
	 
3) Move the binary in to your PATH.
      sudo mv ./kubectl /usr/local/bin/kubectl
4) Test to ensure the version you installed is up-to-date:

kubectl version --client	 

### Install aws CLI In Linux====

1) Download AWS CLI ZIP
    
	curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

2) Download & Install Unzip
   
    sudo yum install unzip -y
   
4) Extract Zip
   
    unzip awscliv2.zip
   	
6) Install
   
	sudo ./aws/install -i /usr/local/aws-cli -b /usr/local/bin

8) Verify
  aws --version		
######## Configure AWS CLI using ACCESS Key & Secret Key ########

aws configure

##### Get KubeConfig file #####

aws eks update-kubeconfig --name <ClusterName> --region <RegionName> 

##### Verify Kubectl #####
kubectl get nodes
kubectl get pods 
## Congratulation!! your EKS cluster is up and running ######
