## Create Manually Image

Now let's create imgae from stopped container not running container.

To stop container, write below command inside your container.

    exit

#### What's happening behind the scene after running above command:
Remember that point that container continue to run till any program running inside it. And that program was Terminal or bash shell. On executing command "exit" on terminal, the terminal gets exited. In other words terminal program stops running. As a result now no program is running inside container. Therefore container will also stop. 

#### Do you know?
Is there any way to come out of container without stopping it ?
Yes, 
    
    press "ctrl p+q" at the same time
Is there any way to go inside any running container?
Yes,

    docker attach tutorial

    The above command takes you inside tutorial container.

Lets get back to the topic. After stopping container. Check it using below command

    docker ps -a

Now, to create Image from it. Run the below command:

    docker commit tutorial tutorial-image

#### What above command says in human language:
Hey docker please save all the changes that I made inside container tutorial. And create new image of name tutorial-image. 

#### Relate with git
"docker commit" is similar to "git commit" command. In "git commit" also it save all the changes till that point of time you made.

Now, check whether "tutorial-image" is present or not:

    docker images

#### What is the advantage of creating image:
You don't need to install dependencies again and again if you are using "tutorial-image". You can use the same image everytime. And also share with anyone. The environment will be same for everyone whosoever using this image.

### Conclusion

    exit
    docker ps -a
    docker commit tutorial tutorial-image

