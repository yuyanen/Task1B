# TIC3001 Task1B
Command for Task1B

1.4 : 
Run “kind create cluster --name kind-1 --config k8s/kind/cluster-config.yaml”
Run “kubectl cluster-info”
Run “kubectl get nodes”

1.5 : 

 Build docker image
 docker build -t task1b ./app/.


Load image
kind load docker-image task1b --name kind-1

Add cluster-config.yaml (Task1.4 done), backend-deployment.yaml and backend-service.yaml files
Run  “kubectl apply -f k8s/manifests/k8s/backend-deployment.yaml”
Run “kubectl apply -f k8s/manifests/k8s/backend-service.yaml”
Run “kubectl get svc”

1.6 :

Run “kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml”
Run “kubectl -n ingress-nginx get deploy -w”
Run “kubectl apply -f k8s/manifests/k8s/backend-ingress.yaml”
Run “kubectl get ingress”
Browse “http://localhost/app”

