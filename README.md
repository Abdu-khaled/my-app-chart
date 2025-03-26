# My App Helm Chart

This repository contains a Helm chart for deploying an application on Kubernetes with LoadBalancer service, auto-scaling, and optional ingress.

## Features
- Deploys an application as a Kubernetes Deployment
- Supports configurable replicas and resource limits
- Exposes the application via a LoadBalancer service
- Optional ingress support
- Auto-scaling using HorizontalPodAutoscaler

## Installation

Ensure Helm is installed:

```bash
curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash
```

Clone this repository:

```bash
git clone https://github.com/your-username/my-app-helm-chart.git
cd my-app-helm-chart
```

Deploy the chart:

```bash
helm install my-app . --values values.yaml
```

## Verifying the Deployment

```bash
kubectl get deployments
kubectl get pods
kubectl get svc
```

## Accessing the Application

Retrieve the external IP:

```bash
kubectl get svc my-app
```

Copy the `EXTERNAL-IP` and open it in your browser:

```
http://<EXTERNAL-IP>
```

For Minikube users:

```bash
minikube service my-app
```

## Uninstalling the Chart

```bash
helm uninstall my-app
```

## Contributing
Feel free to fork the repository and submit pull requests for improvements.

## License
This project is licensed under the MIT License. See `LICENSE` for details.
