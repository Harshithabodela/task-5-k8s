# Task 5 – Kubernetes with Minikube

## Objective
Deploy and manage applications in a Kubernetes cluster using Minikube.

## Steps Performed

1. **Installed Minikube and kubectl**.
2. **Started Minikube Cluster**:
   ```bash
   minikube start
   ```
3. **Created a ConfigMap** using `configmap.yaml`:
   ```bash
   kubectl apply -f configmap.yaml
   ```
4. **Created a Deployment** using `deployment.yaml`:
   ```bash
   kubectl apply -f deployment.yaml
   ```
5. **Exposed the Application** using `service.yaml`:
   ```bash
   kubectl apply -f service.yaml
   ```
6. **Verified Pods and Services**:
   ```bash
   kubectl get pods
   kubectl get services
   ```
7. **Scaled the Deployment**:
   ```bash
   kubectl scale deployment myapp-deployment --replicas=3
   ```
8. **Described Resources for Logs and Status**:
   ```bash
   kubectl describe deployment myapp-deployment
   kubectl logs <pod-name>
   ```
9. **Updated the Deployment Image**:
   ```bash
   kubectl set image deployment myapp-deployment myapp-container=nginx:1.22
   kubectl rollout status deployment myapp-deployment
   ```
10. **Rolled Back the Deployment (if needed)**:
   ```bash
   kubectl rollout undo deployment myapp-deployment
   ```
11. **Deleted All Resources**:
   ```bash
   kubectl delete -f deployment.yaml
   kubectl delete -f service.yaml
   kubectl delete -f configmap.yaml
   ```

## Outcome
Successfully deployed, exposed, and scaled an application on a local Minikube cluster.
<img width="1440" alt="Screenshot 2025-04-14 at 8 57 26 PM" src="https://github.com/user-attachments/assets/2283576e-bec6-417f-a070-4cc0d1ef55ae" />
<img width="1440" alt="Screenshot 2025-04-14 at 8 57 38 PM" src="https://github.com/user-attachments/assets/4d37ba38-ed32-4348-b242-de656222e409" />



## Files Included
- `deployment.yaml` – Kubernetes deployment configuration  
- `service.yaml` – Kubernetes service definition  
- `configmap.yaml` – Kubernetes ConfigMap definition  
- `README.md` – Documentation of the task
