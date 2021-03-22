# Update helm-chart-superset

```bash
git clone https://github.com/apache/superset.git
cd superset/helm/superset
helm repo add superset https://raw.githubusercontent.com/link-webcreations/helm-chart-superset/master
helm repo update
helm dependency update . --skip-refresh
helm repo index . --url https://raw.githubusercontent.com/link-webcreations/helm-chart-superset/master
```
