# Public FMI Helm charts (fmi-public-helm-charts)

This repository contains public Helm charts from FMI.
The Helm chart repository is published to:

https://fmidev.github.io/fmi-public-helm-charts

## Usage

[Helm](https://helm.sh) must be installed to use the charts. Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

```shell
helm repo add fmi-public-helm-charts https://fmidev.github.io/fmi-public-helm-charts
```

To list the available charts in this repository, use:
```shell
helm search repo fmi-public-helm-charts
```

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages. You can then run `helm search repo fmi-public-helm-charts`
to see the charts.

To install, for example, the chart `fmi-routes`:

```shell
helm install my-chart-name fmi-public-helm-charts/fmi-routes
```

To uninstall the chart:

```shell
helm delete my-chart-name
```

## Adding custom charts

The sources of any charts must be placed in the `main` branch under the
`/charts` directory at the top-level of the directory tree.

There is another branch named `gh-pages` which is used to publish the charts.
The changes to that branch will be automatically generated using the GitHub
Actions workflow in the `main` branch.

## Updating

Every push to `main` will check each chart in this repository, and whenever
there is a new chart version, a corresponding GitHub release named for the
chart version is created, the Helm chart artifacts are added to the release,
and an index.yaml file with metadata about those releases is either created
or updated, and then hosted using the GitHub pages.

## Further reading

* [Helm Charts](https://helm.sh/docs/topics/charts/)
* [GitHub Actions workflow for releasing the charts](https://helm.sh/docs/howto/chart_releaser_action/#github-actions-workflow)
