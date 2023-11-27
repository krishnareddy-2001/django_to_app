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
now install docker on system to perform operations
```bash
sudo apt install docker.io -y
```
Dockerfile is used to build image in docker 
```bash
FROM python:3                          #base image used 
RUN pip install django==3.2            #commands to be executed
COPY . .                               #for copying files  in container 
CMD ["python","manage.py","runserver","0.0.0.0:8000"]   
EXPOSE 8000                             #exposing port for serving  

```
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
(https://raw.githubusercontent.com/krishnareddy-2001/django-to_app/develop/staticfiles/Screenshot 2023-11-27110056.png)
In exception cases
if permissions denied in above commands,run 
sudo usermod -aG  docker $USER
sudo reboot
wait for some time or refresh tab after some time 
then execute above commands





