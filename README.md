ReplicaSet Deployment: Managing NGINX Pods in Kubernetes
A ReplicaSet in Kubernetes manages multiple identical pod replicas to ensure a specified number of replicas are always running.

Task
We will create a ReplicaSet with the following configuration:

-name: nginx-replicaset
-image: nginx:latest
-replicas: 3


Creating the ReplicaSet


Verify Replicasets and Pods
Once the ReplicaSet is deployed, we can manage it using kubectl commands.ReplicaSet ensures the the number of pods with labels nginx is always 3.If any of the pods were accidently destroyed or deleted,it will automatically generate the pod by using the template provided in definition file.

To view the replicasets and pods managed by replicset use this commands:
--kubectl get replicasets 
--kubectl get pods  --selector=app=nginx


