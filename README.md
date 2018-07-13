# Installed php and apache using these step: 
 >https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04
 ```
  $touch counter.php
  $nano counter.php
  $git add counter.php
  $git commit -m "get file" 
  $git log
  $git remote add origin git@github.com:Andiswa1/visit-counter.git
  ```
  
 ## created countlog.txt
 
  $touch countlog.txt
  $nano countlog.txt
  $git add countlog.php
  $git commit -m "get file"
  $git log
  $git remote add origin git@github.com:Andiswa1/visit-counter.git 
  ```
  
 ## installed docker using these step:
 
  $curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  $Add the Docker repository to APT sources:sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu         $(lsb_release -cs) stable
  ```

# Install from the Docker repo instead of the default Ubuntu 16.04 repo: apt-cache policy docker-ce,

## Installed docker images following these steps:

 $docker run hello-world
 $docker search ubuntu
 $docker pull ubuntu
 $docker run ubuntu
 ```
 
## Installed following these steps:

 $docker run -it ubuntu
 $apt-get update
 $apt-get install -y nodejs
 ```
 
# Installed committing Changes in a Container to a Docker Image:

 $docker commit -m "What did you do to the image" -a "Author Name" container-id repository/new_image_name
 $docker images
 ```
 
## Listing Docker Containers:

 $docker ps
 $docker ps -a
 $docker ps -l
 $docker stop container-id
 ```
 
# Pushed Docker Images to a Docker Repository using these commands:

 $docker login -u docker-registry-username
 $docker push docker-registry-username/docker-image-name
 ```
 
 # Description
 
 Two core concepts are conveyed in the vanilla example: 1) how to build your own docker from Dockerfile, and 2) how to mount a volume inside of a docker.
 ```
 
 ## How to build
 ```
 
docker build -t zenlab/visit-counter .
```

# How to run
## run with docker image built from Dockerfile

docker run --rm \
  -p 80:80 \
  --name visit-counter \
  zenlab/visit-counter
  
  ## run with docker image built from Dockerfile
 
  
  docker run --rm \
  -p 80:80 \
  --name visit-counter \
  zenlab/visit-counter
  
 ## run with official php docker image
  
docker run --rm \
  -p 80:80 \
  --name php \
  -v "$PWD/scripts":/var/www/html \
  php:7.0-apache
  
  
# How to overwrite the web root with a volume at runtime

docker run --rm \
  -p 80:80 \
  --name visit-counter \
  -v "$PWD/scripts":/var/www/html \
  zenlab/visit-counter
  
 # How to access
 
 http://localhost/counter.php
 
 or

 http://localhost/php.info
 
 # Acknowledgments
 
 Code adapted from http://justintadlock.com/web-design/counter
 
 Docker image extended from https://hub.docker.com/_/php/
 
