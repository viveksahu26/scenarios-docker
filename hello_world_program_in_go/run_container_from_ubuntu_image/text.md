## Run Container from Ubuntu Image.

#### To run container from Ubuntu image, instruct docker with command:

    docker run ubuntu:latest

#### What does above command says in human language:

docker run new container or new light weight OS on top of host OS using Image Ubuntu:latest.

Do you know ?

The actual image used in your host OS is of size approx 8-16 GiB, whereas the image used by Containers are of sizes 10 MiB to 1000 MiB. 

Now check whether container is running or not?

    docker ps
You will find that no container is Running. Why??

You will find that container is in stop mode.

    docker ps -a
Yes, the container is in stop mode. Why so?

After knowing the answer you will be like "WOW :)". 

#### Understand this:

Let’s understand with real life examples. As you all know that you can use your phone to make phone calls or use the 
internet as long as you have talktime balance or data balance respectively. As it ends, you can’t make phone calls or use the Internet. Similarly, the same logic applied on Containers. As long as some program is running inside your container, 
the container will continue to run. If programs stops running, then your container will also stop. That's why your container 
stops automatically after running "docker run ubuntu:latest" .So, to make your container keep running you need to run some program i.e. a terminal or bash shell 
program  using -t option. And along with -t option you need to include -i option also. Why so? To make your terminal continuously run. Have you ever noticed that your terminal cursor continously blinks? It's a signal to the user that it’s waiting for your input.

`NOTE:` 
Terminal is a black color interface which takes your input and prints the corresponding output. Terminal is also a program.

    Windows has Poweshell as Terminal.
    Ubuntu, RedHat, or any other Linux distros has bash shell as Terminal.

#### Are you Curious ??
Why on starting new host operating system you see graphical interface, beautiful icons, etc, whereas on starting new light weight OS(i.e. container) you see a black screen known as Terminal. Why so ? Click here to know. 

Now, let's get back to the topic and run container.

    docker run -t -i --name=tutorial ubuntu:latest

#### What above command says in human language:

Hey, docker please run container(new light-weight OS) on top of host OS using Ubuntu Image, with name of container as tutorial and along with that start program called Terminal in Interactive or input mode, So, that my container keeps running.

#### What's happening behind the scene after running above command:

At the time of running command you was in your host Operating System. But now you are inside Container. In technical terms, now you are inside different namespaces.
Inially you was in host namespace or inside host boundary and now you are inside container namespace or inside container boundary. We will discuss later about the namespaces.

#### How to get confirmation that you are inside Container.
1) Whatever files(that you created) present inside your host operating system, you won't see inside container and vice-versa.
2) See to the left of terminal, from 

    Switched from  "ubuntu $" to "root@ba94a237248f:/#"
    ubuntu $ ---> you are in host OS.
    root@ba94a237248f:/#  ---> You are inside container.

### Conclusion

    docker run -t -i --name=tutorial ubuntu:latest
