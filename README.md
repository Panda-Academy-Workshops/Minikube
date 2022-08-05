# Overview
Minikube + ArgoCD Vagrant - virtual machine environment, defined in code

## Running the example 

* Clone the repository and run `vagrant up` - this will set up the basic vagrant machine with tools installed for the course
* Run the `vagrant provision` on the running machine for update  
* Run the `vagrant destroy` to destroy the machine

1. The Argo CD application is deployed automatically on Minikube. During the vagrant up or vagrant provision, the password to argoCD will be shown on the screen.
2. In the browser go to **192.168.44.45:8080** and log in using credentials: username: `admin`, password: use password from the 1. step

In case you lost the password, you can ssh into vagrant (`vagrant ssh`) and run the following command to retrieve the password:
`sudo kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo`