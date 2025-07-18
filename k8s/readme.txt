# ------------------------------
# 1. Cluster & Context Info
# ------------------------------
kubectl cluster-info
kubectl get nodes
kubectl config current-context
kubectl config get-contexts
kubectl config use-context <context-name>

# ------------------------------
# 2. Namespace Operations
# ------------------------------
kubectl get ns
kubectl create ns <name>
kubectl delete ns <name>
kubectl config set-context --current --namespace=<name>

# ------------------------------
# 3. Pod Management
# ------------------------------
kubectl get pods
kubectl get pods -n <namespace>
kubectl describe pod <pod-name>
kubectl delete pod <pod-name>
kubectl exec -it <pod-name> -- bash
kubectl logs <pod-name>
kubectl logs <pod-name> -c <container-name>

# ------------------------------
# 4. Deployment Management
# ------------------------------
kubectl get deployments
kubectl create deployment <name> --image=<image>
kubectl scale deployment <name> --replicas=<number>
kubectl rollout status deployment/<name>
kubectl rollout undo deployment/<name>
kubectl delete deployment <name>

# ------------------------------
# 5. Service Management
# ------------------------------
kubectl get svc
kubectl expose deployment <name> --type=NodePort --port=80
kubectl describe svc <name>
kubectl delete svc <name>

# ------------------------------
# 6. Configuration Files (YAML)
# ------------------------------
kubectl apply -f <file.yaml>
kubectl delete -f <file.yaml>
kubectl apply -f <file.yaml> --dry-run=client
kubectl get <resource> <name> -o yaml

# ------------------------------
# 7. ConfigMaps & Secrets
# ------------------------------
kubectl create configmap <name> --from-literal=key=value
kubectl get configmap
kubectl create secret generic <name> --from-literal=username=admin
kubectl get secrets
echo <base64_string> | base64 -d

# ------------------------------
# 8. Other Useful Commands
# ------------------------------
kubectl get all
kubectl delete pods --all -n <namespace>
kubectl port-forward <pod-name> 8080:80
kubectl top nodes
kubectl top pods

