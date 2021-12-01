# Update helm-chart-superset

```bash
mkdir -p ~/git && cd ~/git
git clone https://github.com/link-webcreations/helm-chart-superset.git
git clone https://github.com/apache/superset.git
cd ~/git/superset/helm/superset
helm repo add superset https://raw.githubusercontent.com/link-webcreations/helm-chart-superset/master
helm repo update
helm dependency update . --skip-refresh
helm package .
helm repo index . --url https://raw.githubusercontent.com/link-webcreations/helm-chart-superset/master
cp index.yaml ~/git/helm-chart-superset
cp superset-*.tgz ~/git/helm-chart-superset
cd ~/git/helm-chart-superset
git add superset-*.tgz
git coa -m "feat(superset): Update version"
git push
helm repo update
```
