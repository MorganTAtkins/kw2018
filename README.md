# Knowledge Week 2018 Container Pod

## Introduction
With container images, we confine the application code, its runtime, and all of its dependencies in a pre-defined format. And, with container runtimes like runC, containerd, or rkt we can use those pre-packaged images, to create one or more containers. All of these runtimes are good at running containers on a single host. But, in practice, we would like to have a fault-tolerant and scalable solution, which can be achieved by creating a single controller/management unit, after connecting multiple nodes together. This controller/management unit is generally referred to as a Container Orchestrator.

## Containers
Containers are an application-centric way to deliver high-performing, scalable applications on the infrastructure of your choice.

## Slides
[Slides](slides/slides-container-pod.html)

### Slides as a Container
```
$ docker image build -t kw2018-slides slides/.

$ docker container run -d -p 80:80 kw2018-slides
```
Open `localhost/slides-container-pod.html`

# Labs
## [lab 1](labs/lab1/README.md)

In lab one we will be creating and starting a basic python application within a docker container
This applcication container will allow us to upload images to s3.

### Specification:
* Light weight base OS [alpine]
* Pyton 2.7 application
* Access to AWS s3 bucket

## [lab 2](labs/lab2/README.md)

In lab two we will be creating second python application within a docker container that will display images randomly.

### Specification:
* Light weight base OS [alpine]
* Pyton 2.7 application
* Access to AWS s3 bucket
