# mongodb-in-eks-with-ingressController
you can create 👷  mongodb deployment in eks using nginx ingress controller . have fun 👊🏼 !!!

step 1: First create the secret for both the mongo and express deployment 

step 2: create configmap which will hold the value of the mongo url which would be mongodb service name.

step 3: now install the ingress controller using helm  

use helm chart to install ingress controller use the following command  
----------------------------------------------------------------------
helm upgrade --install ingress-nginx ingress-nginx \
  --repo https://kubernetes.github.io/ingress-nginx \
  --namespace ingress-nginx --create-namespace

step 4: in this step you can create mongodb and related service using 'mongodb-deployment.yaml' 
 kubectl apply -f mongodb-deployment.yaml

step 5: After creating the db now we can deploy the mongodb ui which is mongoexpress using the mongoExpress-with-ingress-deployment.yaml 

step 6: You can find the ingress using "kubectl get ingress -n yournamespace" and wait for the load balancer address from aws . now create a record in route53. 


get to work . have fun 🥳 
