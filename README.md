### Demo Project 🔥

►  Deploying MongoDB and Mongo Express Deployments
►  Create of Secret and Config Map 
►  MongoDB Internal Service
►  Deployment of MongoDB Internal Service and Mongo Express external service


- A ConfigMap is an API object used to store non-confidential data in key-value pairs. Pods can consume ConfigMaps as environment variables.


Workflow followed:

[![workflow.png](https://i.postimg.cc/1X6sspSq/workflow.png)](https://postimg.cc/jnsGhnLx)


#### Deployment:

```
kubectl create namespace hns

kubectl apply -f mongo-secret.yaml
kubectl get secret -n hns
kubectl apply -f mongo-configmap.yaml
kubectl get configmap -n hns
kubectl apply -f mongo.yaml -n hns
kubectl get all -n hns
kubectl apply -f mongo.yaml -n hns
kubectl apply -f mongo-express.yaml -n hns
kubectl get all -n hns

kubectl delete deployment mongo-express -n hns
kubectl delete deployment mongodb-deployment -n hns
kubectl delete service mongodb-service -n hns
kubectl delete service mongo-express-service -n hns
kubectl delete secret mongodb-secret -n hns
kubectl delete configmap mongodb-configmap -n hns
```
