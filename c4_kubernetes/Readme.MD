kubectl apply -f .\config.yml



kubectl apply -f .\roles\web\web-role.yml -f .\roles\web\web-role-binding.yml 
kubectl delete -f .\roles\web\web-role.yml -f .\roles\web\web-role-binding.yml 


kubectl apply -f .\roles\api\api-role.yml -f .\roles\api\api-role-binding.yml 
kubectl delete -f .\roles\api\api-role.yml -f .\roles\api\api-role-binding.yml 


kubectl delete -f .\tripviewer\tripviewer-deployment.yml -f .\tripviewer\tripviewer-service.yml
kubectl apply -f .\tripviewer\tripviewer-deployment.yml -f .\tripviewer\tripviewer-service.yml


kubectl apply -f .\poi\poi-deployment.yml -f .\poi\poi-service.yml
kubectl delete -f .\poi\poi-deployment.yml -f .\poi\poi-service.yml


kubectl apply -f .\user\user-deployment.yml -f .\user\user-service.yml
kubectl delete -f .\user\user-deployment.yml -f .\user\user-service.yml




kubectl apply -f .\userprofile\userprofile-deployment.yml -f .\userprofile\userprofile-service.yml
kubectl delete -f .\userprofile\userprofile-deployment.yml -f .\userprofile\userprofile-service.yml


kubectl apply -f .\trips\trips-deployment.yml -f .\trips\trips-service.yml
kubectl delete -f .\trips\trips-deployment.yml -f .\trips\trips-service.yml



kubectl rollout restart deployment poi -n anupam
kubectl rollout restart deployment user -n anupam
kubectl rollout restart deployment userprofile -n anupam
kubectl rollout restart deployment trips -n anupam
kubectl rollout restart deployment tripviewer -n anupam