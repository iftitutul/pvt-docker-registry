- Create s3 bucket 
  
  `s3cmd mb s3://<registry-bucket> --profile <name>`
  
- Apply K8s configuration files
  
  `kubectl apply -f .`

- Now login to our registry URL

  `docker login registry.example.com`

- Testing the docker registry
  
  ```
  $ docker pull busybox
  $ docker tag busybox registry.example.com/busybox:latest
  $ docker push registry.example.com/busybox:latest
  $ docker logout registry.example.com
  $ docker login registry.example.com
  $ docker pull registry.example.com/busybox:latest
  ```
- Check the s3 bucket and verify docker registry repository

**Notes:** For multiple docker registries, must configure `http.secret` is being set correctly. Please see: https://docs.docker.com/registry/configuration/




