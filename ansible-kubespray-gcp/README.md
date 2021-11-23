# Deploy a Production Ready Kubernetes Cluster 

![Kubernetes Logo](https://raw.githubusercontent.com/kubernetes-sigs/kubespray/master/docs/img/kubernetes-logo.png)

### Overview
The goal of this project is the end to end automation of a Google Kubernetes cluster using minimal involvement barring a supplied, customized, yml file

# Getting Started
## Prerequisites
*  Install local dependencies `python-google-auth, gcloud, ansible`
*  Create an account at cloud.google.com
*  Setup account - including gcloud auth
*  Create a new project with name `this name should be standardized`
*  Under IAM&Admin click service account
*  Create service account, add roles `compute project admin` and `network admin`
*  Click action and add JSON key
*  Download Json Key and store it in $HOME directory
*  `git clone <repo>`
*  `ansible-playbook -i inventories/all/all.yml site.yml` 

## TODO
* Update the OS image to use Fedora CoreOS
* Create a prep_bastion playbook to install local dependencies and configure gcloud account
* Using the gcloud api, generate a hosts file of the cluster nodes
* Copy private ssh key to each node
* Request input from end-user as to cluster details
