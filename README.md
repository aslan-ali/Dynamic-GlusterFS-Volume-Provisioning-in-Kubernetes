# Dynamic-GlusterFS-Volume-Provisioning-in-Kubernetes
0 5o5Nhhs9MEklWDd-.png


Firstly we install 3 glusterfs servers and 1 heketi RestAPI

1) Glusterfs_Servers (3 nodes):

configuration file:  glusterfs_servers_config

2) GlusterFs_Client(Example: K8S):

configuration file: glusterfs_k8s_config

3) Heketi RestAPI ( 1 node):

configuration file: heketi_restapi

4) Create cluster , nodes , and device for dynamic volume provisioning in Heketi node:

configuration file: heketi_gluster_config

5) K8s Pod, StorageClass, PVC 

configuration file: deployment.yml


NOTE: Version GlusterFS server and client on K8S nodes must match.



#for testing:
kubectl exec -it busybox -- sh           #because my pod is busybox, and folder /data
cd data
touch file.txt


#delete pod 
kubectl get pod busybox -o yaml > pod.yml
kubectl delete pod busybox
kubectl apply -f pod.yml
kubectl exec -it busybox -- sh
cd data

#and if you see there file.txt , it's mean that your GlusterFS volume provisioning works correctly!!!

That's all! Thanks!
