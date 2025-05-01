# kubernetes-notes
"My summary of Kubernetes architecture with examples"


📄 Kubernetes Architecture Summary
🔧 Overview
Kubernetes is divided into two main components:

Control Plane (Master)

Worker Nodes (Data Plane)

🧠 Control Plane Components
API Server: Exposes Kubernetes to the outside world and handles requests.

Scheduler: Decides where to deploy new pods.

Etcd: Stores all cluster data as key-value pairs.

Controller Manager: Handles ReplicaSets, autoscaling, and state.

Cloud Controller Manager: Connects Kubernetes to cloud services (not needed on-premise).

⚙️ Worker Node Components
Kubelet: Ensures pods are running and reports failures.

Kube-Proxy: Distributes network traffic using IPTables.

Container Runtime: Runs containerized applications (e.g., CRI-O, containerd, Docker).

💡 Example Setup
Component	Node Type	Role
API Server	Control Plane	Handles requests
Scheduler	Control Plane	Assigns pods to nodes
Etcd	Control Plane	Stores cluster state
Kubelet	Worker Node	Monitors and manages pods
Kube-Proxy	Worker Node	Network load balancing
Container Runtime	Worker Node	Runs containers

✅ Key Takeaways
Kubernetes is self-healing through kubelet + controllers.

Docker is not required; Kubernetes supports multiple runtimes.

Control plane = decision-maker, worker nodes = action executors.

Scroll down, write a commit message like Add Kubernetes architecture summary

Click “Commit changes”

