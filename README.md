## helm-charts-home
## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  helm repo add <alias> https://<orgname>.github.io/helm-charts-home

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo <alias>` to see the charts.

To install the <chart-name> chart:

    helm install my-<chart-name> <alias>/<chart-name>

To uninstall the chart:
 
    helm delete my-<chart-name>

## Add , package and publish Chart

To create the Chart :

    helm create helm-chart-sources/helm-chart-test

Lint the chart: 
   
    helm lint helm-chart-sources/*

Create the Helm chart package:

    helm package helm-chart-sources/*

To regenerate the index.yaml:

    helm repo index --url https://burnom.github.io/helm-charts-home/ --merge index.yaml .

To publish to Github pages:

    git add . && git commit -m "Add new comment" && git push origin main
