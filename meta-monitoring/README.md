# meta-monitoring

Step 0. Update k8s-monitoring subchart

```
helm dependency update
```

Step 1. Install Alloy CRD (required for k8s-monitoring v3)

```
kubectl apply -f https://github.com/grafana/alloy-operator/releases/download/alloy-operator-0.3.0/collectors.grafana.com_alloy.yaml
```

Step 2. Install k8s-monitoring

```
helm upgrade metamon . --install --create-namespace --namespace tns-meta-monitoring
```
