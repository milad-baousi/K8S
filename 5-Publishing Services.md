## Publishing Services (ServiceTypes)
For some parts of your application (for example, frontends) you may want to expose a Service onto an external IP address, that's outside of your cluster.

Kubernetes ServiceTypes allow you to specify what kind of Service you want.

**Type values and their behaviors are**

- ClusterIP: Exposes the Service on a cluster-internal IP. Choosing this value makes the Service only reachable from within the cluster.
 This is the default that is used if you don't explicitly specify a type for a Service.
 
- NodePort: Exposes the Service on each Node's IP at a static port (the NodePort). To make the node port available, Kubernetes sets up a cluster IP address,
 the same as if you had requested a Service of type: ClusterIP.
 (Listen a port and publish - publish for all server)
  - target port : port that listen on POD
  - port : port that listen on service
  - nod port : port that listen on nod 
  
- LoadBalancer: Exposes the Service externally using a cloud provider's load balancer.
  - need a publiv ip address from provider on cluster
  - 

- ExternalName: Maps the Service to the contents of the externalName field (e.g. foo.bar.example.com), by returning a CNAME record with its value.
 No proxying of any kind is set up.
  - use name 
Exteral ip have all functinality of publish service
