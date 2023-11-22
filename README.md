# swoom-sre-test


# Using terraform (HCL), provision a Kubernetes cluster (AWS EKS)

* Pre-requisites: 

  Make sure you have the following installed on your local machine.
    1. Terraform
    2. Git
    3. Kubectl

* Provisioning the cluster

  Clone this repository to your machine
    * git clone https://github.com/GhostGeneral/swoom-sre-test.git
    * cd swoom-sre-test/iac
    * terraform init
    * terraform plan
    * terraform apply.


# Deploying a simple Nginx web server on the EKS Cluster using Kubernetes Manifest

* Pre-requistites

  Make sure you have the following provisioned and running.
  1. Docker Engine
  2. Kubernetes Cluster

* Deploying the application.

  There is a Dockerfile for the App inside the app folder

    * cd ..
    * cd app/
    * docker build -t swoom .
    * make sure that you are logged in to a docker registry 
    * docker tag swoom [yourregistry]/swoom
    * docker push [yourregistry]/swoom
    " update the swoom-test-deployment.yaml deployment manifest file with your image"
    * kubectl apply -f swoom-test-deployment.yaml
    * kubectl apply -f swoom-test-service.yaml

 