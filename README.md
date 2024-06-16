# Kubernetes RBAC

## Story

As your Kubernetes knowledge grows and you start to use your knowledge for more and more, it would be worth looking into how you can limit what certain users and processes can do inside your cluster for security purposes.

## What are you going to learn?

- How to limit what users and processes are able to do inside a cluster

## Tasks

1. Create a Service Account for your Cluster
    - Your Service Account can be seen when you ask for information about the Service Accounts in your Cluster

2. Create a Role that only lets the interaction of Pods
    - Your Role is created on the Cluster

3. Attach a Role Binding to the Service Account
    - Your Role Binding is successfully created

4. Create a Pod based on an Image that contains the Kubectl command and attach the Service Account to this Pod, then connect to it
    - You successfully connected to your Pod

5. Try to create a service for Nginx, if the service account is working, then you wont be able to, since it is not defined in the role that you can create it
    - The Nginx service is not created

6. Try to create a pod. You should be able to create this, since the role contains the ability to interact with Pods
    - The Pod is created

7. Try to create a pod again, however, it should be in another namespace
    - The Pod is not created, because that would need a Cluster Role instead of a regular one

## General requirements

None

## Hints

- Kubectl Docker Image: https://hub.docker.com/r/bitnami/kubectl/
- Kubectl has a few commands that are very similar to Docker ones. For example, the ```kubectl exec -it mongo-pod -- bash -c "mongo"``` command is the Kubernetes counterpart of ```docker exec -it <CONTAINER_ID> mongo```


## Background materials

- <i class="far fa-exclamation"></i> [Kubernetes Service Accounts](https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/)
- <i class="far fa-exclamation"></i> [Using RBAC Authorization](https://kubernetes.io/docs/reference/access-authn-authz/rbac/)
