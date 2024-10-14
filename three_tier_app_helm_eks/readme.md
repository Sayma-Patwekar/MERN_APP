helm:

1. Create helm charts
```
$ helm create <chart_name> 
```

2. Install helm charts
```
$ helm install <helm-chart-name> ./<helm-chart-name>
```
# note: stay in helm dir, i.e; one dir out of your generated helm chart dir

3. Upgrade helm charts
```
$ helm upgrade <helm-chart-name> ./<helm-chart-name>
```

4. Uninstall helm charts
```
$ helm uninstall <helm-chart-name>
```
# note: delete in sequence
    frintend -> backend -> database

5. see all deployed applications
```
$ helm list
```

##########################################################

1. Install ingress-controller(load balancer):(it contains ingress class)
cmd : kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.11.1/deploy/static/provider/aws/deploy.yaml

2. for minikube:(it does not contain ingress class)
cmd: 
minikube addons enable ingress
kubectl get pods -n ingress-nginx

minikube ip

3. open in bin/bash or terminal mode:
(do this if you're not seeing database 'school' created using helm)
kubectl exec -it <pod>> -n mern -- bin/bash
rm -rf /var/lib/mysql/*
