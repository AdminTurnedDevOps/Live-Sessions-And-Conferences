https://docs.portainer.io/start/install/server/kubernetes/baremetal

```
Portainer [main] ⚡ kubectl apply -f https://downloads.portainer.io/ee2-16/portainer-agent-k8s-lb.yaml

namespace/portainer created
serviceaccount/portainer-sa-clusteradmin created
clusterrolebinding.rbac.authorization.k8s.io/portainer-crb-clusteradmin created
service/portainer-agent created
service/portainer-agent-headless created
deployment.apps/portainer-agent created
```

```
kubectl get svc -n portainer
```