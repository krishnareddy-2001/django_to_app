# django-todo
A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)
### Setup
launch an ec2 instance ubuntu server on aws account
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
NOW YOU CAN SEE THE DOCKER FILE WHICH IS READY TO BUILD AN IMAGE
INSTALL DOCKER TO PERFORM DOCKER COMMANDS
```bash
sudo apt install docker.io -y
```
DOCKER FILE IS USED TO BUILT DOCKER IMAGE 
```bash
FROM python:3                          #base image used 
RUN pip install django==3.2            #commands to be executed
COPY . .                               #for copying files  in container 
CMD ["python","manage.py","runserver","0.0.0.0:8000"]   
EXPOSE 8000                             #exposing port for serving  

```
NOW BUILD THE DOCKER IMAGE AND RUN THE CONTAINER
```bash
sudo docker build . -t todoapp
sudo docker run -d -p 8000:8000 todoapp
```
NOW COPY THE PUBLIC IP OF INSTANCE AND PORT 127.0.0.1:8000 ON LOCAL HOST
SUCCESSFULLY DEPLOYED WEB APP ON DOCKER.




