# Overview of how to use multipass via a docker for beginner
## multipass
A multipass is a tool that help us run a virtual machine. __Virtual machine__ is digitezed version of a physical machine. Virtual machine help us run programs, operating system, store data and connect to the network.
## how to launch or run a multipass 
To run a multipass you need an ubuntu_instance. The ubuntu_instance we ued was docker. A __docker__ is a tool that help us create and manage container. __Container__ is an isolated user-space that help you run a programs. When you use a container to run a program it some how load all the packages and dependencies related to that program without you noticing.
We use the following command to lauch the multipass:
- < multipass launch docker --name instance_name > to launch ubuntu_instance in multipass 
- We can use the command < multipass --help > to know all the command available on multipass
- To enter the shell ( we some how created a new shell in our multipass so that if our code had to crash then it will neither affect out host machine or host shell). Type to enter the shell < multipass shell instance_name >. So with this command your new default shell in the multipass, will be instance-name which is just a name given to an instance, the instance here in our case is docker. The __docker__ is an ubuntu instance with docker pre-install in the ubuntu.

we can also access our multipass or dry run a code on the host machine, this is done as follow:
- Go to the host shell 
- enter inside the host scriting shell, use the command < nano .zshrc > if of cost you are using the zshell default shell or the command < nano .bashrc > if otherwise.  
- Type < allias any_name= multipass exec instance_name --docker > in you scripting shell
- Save it by pressing ctrl + o and enter, ctrl + x to exit.
- execute your file using the command  < source .bashrc or .zshrc >
- On your host shell, type < any_name _command_ >, this is what you want to execute on the multipass. So it will execute on the virtual machine managed by the multipass.

 With docker in multipass we can run any kind of code without fear because even if it had to face a crash, it will only affect the virtual machine managed by the multipass and the host machine itself. 
  
you may better understand how the process work with the following diagram
![myimage](doc.drawio)(https://drive.google.com/file/d/1C_Z3mA3-9kYLqGYoBO2D72TnDMMAykki/view?usp=drive_link)
