# k8_p3
Problem #3 (Kubernetes)

## Minikube installation
1) Refer to https://kubernetes.io/docs/tasks/tools/install-minikube/ for installation steps.
2) Before the installation, ensure the preferred hypervisor (virtualbox is preferred) is installed on your local machine unless you would like to install it on the local machine without hypervisor. In this case, you need docker or podman for minikube to run on the local machine.
3) Next, download the minikube binary following the steps of the OS of your local machine, in my case MacOS, `$ curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-amd64` then make the file executable `$ chmod +x minikube`. Lastly, add the minikube to  your path `$ sudo mv minikube /usr/local/bin/`.

## Kubectl installation
1) In order to interact with your minikube cluster, the Kubernetes CLI tool `kubectl` is needed to deploy applications, inspect and manage cluster resources, and view logs.
2) Refer to https://kubernetes.io/docs/tasks/tools/install-kubectl/#before-you-begin for installation steps.
3) Again, since I'm using MacOS, download the binary `$ curl -LO "https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/darwin/amd64/kubectl"` then make the file executable `$ chmod +x ./kubectl`. Lastly, add the kubectl to your path `$ sudo mv ./kubectl /usr/local/bin/kubectl`

## Bring up the KUBE!
1) Once minikube and kubectl binaries are ready, it's time to bring up the minikube cluster (i mean node..). 
2) In the terminal, run `minikube start --driver=<driver_name>`, the driver_name is the name of the hypervisor installed on the local machine. eg. virtualbox
3) Check that the minikube node is running normally by running `minikube status`. If the output is like this, it's all set!
```
host: Running
kubelet: Running
apiserver: Running
kubeconfig: Configured
```
## Deploy the Nginx and expose it as service
1) 
