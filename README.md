  # created countlog.txt
 ```
 
  $touch countlog.txt
  $nano countlog.txt
  $git add countlog.php
  $git commit -m "get file"
  $git log
  $git remote add origin git@github.com:Andiswa1/visit-counter.git 
  ```
  
 ## Installed docker using these step
 ```
 
 
  $curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  $Add the Docker repository to APT sources:sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu         $(lsb_release -cs) stable
  ```
  
 ```
 
## Installed following these steps:
```

 $docker run -it ubuntu
 $apt-get update
 $apt-get install -y nodejs
 ```
 
## Listing Docker Containers:
```

 $docker ps
 $docker ps -a
 $docker ps -l
 $docker stop container-id
 ``
 
 # Description
 ```
 
 Two core concepts are conveyed in the vanilla example: 1) how to build your own docker from Dockerfile, and 2) how to mount a volume inside of a docker.
 ```
 # Change file permissions of countlog.txt to add write access for all
 ```
  chmod a+w scripts/countlog.txt
  ```
 
 ## How to build
 ```
 
docker build -t zenlab/visit-counter .
```

# How to run
```
## run with docker image built from Dockerfile


docker run --rm \
  -p 80:80 \
  --name visit-counter \
  zenlab/visit-counter
  ```
  
  ## run with docker image built from Dockerfile
  ```
 
  
  docker run --rm \
  -p 80:80 \
  --name visit-counter \
  zenlab/visit-counter
  ```
  
 ## run with official php docker image
 ```
  
docker run --rm \
  -p 80:80 \
  --name php \
  -v "$PWD/scripts":/var/www/html \
  php:7.0-apache
  ```
  
  
# How to overwrite the web root with a volume at runtime
```

docker run --rm \
  -p 80:80 \
  --name visit-counter \
  -v "$PWD/scripts":/var/www/html \
  zenlab/visit-counter
  ```
  
 # How to access
 ```
 http://localhost/counter.php
 ```
 
 or
 ```

 http://localhost/php.info
 ```
 
 # Acknowledgments
 
 Code adapted from http://justintadlock.com/web-design/counter
 
 Docker image extended from https://hub.docker.com/_/php/
 ```
 
