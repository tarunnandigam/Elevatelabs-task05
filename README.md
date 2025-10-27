In this task, I learned how to deploy, expose, and scale an application using Kubernetes on a local cluster created with Minikube.
I deployed a simple Nginx web application, exposed it through a NodePort service, and verified that it runs successfully in my browser.

This project helped me understand the core Kubernetes workflow — from writing YAML manifests to managing pods and scaling deployments.


Issues Faced and How I Solved Them
1)kubectl command not found
 Reason: kubectl not added to PATH
 Solution: Reinstalled kubectl and added it manually to /usr/local/bin

2)Minikube failed to start (driver issue)
 Reason: No container driver (Docker/VirtualBox) installed
 Solution: Installed Docker and started Minikube with
minikube start --driver=docker

3)Pods stuck in "ContainerCreating" state
 Reason: Image pulling delay due to slow network
 Solution: Waited and verified using kubectl describe pod <pod-name>

4)Browser didn’t open automatically after minikube service
 Reason: Auto-launch not supported in terminal session
 Solution: Copied the provided URL and opened it manually in the browser

Project Outcome
1)Successfully deployed and exposed an Nginx application on Minikube
2) Scaled deployment from 2 to 4 replicas
3) Verified logs, pods, and services through kubectl commands
4) Learned end-to-end Kubernetes deployment workflow
