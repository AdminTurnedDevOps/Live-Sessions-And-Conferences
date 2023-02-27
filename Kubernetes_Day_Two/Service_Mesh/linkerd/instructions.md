1. Download the Linkerd CLI
```
curl --proto '=https' --tlsv1.2 -sSfL https://run.linkerd.io/install | sh
```

2. Ensure that your cluster meets the requirements for Linkerd
```
linkerd check --pre
```

3. Install the Linkerd CRDs
```
linkerd install --crds | kubectl apply -f -
```

4. Install Linkerd
```
linkerd install | kubectl apply -f -
```

You can also use Helm to install Linkerd

```
helm repo add linkerd https://helm.linkerd.io/stable

helm install linkerd-crds linkerd/linkerd-crds \
  -n linkerd --create-namespace

helm install linkerd-control-plane \
  -n linkerd \
  --set-file identityTrustAnchorsPEM=ca.crt \
  --set-file identity.issuer.tls.crtPEM=issuer.crt \
  --set-file identity.issuer.tls.keyPEM=issuer.key \
  linkerd/linkerd-control-plane
```