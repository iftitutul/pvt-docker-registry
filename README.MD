### [Private Docker Registry](https://docs.docker.com/registry/)
----------------------------

The Registry is a stateless, highly scalable server side application that stores and lets you distribute Docker images. The Registry is open-source.

A private Docker registry allows you to share your custom base images within your organization, keeping a consistent, private, and centralized source of truth for the building blocks of your architecture.

### Setting up a Private Docker registry:
  - create a kubernetes cluster in AWS EKS
  - Use AWS s3 bucket to store the repo
  - AWS SSM to manage secrets
  - Create a redis cluster to make high availability using statefulset
  - Ingress controller to serve the applications


