## Pull Ubuntu Image with latest version.

`docker` knows how to manage containers as well images. User only need to
instruct docker through different commands.

#### To pull images, instruct docker with below command.
```
docker pull ubuntu:latest
```

#### What above command says in human language: 
docker please download or install Ubuntu image with latest version.

#### What's happening behind the scene after running above command:

1) docker checks from the list of available images(using "docker images" command) that whether the Ubuntu:latest image is present locally or not. 
2) If present locally then fine. 
3) Else, docker will download image from [DockerHub](https://hub.docker.com/). DockerHub is public registory for Images as GitHub is public repository for codes.

#### Note: 
Like git is a cli tool to interact with GitHub. 
Similarly, docker is also a cli tool to interact with DockerHub.

#### Relate with git
If you are familiar  with git, then you must know to clone or download repo from github. 
To clone git repo from GitHub, command is: 
    
    git clone repository_name 
Similarly, to pull image from DockerHub command is:
    
    docker pull ubuntu:latest

```
git   ---> docker

clone ---> pull

repository_name ---> image name
```

To see list of all available images instruct docker with below command.

    docker images

## Conclusion

    docker pull ubuntu:latest