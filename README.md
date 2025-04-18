# Kubernetes-Cluster-with-Helm
Directory Structure:
k8s-cluster-setup/
├── cluster/
│   ├── eks-terraform/
│   └── helm-charts/
└── apps/
    ├── nginx/
    └── redis/
Key Script:
# eks-setup.sh
eksctl create cluster \
  --name prod-cluster \
  --region us-east-1 \
  --node-type t3.large \
  --nodes 3
# helm-charts/nginx/values.yaml
replicaCount: 3
service:
  type: LoadBalancer
  port: 80
  
  
