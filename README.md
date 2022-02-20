# Kubernetes Crash Course for Absolute Beginners

- Video: https://www.youtube.com/watch?v=s_o8dwzRlu4
- Repo: https://gitlab.com/nanuchi/k8s-in-1-hour

## Getting Started

- Install [Docker](https://www.docker.com/get-started)
- Install [minikube](https://minikube.sigs.k8s.io/docs/start/)
- Start minikube

```sh
minikube start --driver docker
```

- Apply the 4 YAML files to the minikube instance:

```sh
kubectl apply -f mongo-config.yaml
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f webapp.yaml
```

Run the webapp from command line:

```sh
minikube service webapp-service
```

Note that the terminal needs to remain open for the webapp to run.
Control-C will stop the web app.
