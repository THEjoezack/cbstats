# CB Stats

Stats aggregation and prediction for Coding Blocks.

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami

skaffold dev --port-forward
```

Open the following sites in a browser:

- [Grafana](http://localhost:80) (admin/prom-operator)
- [Prometheus](http://localhost:9090)

## TODO

- Liveness/Readiness
- Can skaffold install helm repositories?
- Swap over to minikube

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

