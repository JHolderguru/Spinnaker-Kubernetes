### Kubernetes: Continuos Delivery with Spinnaker

#### K8s 
#### the K8s is about taking a bunch of VM and transforming them into a unified API surface which the developer can ochestrate their applications without thinking about the machines that lie below.
#### Pod - containers co-located on a single machine.
#### service - loadbalancer which can bring traffic down to a collection of pods.
#### Deployment - which under the hood uses a replica set (replicating a container a number of times for availabuity or scale)

#### HTTP call to the K8 server to get the right amount to deploy (.yml)
#### The deployment talks to the the service which load balances the traffic to the containers.If this service is attached to an external load balancer
#### K8 is responsible for talking to the cloud and request that the ext load balancer come into existance so that you get the ip adress which maps to the cloud LB which then maps to the service and be LB to all the containers.
#### We go into the deployment and change the deployment from 3 to 4 containers,the k8s self healing changes it from 3-4, traffic flows from the service to the 4 containers without the end user noticing.
#### We can even upgrade the containers without the end user noticing at all.