# Repository for the public FMI Helm charts

This branch (`gh-pages`) is automatically updated using the GitHub
Actions workflow defined in the `main` branch. There is typically
no need to update this branch manually. This branch contains the
resources needed to serve the public Helm repository published in

https://fmidev.github.io/fmi-public-helm-charts/

## Usage

To add this chart repository:

```shell
helm repo add fmi-public-helm-charts https://fmidev.github.io/fmi-public-helm-charts
```

To list the available charts:
```shell
helm search repo fmi-public-helm-charts
```
