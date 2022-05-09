- Remove Docker image repo but want to keep the most recent **5** images
  
  `docker rmi $(docker images --filter "reference=registry.example.com/app" -q | tail -n +6)`