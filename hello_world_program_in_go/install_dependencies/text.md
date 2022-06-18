# Install dependencies
The final motive is to run golang hello world program, need to install
golang languge.

Before that you need to download some commands which are not present
in this image. The reason is Image is light-weight and it only contains 
only necessary programs.

First of update packages and liabraries of Image:

    apt-get update 

Now install commands like wget, vim

    apt-get install wget -y
    apt-get install vim -y

Now, download or install golang programming langiuage.

    wget https://go.dev/dl/go1.18.3.linux-amd64.tar.gz

Since, the file is in tar mode, similar to zip. Need to extract files
from it. Run the below command to extract files.

    tar xvf go1.18.3.linux-amd64.tar.gz
    x ---> Extract files
    v ---> show me all output while extracting files
    f ---> denotes file
    The file will be extracted in your current directory, inside go/ directory.

Move this `go/` directory inside `/usr/local/`

    mv go/ /usr/local/

Now, check whether go is installed or not.

    go version

There is no such command. Why so? After installing go, then also it says 
no `go` command is found.
The go command is present inside `/usr/local/go/bin` folder. So, add this
folder in your path by `export` keyword.

    export PATH=$PATH:/usr/local/go/bin
                    or 
    echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.bashrc

Now, again check whether go is installed or not.

    go version

Yes, now it is installed. Finally golang is installed inside you new
light weight operating system.




