[![Dalinkw3nt](https://circleci.com/gh/Dalinkw3nt/ML-microservices.svg?style=svg)](https://app.circleci.com/pipelines/github/Dalinkw3nt/ML-microservices)

## Project Overview

In this project, I have used skills acquired in this course to operationalize a Machine Learning Microservice API. 

Using a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). I have operationalized a Python flask app, `app.py`—that serves out predictions (inference) about housing prices through API calls.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

## Setup the Environment

* Create a virtualenv and activate it
* python3 -m venv ~/.devops
* source ~/.devops/bin/activate
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

1. Setup and Configure Docker locally
* install docker as described in the link.
* Run ./run_docker.sh
* Run docker ps to check if docker is running.
* Run ./make_prediction.sh to make prediction and copy/paste the logging info at terminal to output_txt_files/docker_out.txt

2. Setup and Configure Kubernetes locally
* Run minikube start to start minikube
* Run kubectl get pods to see which pods are running.
* Run ./run_kubernetes.sh
* Run ./make_prediction.sh to make prediction and copy/paste the logging info at terminal to output_txt_files/kubernetes_out.txt

3. Create Flask app in Container
* Run ./run_docker.sh to build and start the Flask app container.
* Run ./upload_docker.sh to upload the container to docker hub.

