
This is a Node application that allows us to create and log in users

We have the user and the auth API applications
The user API will communicate with the Auth API
The Auth Api should not be accessible to the public 

We have different K8S manifests (svc,deployment)  have one for the user and the auth API applications

user-app.js is directing traffic to Nodeport 

port 3000 via port 80

Auth service is type cluster IP

---
in the users.yaml, I am providing a mongo db connection, you can see the connection strings in the users-app.js file. see line 33...

...TO TRY THIS ON YOUR OWN, go to mongodb.com, create your own cluster, click connect, get the connection strings and try connecting with those info.
Get more from video 244... preparing the starting project

build the respective images and push to dockerhub


https://www.udemy.com/course/docker-kubernetes-the-practical-guide/learn/lecture/22628015#overview

EFS
Add Volume by installing the
- EFS driver.
kubectl apply -k "github.com/kubernetes-sigs/aws-efs-csi-driver/deploy/kubernetes/overlays/stable/?ref=release-1.4" 

- Add EFS File System

SO, SC, PV, PVC, EFS Driver, Pod