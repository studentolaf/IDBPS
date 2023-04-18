# IDBPS

gd repo clone studentolaf/IDBPS

cd IDBPS/react/v6\ \(working\)/
minikube start
kubectl create namespace spine
kubectl apply -f ./ -n spine
minekube service list
minikube dashboard
