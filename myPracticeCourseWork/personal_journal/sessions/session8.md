[Personal Learning Record](../../personal_journal/personal_journal.md) | [Session Notes](../sessions/README.md) 

# Session 8

## Topics covered
In this session, I learned about Kubernetes (K8s), an open-source container orchestration platform used to deploy, manage and scale containerised applications.

The main topics covered were:

Kubernetes Architecture: Understanding the Control Plane, Worker Nodes and how Kubernetes manages containers across a cluster.

Pods: Learning how Pods contain one or more containers and represent the smallest deployable units in Kubernetes.

Deployments and ReplicaSets: Understanding how Kubernetes manages application replicas and maintains the desired number of running Pods.

Services: Learning how applications can be accessed through stable network endpoints.

Namespaces: Organising and separating Kubernetes resources.

Self-Healing: Understanding how Kubernetes automatically replaces failed or deleted Pods.

Scaling: Increasing or decreasing the number of application replicas.

kubectl Commands: Using the command-line interface to deploy, inspect, monitor and manage Kubernetes resources.

Docker Compose vs Kubernetes: Comparing basic multi-container orchestration with more advanced container management.


## Personal Notes and research following this session

During this session, I developed my understanding of container orchestration by building on the Docker and Docker Compose exercises from Sessions 5 and 6.

Docker allows applications to run inside containers, while Docker Compose manages multiple related containers using YAML configuration files. Kubernetes provides additional functionality, including automated scaling, self-healing and application deployment management.

I learned that Kubernetes uses a declarative approach, where configuration files define the desired state of an application. Kubernetes continuously works to maintain that state.

I also explored the relationship between Deployments, ReplicaSets and Pods. A Deployment manages ReplicaSets, which maintain the required number of Pods.

For example, if a Deployment specifies three replicas, Kubernetes attempts to keep three Pods running. If one Pod is deleted, a replacement can be created automatically.

I used Docker Desktop on my MacBook to run a local Kubernetes cluster and Terminal to execute kubectl commands.

## Exercises and results

Session 5 – Docker and Containerisation

Session 6 – Docker Compose

Session 8 – Exercise 8.1: Basic Kubernetes Deployment

Session 8 – Exercise 8.2: Kubernetes Example 1
## Summary of learning
Exercise 8.1 – Basic Kubernetes Deployment

In this exercise, I used Kubernetes to deploy an Nginx web server.

First, I started the Kubernetes cluster using Docker Desktop and created a Deployment with the following command:

kubectl create deployment nginx --image=nginx

I then checked the running Pods:

kubectl get pods

The output showed that the Nginx Pod was running successfully with a READY status of 1/1.

I used:

kubectl get all

This displayed the Pod, Deployment, ReplicaSet and Kubernetes Service.

My results:

Nginx Pod status: Running

Ready containers: 1/1

Deployment: 1/1 available

ReplicaSet: 1 desired, 1 current and 1 ready

Container restarts: 0

I also used the kubectl describe pod command to inspect the Pod configuration, including its IP address, container image, node assignment and lifecycle events.

During this exercise, I encountered an error because I used a Pod name copied from the lecturer's example. I discovered that Kubernetes generates unique Pod names, so I needed to use the name displayed by my own kubectl get pods output.

This helped me understand how to identify and troubleshoot Kubernetes resources.

Exercise 8.2 – Deploying a Node.js Application

In the second exercise, I worked with a Kubernetes project containing a Dockerfile and YAML configuration files.

The project included:

namespace.yaml – defines the Kubernetes namespace.

deployment.yaml – configures the application Deployment.

service.yaml – provides network access to the application.

configmap.yaml – stores application configuration.

Dockerfile – defines how the application container image is built.

Initially, I encountered a Docker build error because the app/index.js file was missing from my local project.

The error occurred when Docker attempted to execute:

COPY app/index.js ./

I investigated the problem using Terminal commands such as ls, find and cat Dockerfile.

After identifying the missing application files, I checked the GitHub repository for updates.

The application was then deployed to Kubernetes using the provided YAML configuration files.

The main commands used were:

kubectl apply -f k8s/namespace.yaml

kubectl apply -f k8s/configmap.yaml

kubectl apply -f k8s/deployment.yaml

kubectl apply -f k8s/service.yaml

I monitored the application using:

kubectl get pods -n k8s-demo -w

My results:

The output showed three running Pods:

k8s-demo-app-794cc59779-4p8xs

k8s-demo-app-794cc59779-fxx9k

k8s-demo-app-794cc59779-n282k

All three Pods had a READY status of 1/1, a Running status and zero restarts.

This demonstrated that Kubernetes was successfully managing multiple replicas of the application.

I also learned that the -w option continuously watches Kubernetes resources and that the monitoring process can be stopped using Control + C without stopping the running Pods.

The exercise also introduced manual scaling using:

kubectl scale deployment k8s-demo-app -n k8s-demo --replicas=5

This command changes the desired number of application replicas to five.

Screenshot 3: Docker build process and troubleshooting the missing application files.

Screenshot 4: Three running application Pods in the k8s-demo namespace.

Screenshot 5: Kubernetes Pod scaling results, if completed.

Summary of learning

Through Session 8, I gained practical experience using Kubernetes to deploy and manage containerised applications.

I learned how Kubernetes differs from Docker Compose and how it provides more advanced features for managing applications.

I developed an understanding of the relationships between Pods, Deployments, ReplicaSets, Services and Namespaces.

The practical exercises helped me become more confident using kubectl commands to inspect application status, monitor Pods and troubleshoot deployment errors.

One of the most useful parts of this session was learning how Kubernetes maintains the desired number of application replicas and supports scaling.

I also improved my troubleshooting skills by identifying missing application files, checking Docker build errors and understanding why Pod names differ between deployments.

Overall, this session helped me understand how Kubernetes can be used to manage containerised applications more reliably and efficiently, particularly in environments where multiple application instances are required.
