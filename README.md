# django-todo
A simple todo app built with django on ec2 instance ubuntu server in aws account

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)
### Setup
```bash
sudo apt-get update
```
To get this repository, run the following command inside your git enabled terminal
```bash
git clone https://github.com/krishnareddy-2001/django_to_app.git
```
now go to the django_to_app folder 
```bash
cd  django_to_app
```
now install docker on system to perform operations
```bash
sudo apt install docker.io -y
```
Dockerfile is used to build image in docker 
docker needs to create image run,
```bash
sudo docker build . -t todoapp
```
to see image built or not ,run
```bash
sudo docker images
```
now use the image to run container run,
```bash
sudo docker run -d -p 8000:8000 todoapp
```
to see the container is running or not run,
```bash
sudo docker ps
```
now copy the ip and add : port 8000
successfully deployed django todo app


![todo App](https://github.com/krishnareddy-2001/django_to_app/blob/2016b37446623db7567ea4629a362b792c7ba23c/staticfiles/Screenshot%202023-11-27%20110056.png)


In exception cases
if permissions denied in above commands,run 
sudo usermod -aG  docker $USER
sudo reboot
wait for some time or refresh tab after some time 
then execute above commands

now automating this code through jenkins 
####SETUP
installing jenkins on the server
```bash
cd
sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.8" 2023-07-18
OpenJDK Runtime Environment (build 17.0.8+7-Debian-1deb12u1)
OpenJDK 64-Bit Server VM (build 17.0.8+7-Debian-1deb12u1, mixed mode, sharing)
```
then run,
```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian/jenkins.io-2023.key
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```
Now to check and start jenkins 
```bash
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```
Enter ctrl+c to exit
Now go to the browser with ip:8080
jenkins port number is 8080 to begin with jenkins
now u have to setup jenkins in GUI(graphical user interface) and work on it







