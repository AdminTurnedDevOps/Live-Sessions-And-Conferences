```
docker run -d --restart=unless-stopped \
  -p 80:80 -p 443:443 \
  --privileged \
  rancher/rancher:latest
```

```
docker logs  your_rancher_container_id  2>&1 | grep "Bootstrap Password:"
```