1. Add the Datadog Helm Repo
```
helm repo add datadog https://helm.datadoghq.com
```

2. Install the Helm Repo
```
helm install datadog --set datadog.site='datadoghq.com' --set datadog.apiKey='02f652f21ce87cbca983ed36de55b676' datadog/datadog 
```

3. Once installed, go to Datadog and click on Infrastructure -> Kubernetes

You'll see all of the information about your cluster.