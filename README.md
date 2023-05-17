# Distribited Tracing using fluentbit


### Tutorial
[![IMAGE ALT TEXT](http://img.youtube.com/vi/33VEu9Kqvno/0.jpg)](http://www.youtube.com/watch?v=33VEu9Kqvno "Logging in Kubernetes | Fluent Bit | Observability")

### Installation

Fluent Bit must be deployed as a DaemonSet, so on that way it will be available on every node of your Kubernetes cluster. To get started run the following commands to create the namespace, service account and role setup:


**1.** We will first setup the required role, rolebinding, namespace and service-account/
For Kubernetes v1.21 and below
```bash
kubectl apply -f install/v1.21
```
For Kubernetes v1.22
```bash
kubectl apply -f install/v1.22
```

**2.** After setting up the required kubernetes objects, we can now install the fluentbit(daemonsets) and it's configuration (configmap).
```bash
kubectl apply -f ./fluentbit/
```
