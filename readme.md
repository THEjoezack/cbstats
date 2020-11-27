# CB Stats

Stats aggregation and prediction for Coding Blocks.

```bash
skaffold dev --port-forward
```

Open the following sites in a browser:

- [Grafana](http://localhost:80) (admin/prom-operator)
- [Prometheus](http://localhost:9090)


## TODO

- Get basic info about the data showing up in a notebook
- Can skaffold install helm repositories?

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
helm install prometheus prometheus-community/kube-prometheus-stack
helm repo add elastic https://helm.elastic.co
helm repo update
```

## Benefits of Skaffold

- Builds your images, as needed




## Steps:

https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-deploy-elasticsearch.html

- Install Docker, K8s, Skaffold

- Add the repo
```helm
helm repo add elastic https://helm.elastic.co
helm repo update
```
(alternatively: https://www.elastic.co/guide/en/cloud-on-k8s/current/k8s-deploy-eck.html)

- Add the release to skaffold.yaml:

```yaml
apiVersion: elasticsearch.k8s.elastic.co/v1
kind: Elasticsearch
metadata:
  name: quickstart
spec:
  version: 7.10.0
  nodeSets:
  - name: default
    count: 2
    config:
      node.store.allow_mmap: false
```

- Get the password:

kubectl get secret quickstart-es-elastic-user




- Verify the creds

```elastic
curl.exe -u "elastic:$PASSWORD" -k "https://localhost:9200"
```

TODO Kibana