1. Frontend (React) Application
The frontend will be a basic React application that displays data fetched from the backend.

1. to generate 'package-lock.json' run 'npm install' inside the directory.
Docker cmd :  docker build -f ./Dockerfile-database -t saymapatwekar/mysql-image:v1 .

2. switch namespace:
kubectl config set-context --current --namespace=<namespace>

3. restart deployment
kubectl rollout restart deployment backend -n mern

4. login to mysql pod
kubectl exec -it <mysql-pod-name> -n mern -- mysql -u root -p
kubectl exec -it database-9979c94f-kwhkp -- printenv

5. logs:
kubectl logs -l role=database