# Distribited Tracing using fluentbit


### Tutorial
[![IMAGE ALT TEXT](http://img.youtube.com/vi/33VEu9Kqvno/0.jpg)](http://www.youtube.com/watch?v=33VEu9Kqvno "Logging in Kubernetes | Fluent Bit | Observability")

### Installation

Fluent Bit must be deployed as a DaemonSet, so on that way it will be available on every node of your Kubernetes cluster. To get started run the following commands to create the namespace, service account and role setup:
For Kubernetes v1.21 and below
```bash
kubectl create namespace logging
kubectl create -f https://raw.githubusercontent.com/fluent/fluent-bit-kubernetes-logging/master/fluent-bit-service-account.yaml
kubectl create -f https://raw.githubusercontent.com/fluent/fluent-bit-kubernetes-logging/master/fluent-bit-role.yaml
kubectl create -f https://raw.githubusercontent.com/fluent/fluent-bit-kubernetes-logging/master/fluent-bit-role-binding.yaml
```
For Kubernetes v1.22
```bash
kubectl create namespace logging
kubectl create -f https://raw.githubusercontent.com/fluent/fluent-bit-kubernetes-logging/master/fluent-bit-service-account.yaml
kubectl create -f https://raw.githubusercontent.com/fluent/fluent-bit-kubernetes-logging/master/fluent-bit-role-1.22.yaml
kubectl create -f https://raw.githubusercontent.com/fluent/fluent-bit-kubernetes-logging/master/fluent-bit-role-binding-1.22.yaml
```
