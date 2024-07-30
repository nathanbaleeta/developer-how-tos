#### List Helm repositories added to machine
```
helm repo list
```
#### Add virtual repository
```
helm repo add <VIRTUAL_REPO>
```
#### Update cache of local repos with latest artifacts
```
helm repo update
```
#### Search virtual repo for specific chart
```
helm search repo <VIRTUAL_REPO>
helm search repo dask (select dask/daskhub version==2024.1.0)
helm search repo dagster
```
#### Extract config values.yaml file from helpm virtual repo
```
helm show values dagster/dagster > config.yaml
helm show values dask/daskhub > daskhub.yaml -n daskhub-staging
```

#### Install specific chart
```
helm install <RELEASE_NAME> <VIRTUAL_REPO>/<CHART_NAME> -n <NAMESPACE>
```
```
helm install project-daskhub dask/daskhub --version 2024.1.0 -n daskhub-dev
```
```
helm install project-dagster dagster/dagster \
    --namespace dagster-dev \
    --create-namespace
```
