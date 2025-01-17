# Deployment on kubernetes 

## Déploiement du pod webapp-color 

````Bash
   kubectl apply -f pod.yml
   kubectl port-forward webapp-color 8080:8080 --address 0.0.0.0 # Exposition du pod pour qu'il soit accessible
````

## Déploiement du nginx-deployment 

````Bash
   kubectl apply -f nginx-deployment.yml
   kubectl describe deploy nginx-deployment # Voir les informations sur le déploiement effectué
   kubectl get pods
   kubectl get deployment
````

### Déploiement avec les commandes impératives

````Bash
   kubectl run webapp-color --image=mmumshad/simple-webapp-color:latest --port=8080 --env="APP_COLOR=red"
   kubectl port-forward webapp-color 8080:8080 --address 0.0.0.0 # Exposition du pod pour qu'il soit accessible
   kubectl create deployment nginx-deployment --image=nginx:1.18.0 --port=80 --replicas=2
````
