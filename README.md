1. Install olm
```
 curl -sL https://github.com/operator-framework/operator-lifecycle-manager/releases/download/0.15.1/install.sh | bash -s 0.15.1
 ```

2. Install Operator
```
kubectl create -f https://operatorhub.io/install/prometheus.yaml
```

3. Check install
```
kubectl get csv -n operators
```

4. Create prometheus instance
```
kubectl create ns monitoring
kubectl apply -n monitoring -f serviceAccount.yaml
kubectl apply -n monitoring -f prometheus-install.yaml
```

5. Create podMonitor for the application
```
kubectl apply -f podMonitor.yaml
```

6. Deploy app 
```
kubectl create ns demo
kubectl apply -n demo -f  app.yaml
```