# clusterautoscaler
Implementation of Cluster Auto Scaler on AWS provisioned using KOPS



kops create ig test-node --name=di-platform-v1.dev-cluster.didevops.com --role node --subnet us-east-1a --dry-run -oyaml --state=s3://di-platform-dev-clusters > /Volumes/data/personal/clusterautoscaler/kops/test-node.yaml


AWS_PROFILE=dev kops get ig test-node --name=di-platform-v1.dev-cluster.didevops.com --state=s3://di-platform-dev-clusters

AWS_PROFILE=dev kops edit ig test-node --name=di-platform-v1.dev-cluster.didevops.com --state=s3://di-platform-dev-clusters