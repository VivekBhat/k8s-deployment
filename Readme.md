This is a repo of me experimenting with Kubernetes deploymentd and rolling updates for a web application

The folder structure:

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
├── scratch
└── setup_scripts
    ├── install_docker.sh
    └── install_kubeadm.sh
```