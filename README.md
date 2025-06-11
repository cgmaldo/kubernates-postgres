# Ejemplo Kubernates Postgres + pgadmin

## 1) Instalacion minikube
- curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
- sudo dpkg -i minikube_latest_amd64.deb
- minikube version

## 2) Instalación de kubectl
- Método 1:
minikube kubectl
minikube kubectl -- version

- Método 2:
	https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/
	kubectl version

## 3) Arrancar 
- minikube start
- docker container ls -a

## 4) Aplicar ficheros de configuración al cluster
- kubectl apply -f postgres-config.yml
- echo -n <string> | base64
- kubectl apply -f postgres-secrets.yml
- kubectl apply -f postgres.yml
- kubectl get all
- kubectl describe <id>
- kubectl logs <id>
- kubectl apply -f pg-admin-secrets.yml
- kubectl apply -f pg-admin.yml
- kubectl get all
- minikube service pg-admin-service
- kubectl apply -f backend-secrets.yml
- kubectl apply -f backend.yml
- minikube service backend-service

## 5) Para pulgar el cluster y eliminar toda información
- minikube delete --all