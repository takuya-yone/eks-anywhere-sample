https://anywhere.eks.amazonaws.com/docs/getting-started/local-environment/

```Bash:Prepare EKS Anywhere
brew install aws/tap/eks-anywhere
eksctl anywhere version
```

```Bash:Create Cluster
CLUSTER_NAME=dev-cluster
eksctl anywhere generate clusterconfig $CLUSTER_NAME --provider docker > $CLUSTER_NAME.yaml
eksctl anywhere create cluster -f $CLUSTER_NAME.yaml
```