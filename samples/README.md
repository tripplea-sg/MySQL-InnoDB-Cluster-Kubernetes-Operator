
---

## Deployment on Kubernetes

1. **Create Namespace**
```
kubectl create ns mysql-cluster
```
2. **Create Service Account**
```
kubectl apply -f k8s-service-account.yaml
```
3. **Apply Roles**
```
kubectl apply -f k8s-role.yaml
```
4. **Apply Role Bindings**
```
kubectl apply -f k8s-role-binding.yaml
```
5. **Apply InnoDB Cluster without PV**
```
kubectl apply -f k8s-mysql-no-disk.yaml
```
6. **Apply InnoDB Cluster with PV**
```
kubectl apply -f k8s-mysql-with-disk.yaml
```
7. **Check InnoDB Cluster Status**
```
kubectl -n mysql-cluster exec -it mysql-0 -- mysqlsh root:root@localhost:3306 -- cluster status
```
8. **Backup Database**
```
kubectl apply -f k8s-mysql-backup.yaml
```
9. **Show Logs**
```
kubectl -n mysql-cluster logs mysql-0 -c agent
```



