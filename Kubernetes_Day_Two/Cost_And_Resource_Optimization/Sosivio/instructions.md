**ensure that you have at least a three node cluster**

1. Go to the following page to download Sosivio
https://www.sosiv.io/app/download

2. Untar
```
tar -xvf tar -xvf installer-release-1.5.3-mac.tar.gz
```

3. Run the installer
```
./installer-release-1.5.3-mac
```

4. Expose the k8s Service for Sosivio so you can log in
```
kubectl port-forward -n sosivio svc/dashboard 8088:8088
```

Username: admin
Password: It'll be displayed on the terminal