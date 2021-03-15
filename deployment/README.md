#Deployment

kubectl create -f deployment.yml

    kubectl get deployment

Update the nginx image with new version 1.19

    kubectl set image deployment/nginx-deployment nginx=nginx:1.19 --record=true
    
Check the history of deployment

     kubectl rollout history deployment/nginx-deployment
     
     
Check the status of deployment   

    kubectl rollout status deployment/nginx-deployment
    
 Undo the deployment and move it to previous version of deployment
 
 
    kubectl rollout undo deployment/nginx-deployment
 
   
