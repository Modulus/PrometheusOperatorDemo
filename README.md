1. Install olm
```
 curl -sL https://github.com/operator-framework/operator-lifecycle-manager/releases/download/0.15.1/install.sh | bash -s 0.15.1
 ```

 2. Install Operator
 kubectl create -f https://operatorhub.io/install/prometheus.yaml

 3. Check install
 kubectl get csv -n operators