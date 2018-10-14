## Mandatory Information

Since I am using docker toolbox I wont have access to localhost or my IP address. I have to use the ip
address of the VM, yes docker is running our image on a VM.
<br>
The ip address of the VM is
<br>
http://192.168.99.100
<br>
So to visit a website which is hosted on port 8080 lets say we have to go to
<br>
http://192.168.99.100:8080

<br>

The first step is to open docker quickstart terminal. From there naviagate to your project directory.
To change drive type cd /d which is **cd /[drive name in small caps]**
<br>

Then make a docker file in your project having the configurations. Then run the docker image like this.
<br>
**$ docker build -t hello-world .**
hello-world is the **image name**
After that is done we can run the image with
<br>
$ docker run -p 8082:8081 hello-world
<br>
This is mapping port 8082 from the world to port 8081 of our application. So basically we can map
port 80 to port 3000 of our application.

<br>
After this command our application will be running. 
If we want to see all the running docker images we have to type
<br>
docker ps
<br>
$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                              NAMES
79f78666d31e        hello-world         "/bin/sh -c 'node in…"   3 minutes ago       Up 3 minutes        8082/tcp, 0.0.0.0:8083->8081/tcp   fervent_keldysh
fc343aecaebe        hello-world         "/bin/sh -c 'node in…"   7 minutes ago       Up 7 minutes        8082/tcp, 0.0.0.0:8082->8081/tcp   goofy_hopper

We can get the name of the docker container here under name section.
To stop it we have to type **docker stop [name]**

s
