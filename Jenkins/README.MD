### Docker Registry Rentention
    
    There are container with various tags push to the Docker registry e.g. `app/calculator:v1` , `app/calculator:v2`, `app/jmeter:v1`, `app/jmeter:v2` etc.

    There is a need to go through all of the repositories in the registry and retain only the last `X` images. 

- Remove Docker image repo but want to keep the most recent `5` images by CLI
  
  `docker rmi $(docker images --filter "reference=registry.example.com/app" -q | tail -n +6)`

- Write a Jenkinsfile for the Docker Registry Rentention
 
  ![Jenkins Job](/images/jenkins.png)