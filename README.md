Create new EKS cluster

Add an IAM role for EKS

Create a new VPC (Public and Private) using cloud formation using the template in site
https://docs.aws.amazon.com/eks/latest/userguide/creating-a-vpc.html#create-vpc

Once the EKS cluster is created, download the AWS CLI 

run `aws configure` to connect via access key

run `aws eks --region ap-south-1 update-kubeconfig --name kub-app-dep` so it will update the `.kube/config file`

Go to EKS cluster and browse to compute tab, add new node

You need to create new EC2 role with policies

![alt text]("aws ec2 policies.png" "Policies")

Once the node is created and active, run `kubectl apply` command. Note these commands are running in EKS cluster because of updated `.kube/config`

rest steps are same as local minikube cluster
