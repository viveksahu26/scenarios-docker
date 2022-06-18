## Run Container from Ubuntu Image.

To run container from Ubuntu image, instruct docker with command:

    docker run ubuntu:latest

What above command says in human language:

    docker please run new container or new OS(light weight) with Image Ubuntu:latest.
    Remeber this OS is very lightweight of approx 100MB to 1000MB. Whereas your real host Operating system weight in GBs(approx 8-16 GiB)

Now check whether container is running or not?

    docker ps
You will find that no container is Running. Why why??

You will find your container is in stop mode.

    docker ps -a
Yes, the container is in stop mode. Why so?

After knowing the answer you will be like "WOW :)". 

Understand this:

     Let’s understand with real life examples. As you all know that you can use your phone to make phone calls or use the internet as long as you have talktime balance or data balance respectively. As it ends, you can’t make phone calls or use the Internet. Similarly, the same logic applies on Containers. As long as some program is running inside your container, the container will continue to run. If programs stops running, then your container will also stop. That's why your container stops automatically here. So, to make your container keep running you need to run some program i.e. a terminal or bash shell program  using `-t` option. And along with `-t` option you need to include `-i` option also. Why so? To make your terminal continuously run. Have you ever notice that your terminal cursor continously blinks. It means it’s waiting for your input. 

`NOTE:` Terminal is a black color interface which takes your input and prints the corresponding output. Terminal is also a program. To know more about terminal click here.  ---> Why docker image is less in size than real OS image.

    Windows has Poweshell as Terminal.
    Ubuntu, RedHat, or any other Linux distros has bash shell as Terminal.

I know one more question in your mind. When you start new OS(suppose Windows). You don't see terminal. But instead you see graphical interface and beautiful icons, but why not here. To know it better click here.
In short, that's why Image size is in b/w 100MB to 1000MB, whereas your actual OS size in 8 to 16 GiB. The reason is normal OS supports graphical interface, media player, drivers for printers, earphone, speakers and many more. Whereas docker image has only limited and only required functionalities. 

Now, let's get back to the topic and run container.

    docker run -t -i --name=tutorial ubuntu:latest
What above command says in human language:

    docker run container(new OS) using image Ubuntu, with name tutorial and at the same time start terminal program in input mode or interactive mode. As a result your container keeps running.

What's happening behind the scene after running above command:

    At the time of running command you was in your host Operating System. but now you are inside Container. Intechnical terms, now you are inside different namespace. You will get to know about it when you learn how containers are created internally. See this difference. 
    
    Whatever files present inside your host operating system, you won't see inside container. Or whatever you will create file inside container you won't se in the host operating system.


