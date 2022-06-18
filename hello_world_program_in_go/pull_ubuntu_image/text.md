## Pull Ubuntu Image with latest version.

`docker` knows how to manage containers as well images. User only need to instruct docker through different commands.

To pull images, instruct docker with below command.

    docker pull ubuntu:latest

What above command says in human language: 

    docker please download or install ubuntu image with latest version.

What's happening behind the scene after running above command:

```
First docker checks from the list of available images(using `docker images` command) that whether the image user want 
is present locally or  not. If image is present locally then it will not download or install. If not, then docker will 
go to public registory, [DockerHub](https://hub.docker.com/) and download image from there. DockerHub is registory for images. 
It is similar to github registory. If you are familiar  with git, then you must know to download the repo from github. 
For the same run command,  `git clone repository_name`. Similarly, in the case   of DockerHub, to download image fom it.  
Replace,
              git ---> docker
              clone ---> pull
              repository_name ---> image name
```

To see list of all available images instruct docker with below command.

    docker images
