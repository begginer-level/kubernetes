1. create ec2 instance
2. install aws cli in your local system
3. connect the ec2 instance
4. install eksctl by using below commands 
EKSCTL INSTALLATION COMMANDS ON EC2:
curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" -o eksctl.tar.gz && \
tar -xzf eksctl.tar.gz && \
sudo mv eksctl /usr/local/bin && \
eksctl version
5. AFTER DONE WITH INSTALLATION WE NEED TO CRAETE CLUSTER 
eksctl create cluster --name demo-cluster --region us-east-1

DELETE THE CLUSTER
eksctl delete cluster --name demo-cluster --region us-east-1

6. NOW INSTALL KUBECTL ON EC2
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && \
chmod +x kubectl && \
sudo mv kubectl /usr/local/bin/ && \
kubectl version --client

7. CONNECT TO YOUR EKS CLUSTER
aws eks update-kubeconfig --region us-east-1 --name your-cluster-name

THIS CREATES A KUBECONFIG FILE
~/.kube/config

8. VERIFY CLUSTER CREATION
kubectl get nodes

9. NOW WRITE SOME YAML FILES 
10. CREATE A REPO IN GITHUB
11. AFTER CREATING YAML APPLY BELOW COMMANDS
$ git init
$ git branch -M main
$ git remote add origin <repo_url>
$ git add . ; git commit -m "msg" ; git push origin main

12. now check the installations are completed or not 

13. now again clone the repo

14. apply the yaml 
ex:
$ kubectl apply -f namespace.yaml
15. check using 
$ kubectl get namespaces
