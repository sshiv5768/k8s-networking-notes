# K8S basic networking concepts

- Pods have their own ips. Containers inside pod use pod's ip for communication. Pods are able to communitcate with each-other using that ip's without any network translations.
- These ip are stored by default in Pod Network.

# CNI - Container Network Interface

- CNI is responsible for setting up pod network and association of Pod IPs.
- CNI uses different plugins for different networking tasks like for pod network management it can use Calico network Plugin and for IPAM( IP Address Management) it can use Calico IPAM plugin.
- When kubelete creates a pod, network plugin creates a pod network and IPAM plugin creates an ip for the pod. Then it transfers the IP to the network plugin which will add that ip to the pod network.

  
