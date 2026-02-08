# lab2-kubernetes
Kubernetes lab demonstrating pods, services, and DNS-based service 



## Screenshot Walkthrough

### 01 – Value and Zone Configuration
![Value and Zone](screenshots/01-value-and-zone.png)
This screenshot shows the active Google Cloud project and compute zone being set and verified before creating the Kubernetes cluster.

---

### 02 – Creating the Cluster
![Create Cluster](screenshots/02-create-clusters.png)
This screenshot captures the command used to create the GKE cluster, including node count and machine configuration.

---

### 03 – Cluster List
![Cluster List](screenshots/03-cluster-list.png)
This screenshot confirms that the GKE cluster was successfully created and is running in the specified zone.

---

### 04 – Nodes
![Nodes](screenshots/04-nodes.png)
This screenshot shows the Kubernetes nodes in the cluster and confirms they are all in the Ready state.

---

### 05 – Authentication Login
![Auth Login](screenshots/05-auth-login.png)
This screenshot shows authentication being verified so that kubectl can interact with the Kubernetes cluster.

---

### 06 – Creating Pods
![Creating Pods](screenshots/06-creating-pods.png)
This screenshot shows the creation of the nginx, server, and client pods within the Kubernetes cluster.

---

### 07 – Verifying Nodes
![Verifying Nodes](screenshots/07-verifying-nodes.png)
This screenshot confirms that the nodes are active and ready to schedule and run pods.

---

### 08 – Localhost Curl Test
![Localhost Curl](screenshots/08-localhost-curl.png)
This screenshot verifies that the nginx web server is running correctly inside the server pod by accessing it through localhost.

---

### 09 – Server Pod IP
![Server Pod IP](screenshots/09-server-pod-ip.png)
This screenshot displays the internal IP address assigned to the server pod, which is needed for direct pod-to-pod communication.

---

### 10 – Pod-to-Pod Communication
![Pod to Pod Curl](screenshots/10-server-pod-ip-curl.png)
This screenshot demonstrates successful communication from the client pod to the server pod using the server pod’s internal IP address.

---

### 11 – Server Service Created
![Server Service](screenshots/11-server-service.png)
This screenshot shows the creation of a Kubernetes Service named server-service to expose the server pod internally.

---

### 12 – Listing Services
![Get Services](screenshots/12-get-services.png)
This screenshot confirms that the server-service appears in the list of Kubernetes services with an assigned ClusterIP.

---

### 13 – Describe Service
![Describe Service](screenshots/13-describe-service.png)
This screenshot provides detailed information about the server-service, including its ClusterIP and backend pod endpoints.

---

### 14 – DNS Client Created
![DNS Client](screenshots/14-dns-client-created.png)
This screenshot shows the creation of a DNS client pod used to test Kubernetes DNS-based service discovery.

---

### 15 – DNS Lookup
![NS Lookup](screenshots/15-ns-lookup.png)
This screenshot demonstrates DNS resolution of the service name server-service to its ClusterIP address.

---

### 16 – Service Name Curl
![Service Curl](screenshots/16-client-curl-server-service.png)
This screenshot confirms that the client pod can successfully access the server using the service name instead of a pod IP.

---

### 17 – Multiple Service Requests
![Multiple Curl](screenshots/17-curl-multiple-request.png)
This screenshot shows multiple successful requests sent through the service, confirming stable routing.

---

### 18 – Resource Deletion
![Delete Resources](screenshots/18-delete.png)
This screenshot documents the deletion of Kubernetes resources such as pods and services as part of cleanup.

---

### 19 – GKE Cluster Deletion
![Delete Cluster](screenshots/19-delete-gke-cluster.png)
This screenshot confirms the deletion of the GKE cluster to ensure no resources remain running after the lab assignment.
