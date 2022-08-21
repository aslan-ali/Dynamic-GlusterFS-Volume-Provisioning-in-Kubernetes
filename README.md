# Dynamic-GlusterFS-Volume-Provisioning-in-Kubernetes


Firstly we install 3 glusterfs servers and 1 heketi RestAPI

1) Glusterfs_Servers (3 nodes):

configuration file:  glusterfs_servers_config

2) GlusterFs_Client(Example: K8S):

configuration file: glusterfs_k8s_config

3) Heketi RestAPI ( 1 node):

configuration file: heketi_restapi

4) K8s Pod, StorageClass, PVC 

configuration deployment.yml