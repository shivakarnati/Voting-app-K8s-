**Kubernetes (K8s) based application**

This is a sample K8s project implemented, and originally taken from the source "https://www.youtube.com/watch?v=XuSQU5Grv1g&t=3792s".


## To run the application

1. `docker run -d --name=redis redis`
2. `docker run -d --name=db postgres:9.4`
3. `docker run -d --name=vote -p 5000:80 --link redis:redis voting-app`
4. `docker run -d --name=result -p 5001:80 --link db:db result-app`
5. `docker run -d --name=worker --link db:db --link redis:redis worker`
