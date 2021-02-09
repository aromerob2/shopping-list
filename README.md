Shopping List

Simple shopping list developed using Vue.
It allows to add items to the shopping list (default list provided), edit or delete them.
Items can be checked so you know you already bougthy it.
List can not be saved since is not connected with any database

Also a docker image exists, so you can run it locally with docker:
 - docker run -d -p 8080:80 --name shopping-list arzur88/shopping-list:v0
Or you can create a kubernetes deployment and a service to expose it. For instance:
 - kubectl create deployment shopping-list --image=arzur88/shopping-list:v0 --replicas=1 --dry-run=client -o yaml > shopping_deployment.yaml
 - kubectl create -f shopping_deployment.yaml
 - kubectl expose deployment shopping-list --type=NodePort --port=80 --dry-run=client -o yaml > shopping_service.yaml
 - kubectl create -f shopping_service.yaml


