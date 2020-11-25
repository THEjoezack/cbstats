# CB Stats

Stats aggregation and prediction for Coding Blocks.

```bash
skaffold dev --port-forward
```

Open the following sites in a browser:

- [Grafana](http://localhost:80) (admin/prom-operator)
- [Prometheus](http://localhost:9090)

## TODO

- Get it showing up in Grafana?
- Can skaffold install helm repositories?
- Skaffold didn't republish my change

## Questions

- Does Grafana/Prometheus make sense here, since the data is so slow?

## Sources of Data

- [YouTube](https://support.google.com/youtube/answer/9088722?hl=en)
- Google Spreadsheets
- Twitch
- Facebook
- Twitter
- Libsyn

## Tools

- Kuberentes
- [Prometheus](https://prometheus.io/)
- Grafana
- [Skaffold](https://github.com/GoogleContainerTools/skaffold/releases)
- Google Spreadsheets
- [Prometheus Operator](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack)


## Installing Operators

```helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add stable https://charts.helm.sh/stable
helm repo update
helm install prometheus prometheus-community/kube-prometheus-stack
```

## Benefits of Skaffold

- Builds your images, as needed
