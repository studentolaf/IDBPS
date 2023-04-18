# IDBPS Kubernetes Environment Setup Guide \
This guide is designed to help you set up the IDBPS Kubernetes environment and start up the servers. The IDBPS (Intelligent Distributed Business Processing System) is a platform for processing business transactions using a distributed architecture. Make sure before running the serves to have minkube, docker and kubectl installed. \

1	Docker/Kubernetes install: \
sudo apt update \
sudo apt upgrade \

1.1	Install docker: \
(Delete old versions) \
sudo apt-get remove docker docker-engine docker.io containerd runc \
(Install) \
sudo apt install apt-transport-https ca-certificates curl software-properties-common \
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add – \
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" \
apt-cache policy docker-ce \
sudo apt install docker-ce \
(Make you don’t have to use sudo) \
Sudo usermod -aG docker (username) && newgrp docker \
Sudo apt update \
Reboot 

1.2	Install minikube: \
wget https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64 \
chmod +x minikube-linux-amd64 \
sudo mv minikube-linux-amd64 /usr/local/bin/minikube \
(Install docker cli  for Kubernetes) \
minikube docker-env \
minikube version \
 
1.3	Install kubectl \
curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl \
chmod +x ./kubectl \
sudo mv ./kubectl /usr/local/bin/kubectl \
kubectl version -o json  --client \
Sudo apt update \

2.1 Installation \
Clone the IDBPS repository by running the following command: \
git clone https://github.com/studentolaf/IDBPS.git \


2.2 Navigate to the React application directory by running the following command: \
cd IDBPS/react/v6\ \(working\)/ \


2.3 Start the Minikube cluster by running the following command: \
minikube start \


2.4 Create a new Kubernetes namespace by running the following command:
kubectl create namespace spine


2.5 Apply the IDBPS configuration files to the spine namespace by running the following command:
kubectl apply -f ./ -n spine


2.6 Verify that the IDBPS services are running by running the following command:
minikube service list


2.7 Access the Kubernetes dashboard to manage the IDBPS deployment by running the following command:
minikube dashboard


2.8 Conclusion:
Congratulations! You have successfully set up the IDBPS Kubernetes environment and started up the servers.
