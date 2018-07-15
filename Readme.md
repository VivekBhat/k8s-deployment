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
│   ├── master
│   │   └── Vagrantfile
│   ├── node-1
│   │   └── Vagrantfile
│   └── node-2
│       └── Vagrantfile
├── definitions
│   ├── deployment
│   │   └── deployment-definition.yml
│   ├── pod-definition
│   │   └── pod-definition.yml
│   └── replicaset
│       └── replicaset-definition.yml
└── setup_scripts
    ├── install_docker.sh
    └── install_kubeadm.sh
```

#### boxes:
This has the Vagrantfile for the 3 VMs that I am using. 

##### definitions:
This folder has the various yaml config files that are needed to create the various objects in kubernetes

#### setup_scripts:
If you are doing a pristine install then these scripts can help you setup docker and then kubernetes on the nodes. 

**Note:** Docker and kubernetes are needed in all the nodes and master. We will be using docker 17.03 installation 