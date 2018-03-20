I installed php and apache using these step: 
 >https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04
I created counter.php using these step:
  $touch counter.php
  $nano counter.php
  $git add counter.php
  $git commit -m "get file" 
  $git log
  $git remote add origin git@github.com:Andiswa1/visit-counter.git
 I created countlog.txt
  $touch countlog.txt
  $nano countlog.txt
  $git add countlog.php
  $git commit -m "get file"
  $git log
  $git remote add origin git@github.com:Andiswa1/visit-counter.git,  
  
 I installed docker using these step:
  $curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  $Add the Docker repository to APT sources:sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable",

Install from the Docker repo instead of the default Ubuntu 16.04 repo: apt-cache policy docker-ce,

I installed docker images following these steps:
 $docker run hello-world
 $docker search ubuntu
 $docker pull ubuntu
 $docker run ubuntu,
 
I installed following these steps:
 $docker run -it ubuntu
 $apt-get update
 $apt-get install -y nodejs,
 
I installed committing Changes in a Container to a Docker Image:
 $docker commit -m "What did you do to the image" -a "Author Name" container-id repository/new_image_name
 $docker images,
 
Listing Docker Containers:
 $docker ps
 $docker ps -a
 $docker ps -l
 $docker stop container-id,
 
I Pushed Docker Images to a Docker Repository using these commands:
 $docker login -u docker-registry-username
 $docker push docker-registry-username/docker-image-name
