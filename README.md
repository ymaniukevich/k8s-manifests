# How to increase PVC in StatefulSet
- Increase its capacity for each PVC
```bash
    kubectl edit pvc <name> 
```
- Delete the StatefulSet and leave its pods
```bash
    kubectl delete sts --cascade=orphan <name>
```
- Re-create the StatefulSet
```bash
    kubectl apply -f <name>
```
- Restart the pods
```bash
    kubectl rollout restart sts <name>
```
