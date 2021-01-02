
# Helm Charts

This repo contains various helm charts to use with my CI/CD test repos.

- samplepythonapp : sample python app repositry located at : https://github.com/okutkan/PythonSampleApp
- simplejavaapp:  sample java app repository located at:  https://github.com/okutkan/JavaMavenSampleApp
- mysqlsample: sample mysql server chart fort sample pythno app

*Disclaimer:* This is a work in progress. These charts may or may not work for your project.

# How to use it as a helm repo

You might know github has a raw view. So simply use the following:

```bash
$ helm repo add sample 'https://raw.githubusercontent.com/okutkan/helm-charts/master/'
$ helm repo update
$ helm search samplepythonapp
NAME             VERSION DESCRIPTION
sample/samplepythonapp	0.1.2  	A Helm chart for samplepythonapp in Kubernetes
```

# Adding a new version or chart to this repo

```bash
helm package $YOUR_CHART_PATH/ # builds the tgz file and copy it here
helm repo index . # create or update the index.yaml for repo
git add . # you know how this works
git commit -m 'New chart version'
```

# How to use it as a helm repo

You might know github has a raw view. So simply use the following:

```bash
$ helm repo add sample 'https://raw.githubusercontent.com/okutkan/helm-charts/master/'
$ helm repo update
$ helm search samplepythonapp
NAME            	VERSION	DESCRIPTION
sample/samplepythonapp	0.1.2  	A Helm chart for samplepythonapp in Kubernetes
```

