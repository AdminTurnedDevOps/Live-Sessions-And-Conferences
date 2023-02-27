1. Add the Datadog Helm Repo
```
helm repo add datadog https://helm.datadoghq.com
```

2. Install the Helm Repo
```
helm install datadog --set datadog.site='datadoghq.com' --set datadog.apiKey='your_database_api_key' datadog/datadog 
```

3. Once installed, go to Datadog and click on Infrastructure -> Kubernetes

You'll see all of the information about your cluster.