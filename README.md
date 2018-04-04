# Kubernetes à la dure

Ce tutoriel est une traduction et une adaptation du fameux [Kubernetes The Hard Way](https://github.com/kelseyhightower/kubernetes-the-hard-way). Ce guide permet de comprendre, pas à pas, comment installer un cluster Kubernetes.

Si vous recherchez une installation automatisée, je vous conseille de vous orienter vers [Google Kubernetes Engine](https://cloud.google.com/kubernetes-engine), ou [Getting Started Guides](http://kubernetes.io/docs/getting-started-guides/).

De nombreux projets permettent d'installer Kubernetes de facon automatisée. Par exemple:
|Outil|Plateforme|
|-----|----------|
|[Kubespray](https://github.com/kubernetes-incubator/kubespray)|AWS, GCP, Azure, OpenStack, Baremetal, VMware|
|[Kops](https://github.com/kubernetes/kops)|AWS, GCP, VMware|


> Ce tutorial ne doit pas être considéré comme "production ready" et il se peut qu'il ne soit pas supporté par la communauté mais ne vous arrètez pas à cela. Rien ne doit vous empècher d'apprendre !

## Public concerné

Toute personnes qui prévoit d'installer ou devra opérer un cluster Kubernetes en production devrait faire ce toturiel afin d'en comprendre tout les méchanismes sous-jacents. 

## Détail sur le cluster

"Kubernetes à la dure" vous guidera pour créer un cluster Kubernetes hautement disponible (HA) avec des communications chiffrées et de l'authentification (RBAC).

* [Kubernetes](https://github.com/kubernetes/kubernetes) 1.9.0
* [cri-containerd Container Runtime](https://github.com/kubernetes-incubator/cri-containerd) 1.0.0-beta.0
* [CNI Container Networking](https://github.com/containernetworking/cni) 0.6.0
* [etcd](https://github.com/coreos/etcd) 3.2.11

## Labs

Ce tutoriel nécessite un compte à la console [Google Cloud Platform](https://cloud.google.com). Ce tutoriel peut évidement être appliquè sur n'importe quelle plateforme.

* [Prérequis](docs/01-prerequisites.md)
* [Installer les outils nécessaires](docs/02-client-tools.md)
* [Provisionner l'infrastructure](docs/03-compute-resources.md)
* [Générer et provisionner la CA et les certificats TLS](docs/04-certificate-authority.md)
* [Générer et provisionner les fichiers de configuration pour l'authentification](docs/05-kubernetes-configuration-files.md)
* [Générer et provisionner la configuration pour le chiffrement des données](docs/06-data-encryption-keys.md)
* [Démarrer le cluster etcd](docs/07-bootstrapping-etcd.md)
* [Démarrer le Control Plane](docs/08-bootstrapping-kubernetes-controllers.md)
* [Démarrer les Worker nodes](docs/09-bootstrapping-kubernetes-workers.md)
* [Configurer kubectl pour accéder au cluster](docs/10-configuring-kubectl.md)
* [Provisioning Pod Network Routes](docs/11-pod-network-routes.md)
* [Deploying the DNS Cluster Add-on](docs/12-dns-addon.md)
* [Tests](docs/13-smoke-test.md)
* [Désinstaller](docs/14-cleanup.md)
