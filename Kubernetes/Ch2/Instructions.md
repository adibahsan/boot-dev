
# Chapter 2

<ol>

<li> Pods </li>

Certainly! Here's a summary of the page content in markdown format:

---

## Kubernetes Basics

### 1. Pods
- **Definition**: Pods are the smallest and simplest unit in the Kubernetes object model¹[1].
- **Purpose**: They represent one or more running containers in a cluster²[2].
- **Example**:
    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: my-pod
    spec:
      containers:
      - name: my-container
        image: nginx
    ```
    In this example, a pod named `my-pod` runs an Nginx container.

### 2. Assignment
- **Task**: Deploy a second pod.
- **Steps**:
    1. Edit the deployment configuration file.
    2. Change the `replicas` field from 1 to 2.
- **Example**:
    ```yaml
    apiVersion: apps/v1
    kind: Deployment
    metadata:
      name: my-deployment
    spec:
      replicas: 2
      template:
        spec:
          containers:
          - name: my-container
            image: nginx
    ```
    This modification ensures two pods are running.

### 3. Tips
- **VS Code as Default Text Editor**:
    - Set VS Code as the default editor for Kubernetes YAML files.
    - Example command: `kubectl edit configmap kube-config -n kube-system`
- **Using kubectl Commands**:
    - Execute commands like `kubectl get pods`, `kubectl describe pod`, etc.
    - Example: `kubectl get pods -n my-namespace`


---

Feel free to use this summary for your revisions! If you have any further questions, don't hesitate to ask. 😊


- **Deployments:** 


# Pods

Pods are the smallest and most basic unit of computing in Kubernetes. They are a group of one or more containers that share resources and network.

## Ephemeral

Pods are designed to be temporary and replaceable. They can be terminated and restarted at any time, which allows for high availability and immutability.

## Assignment

The web page contains an interactive assignment that tests your understanding of Pods and their ephemeral nature. You have to use `kubectl` commands to get, log, and delete Pods.

For example, to get the list of Pods, you can use:

```bash
kubectl get pods
```

To view the logs of a Pod, you can use:

```bash
kubectl logs pod-name
```

To delete a Pod, you can use:

```bash
kubectl delete pod pod-name
```


- **Unique IP Address**

Sure, I can help you with that. Here is the same text in a markdown format:


# ASSIGNMENT

Run this command to get a "wide" output of your pods:

```bash
kubectl get pods -o wide
```


It gives a few more columns of information, including the IP address of each Pod. Notice that each Pod has a unique IP address!

Next, run:

```bash
kubectl proxy
```


This will start a proxy server on your local machine, probably on 127.0.0.1:8001. Assuming that's the host, navigate to [http://127.0.0.1:8001/api/v1/namespaces/default/pods](^1^) in your browser. You should see a big nasty JSON blob that describes the pods that you have running.

Paste just the root: [http://127.0.0.1:8001](^2^) into the tests on the right and run

The tests will make sure that the proxy server is accessible and that it's returning information about the current Pods in your cluster.

</ol>


