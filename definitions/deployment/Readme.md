Useful commands:

`kubectl get all` 

`kubectl create -f deployment-definition.yml` This will create a new deployment based on your yaml file

`kubectl rollout status deployment/myapp-deployment` to check the background process for rolling updates

`kubectl rollout history deployment/myapp-deployment`

`kubectl delete deployment/myapp-deployment` To delete the deployment

`kubectl create -f deployment-definition.yml --record` to record the CHANGE-CAUSE