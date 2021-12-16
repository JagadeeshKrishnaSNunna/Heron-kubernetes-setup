minikube start --memory=7168 --cpus=5 --disk-size=20G
alias kubectl="minikube kubectl --"
docker pull apache/heron:0.20.4-incubating
kubectl create -f zookeeper.yaml
kubectl create -f bookkeeper.yaml
kubectl create -f heronTool.yaml
kubectl create -f heronAPIServer.yaml
kubectl proxy -p 8001
