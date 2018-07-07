### Useful commands:

`kubectl get all` 

`kubectl create -f deployment-definition.yml` This will create a new deployment based on your yaml file

`kubectl rollout status deployment/myapp-deployment` to check the background process for rolling updates

`kubectl rollout history deployment/myapp-deployment`

`kubectl delete deployment/myapp-deployment` To delete the deployment

`kubectl create -f deployment-definition.yml --record` to record the CHANGE-CAUSE

OR

`kubectl create --filename=deployment-definition.yml --record=true`


### Updating the image:

kubectl set image deployment/myapp-deployment nginx-container=nginx:1.14


### Undoing the deployment

```
kubectl rollout undo deployment/myapp-deployment

kubectl rollout history deployment/myapp-deployment
```