# kubernetes-postgres

Repository to deploy a PostgreSQL database on Kubernetes cluster

# Generate the mysql root password
```
kubectl create secret generic postgres-pass --from-literal=password=<PASSWORD> -n postgres
```

# Databases
Once the PostgreSQL instance is deployed, databases and users must have to be created manually.
Execute the following commands to connect to the PostgreSQL instance:
```
CREATE USER username PASSWORD <PASSWORD>;
CREATE DATABASE database OWNER=username;
```
