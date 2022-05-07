- Install htpasswd tool to generate authentication
  - On Debian/Ubuntu

    `sudo apt-get install -y apache2-utils`

  - On Red Hat/CentOS

    `sudo yum install -y httpd-tools`


- Generate authentication file

  HTPasswd authentication need to use Bcrypt mode
  Replace <username> with your 'username' that will be used for the auth.

  `htpasswd -B registry/auth/htpasswd tt`

  *Notes:* '-B' seems like use bcrypt encryption method.

- Configure and run docker-compose.yml
  
  `docker-compose up -d`

- Check the Container Registry Stack

  `docker-compose ps`

  `docker-compose logs`

- Forcefully restart the Docker set up to make the changes accessible
 
  `docker-compose up -d --force-recreate`

- Log in to the registry:
  
  `docker login localhost:5000`

- Testing the authentication

  `curl -iv -H "Authorization: Basic $(echo -n "tt:tt1234" | base64)" localhost:5000/v2/`