
Future Scope:

- For application, create Frontend UI and enable for multiple users for authentication and authorization
- Can be used AWS Elasticache instead of K8 redis cluster
- Use Crossplane to create AWS S3 and AWS Elasticache 
- Create seperate nodegroups for application using labels and taints
- use reguests and limits on Kubernetes deployments
- deploy the K8s manifests using tolerations and affinity
- Use cluster Autoscaling/ Karpenter
- deploy metrics server on AWS EKS and use HPA
- Enable Promethues metrics for observability
- Use AWS WAF for protect the frontend applications
- Use Jenkins to build the images and upload the images into AWS ECR
- Use Helm Charts to provide the ability to leverage Kubernetes packages through the click of a button or single CLI command
- USe ArgoCD for automates the deployment of the desired application states in the specified target environments