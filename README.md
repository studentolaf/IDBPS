#IDBPS Kubernetes Environment Setup Guide
This guide is designed to help you set up the IDBPS Kubernetes environment and start up the servers. The IDBPS (Intelligent Distributed Business Processing System) is a platform for processing business transactions using a distributed architecture.

Installation
Clone the IDBPS repository by running the following command:
git clone https://github.com/studentolaf/IDBPS.git

Navigate to the React application directory by running the following command:
cd IDBPS/react/v6\ \(working\)/

Start the Minikube cluster by running the following command:
minikube start

Create a new Kubernetes namespace by running the following command:
kubectl create namespace spine

Apply the IDBPS configuration files to the spine namespace by running the following command:
kubectl apply -f ./ -n spine

Verify that the IDBPS services are running by running the following command:
minikube service list

Access the Kubernetes dashboard to manage the IDBPS deployment by running the following command:
minikube dashboard

Conclusion:
Congratulations! You have successfully set up the IDBPS Kubernetes environment and started up the servers.
