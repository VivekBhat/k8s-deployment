## Kubernetes Deployments

This is a repo of me experimenting with Kubernetes deployments and performing some of the know deployment strategies like Rolling Updates, Blue Green deployment etc for a web application

## Infrastructure
To perform this test you will need 1 master server and 2 worker nodes.

(You can also work with a single node and use minikube to setup the master and worker nodes on the same server)

There are various known ways to setup the infrastructure like:
1. Cloud providers like Amazon Web Services, Google Cloud etc
2. Virtual Machines

#### I am using Vagrant to spin up 3 Virtual Machines on a Mac


## Folder Structure

```
.
├── Readme.md
├── boxes
│   ├── Readme.md
│   ├── master
│   │   └── Vagrantfile
│   ├── master-2
│   │   └── Vagrantfile
│   ├── node-1
│   │   └── Vagrantfile
│   └── node-2
│       └── Vagrantfile
├── definitions
│   ├── deployment
│   │   ├── Readme.md
│   │   └── deployment-definition.yml
│   ├── pod-definition
│   │   ├── Readme.md
│   │   └── pod-definition.yml
│   └── replicaset
│       └── replicaset-definition.yml
├── example-voting-app-kubernetes
│   ├── pods
│   │   ├── postgres-pod.yml
│   │   ├── redis-pod.yml
│   │   ├── result-app-pod.yml
│   │   ├── voting-app-pod.yml
│   │   └── worker-app-pod.yml
│   └── services
│       ├── postgres-service.yml
│       ├── redis-service.yml
│       ├── result-app-service.yml
│       └── voting-app-service.yml
├── resources
│   └── nodes.png
└── setup_scripts
    ├── install_docker.sh
    └── install_kubeadm.sh

14 directories, 23 files

```

### Folders
#### 1. boxes:
* **master:** This has the Vagrantfile for the master node
* **master-2:** This has the Vagrantfile for the second master node
* **node-1:** This has the Vagrantfile for the first worker node
* **node-2:** This has the Vagrantfile for the second worker node

#### 2. definitions:
This folder has the various yaml config files that are needed to create the various objects in kubernetes along with a Readme for the various useful commands

#### 3. setup_scripts:
If you are doing a pristine install then these scripts can help you setup docker and then kubernetes on the nodes. 

**Note:** Docker and kubernetes are needed in all the nodes and master. We will be using docker 17.03 installation 