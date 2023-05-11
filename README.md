# IDBPS Kubernetes Environment Setup Guide 
This guide is designed to help you set up the IDBPS Kubernetes environment and start up the servers. Make sure before running the serves to have minkube, docker and kubectl installed on your Linux machine. 

1.1 Installation \
Clone the IDBPS repository by running the following command: \
git clone https://github.com/studentolaf/IDBPS.git 


1.2 Navigate to the React application directory by running the following command: \
cd IDBPS/react/v6\ \(working\)/ 


1.3 Start the Minikube cluster by running the following command: \
minikube start 


1.4 Create a new Kubernetes namespace by running the following command: \
kubectl create namespace spine 


1.5 Apply the IDBPS configuration files to the spine namespace by running the following command: \
kubectl apply -f ./ -n spine 


1.6 Verify that the IDBPS services are running by running the following command: \
minikube service list 


1.7 Access the Kubernetes dashboard to manage the IDBPS deployment by running the following command: \
minikube dashboard 


1.8 Conclusion: \
Congratulations! You have successfully set up the IDBPS Kubernetes environment and started up the servers. 
