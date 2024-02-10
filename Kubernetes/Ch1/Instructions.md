<ol>

<li> **Minikube** </li>

- **Minikube Config:**
```cmd
minikube start --extra-config "apiserver.cors-allowed-origins=["http://boot.dev"]"
```

- minikube version
- **Minikube Dashboard:** to check minikube's version -

```cmd
minikube dashboard
```

<li>DEPLOYING SYNERGYCHAT</li>

- **Deploying an image:** Use `kubectl create deployment` with the name of the deployment and the ID of the Docker image.

```bash
kubectl create deployment synergychat-web --image=lanecwagner/synergychat-web:latest

```


- **Viewing deployments:** Use `kubectl get deployments` to see the status of the deployments.

```bash
NAME              READY   UP-TO-DATE   AVAILABLE   AGE
synergychat-web   1/1     1            1           59m
```

- **Viewing Pods:** Use `kubectl get pods` to see the status of the pods.

```bash
NAME                               READY   STATUS    RESTARTS   AGE
synergychat-web-85f945bfdd-d92fn   1/1     Running   0          60m
```

- **Accessing the web page:** Use `kubectl port-forward` with the pod name and the port number to forward the traffic from the cluster to the local network. 

-- `kubectl port-forward PODNAME 8080:8080`

```
kubectl port-forward synergychat-web-f6555699b-bbnc7 8080:8080

```
<li>Minikube vs Prod</li>

- **Minikube vs Production:** Minikube is a single-node cluster for learning Kubernetes, while production clusters are multi-node distributed systems.

- **Distributed Systems:** Systems that involve multiple machines communicating over a network. Kubernetes abstracts away the complexity of distributed systems and does the hard work for you.

- **Resources and Nodes:** Kubernetes manages the resources (CPU, memory, disk space) that applications require and automatically distributes the load across nodes (machines). Kubernetes can scale up the cluster by adding more nodes when needed.



</ol>


