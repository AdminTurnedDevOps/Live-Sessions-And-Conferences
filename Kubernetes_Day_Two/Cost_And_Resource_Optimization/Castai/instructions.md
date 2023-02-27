1. Sign up for free to use Cast.ai
https://cast.ai/

2. Install Cast.ai on your k8s cluster
```
curl -H "Authorization: Token (you'll get this from your Cast.ai dashboard when you signed up) "https://api.cast.ai/v1/agent.yaml?provider=aks" | kubectl apply -f -
```

3. Go to your Cast.ai dashboard and you'll now see your cluster.