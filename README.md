# MERN Webapp Deployed on the Kubernetes Cluster

# Tools Used
🐳 Docker: Docker is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers.The software that hosts the containers is called Docker Engine

GitHub :GitHub is a platform and cloud-based service for software development and version control using Git, allowing developers to store and manage their code. It provides the distributed version control of Git plus access control, bug tracking, software feature requests, task management, continuous integration

☸️ Kubernetes (K8's) : Kubernetes, often abbreviated as K8s, is an open-source container orchestration system for automating software deployment, scaling, and management It was originally designed by Google and is now maintained by the Cloud Native Computing Foundation

Visuals studio : Visual Studio Code is a source-code editor that can be used with a variety of programming languages, including C, C#, C++, Go, Java, JavaScript, Node.js, Python, etc. It is based on the Electron framework.Which is used to develop Node.js web applications that run on the Blink layout engine. Visual Studio Code employs the same editor component used in Azure DevOps

Mongo Express:Mongo Express is a web-based MongoDB admin interface that allows you to manage MongoDB databases interactively.It is written in Node.js, Express.js, and Bootstrap.Mongo Express can be deployed on the Internet, but it requires authentication to prevent unauthorized access

MiniKube :Minikube is a tool that sets up a Kubernetes environment on a local PC or laptop. It creates a VM on your local machine and deploys a simple cluster containing only one node.Minikube is a lightweight Kubernetes implementation that is ideal for testing and development purposes. It is available for Linux, macOS, and Windows systems

Kubernetes (K8's) : Kubernetes, often abbreviated as K8s, is an open-source container orchestration system for automating software deployment, scaling, and management It was originally designed by Google and is now maintained by the Cloud Native Computing Foundation


# Prerequisites Steps

1. Install Kubernetes (K8's)

     Enter below commands to install kubernetes to your local machine.

        For windows - https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/

        For Mac-os - https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/

2. Install minikube

     Enter below commands to install Minikube to your local machine.

        Link for Every operationg system - https://minikube.sigs.k8s.io/docs/start/

3. Install DockerDesktop

        Windows - Install Docker Desktop on Windows | Docker Docs

        Mac - Install Docker Desktop on Mac | Docker Docs

 4. Sign up to Dockerhub

        https://hub.docker.com/signup/
 

 5. Refer sample Deployement file from Official Kubernete's documentation

       https://kubernetes.io/docs/concepts/workloads/controllers/deployment/

6. Refer sample ConfigMap file from Official Kubernete's documentation

       https://kubernetes.io/docs/concepts/configuration/configmap/

 7. Refer sample Secrets file from Official Kubernete's documentation

       https://kubernetes.io/docs/concepts/configuration/secret/     


       
# Interactive Steps

   Step 1 - Download code from the repository in your local machine

   <img width="400" height="400" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/Download%20in%20local.png>
   
   Step 2 - Open VS Code and open folder having your all files

   <img width="400" height="400" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/Screenshot%202023-11-17%20145423.png>

   Step 3 - Open Terminal in VS Code

   <img width="400" height="200" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/Screenshot%202023-11-17%20165956.png>

   Step 4 - Start Minikube using minikube start

   <img width="1000" height="400" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/minikube%20start.png>

   Step 5 - Check for the pods whether is not active by following command

        kubectl get pods
   <img width="1000" height="400" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/get%20pods.png>

   Step 6 - Apply secrets file in the terminal by following command

        kubectl apply -f secret.yaml
   <img width="1100" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/apply%20secrets.png>   

   Step 7 - Apply Config Map file in the terminal by following command

        kubectl apply -f mongo-confiq.yaml
   <img width="1100" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/mongoconfig.png>  

   Step 8 - Apply Mongo app file in the terminal by following command

        kubectl apply -f mongo-app.yaml
         
   <img width="1100" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/mongoapp.png>

   Step 9 - Apply Mongo webapp file in the terminal by following command

        kubectl apply -f web-app.yaml

   <img width="1600" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/webapp.png> 

   Step 10 - To see details of the node which you created in the terminal by following command

        kubectl get node -o wide
   <img width="1500" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/node-o-wide.png>

   Step 11 - You have to expose your service to external world using this command in terminal

        minikube service webapp-service
        
   <img width="1100" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/extrnal%20wrld.png> 

   Step 12 -  Now you can see a login pop up on the screen

        Use This Credentials

         Username - admin

          assword - pass

            As this was mentioned in the ofiicial documentation of the mongo-express in dockerhub
   <img width="900" height="400" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/login.png>     

   Step 13 - Now we can see our application is up and runing in the kubernetes Cluster

   <img width="1100" height="300" src=https://github.com/tohidhanfi20/MERN-Webapp-Deployed-on-the-Kubernetes-Cluster/blob/main/Screenshots/webapp%20(2).png>  
