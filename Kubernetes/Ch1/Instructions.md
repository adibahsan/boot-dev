<ol>

<li> **Minikube** </li>

- **Minikube Config:** minikube start --extra-config "apiserver.cors-allowed-origins=["http://boot.dev"]"
- minikube version
- **Minikube Dashboard:** to check minikube's version -

```cmd
minikube dashboard
```

<li>DEPLOYING SYNERGYCHAT</li>

- **Deploying an image:** Use `kubectl create deployment` with the name of the deployment and the ID of the Docker image.

- **Viewing deployments:** Use `kubectl get deployments` to see the status of the deployments.

- **Accessing the web page:** Use `kubectl port-forward` with the pod name and the port number to forward the traffic from the cluster to the local network.

- **Testing the HTTP requests:** Use the text box and the button to run the HTTP tests on the web page, and check the results below.

- **Asking Boots a question:** Use the chat box at the bottom to ask Boots the Bear with a Back-End for help or clarification on any topic related to the tutorial.


</ol>


