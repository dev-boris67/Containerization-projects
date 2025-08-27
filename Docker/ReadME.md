# Deploy an App with Docker

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-compute-eb)

**Author:** Nchindo Boris  
**Email:** nchindoboris37@gmail.com

---

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-compute-eb_c4df13c84)

---

## Introducing Today's Project!

### What is Docker?

Docker is a tool that allows you to package and run applications in a container. In today`s project I deployed an App with Docker


### One thing I didn't expect...

In this project  I did not expect  running many commands on terminal

### This project took me...

It took me 1 hour 45 minutes to complete this project

---

## Understanding Containers and Docker

### Containers

Containers are DevOps tools used for making software development and deployment more efficient. They are useful because they solve a common problem called the "it works on my machine" problem. Containers pack applications to run in one file easily



A container image is a blueprint or template for containers. It gives Docker instructions on what to include in a container, such as application code, libraries, dependencies, and necessary files.

### Docker

Docker is a software tool which helps you create, manage, and deploy these containers efficiently.
Docker Desktop lets you manage everything about your containers. You can create new containers, adjust their settings, or monitor how they run. 

Docker daemon is an engine or background process that manages the Docker containers on your computer. It takes commands from the Docker client and does the heavy lifting of building, running, and distributing your containers.

---

## Running an Nginx Image

Nginx is a web server, which means it's a program that serves web pages to people on the internet.

The command I ran to start a new container was docker run 

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-compute-eb_6245f5bb10)

---

## Creating a Custom Image

A Dockerfile is a document with all the instructions for building your Docker image

My Dockerfile tells Docker three things;
1. FROM nginx:latest = our image starts as a copy of the latest Nginx image
2. COPY index.html /usr/share/nginx/html/ replaces the default HTML file provided by Nginx with your own custom index.html file

The command I used to build a custom image with my Dockerfile was docker build -t my-web-app. The '.' at the end of the command Docker to find the Dockerfile in the current directory

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-compute-eb_4c741d1913)

---

## Running My Custom Image

There was an error when I ran my custom image because there's already a container using port 80, so the new container you're creating can't access it. I resolved this by stopping the container I first created to run on port 80

In this example, the container image is the blueprint that tells Docker the application code, etc that should go into a container. The container is the actual software that's created from this image and running the web server displaying my index.html

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-compute-eb_74b5c3d619)

---

## Elastic Beanstalk

AWS Elastic Beanstalk is a service that makes it easy to deploy cloud applications without worrying about the underlying infrastructure.
Elastic Beanstalk can run applications that are packaged as Docker containers

Deploying my custom image with Elastic Beanstalk took me about 20 minutes

![Image](http://learn.nextwork.org/soothed_rose_serene_peach/uploads/aws-compute-eb_26d5573b23)

---

## Deploying App Updates

---

---

