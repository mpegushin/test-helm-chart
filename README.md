# Test Helm Chart

This repository was created for a test assignment.
This repository contains the Helm chart for deploying a **test service**.  

## What is Helm?

[Helm](https://helm.sh/) is a package manager for Kubernetes that helps you define, install, and manage Kubernetes applications.  
With Helm, you can bundle Kubernetes manifests into reusable packages called **charts**, making deployments consistent and easy to manage.

## Repository Structure

- **/templates/** – contains the helm chart templates for the test service
- **values.yaml** – default configuration values for the chart
- **Chart.yaml** – metadata about the chart

## Chart Distribution

The chart is published as a package in the [GitHub Container Registry (GHCR)](https://ghcr.io).  
This allows it to be reused during deployments without having to store chart sources inside the service repository.  

Example of pulling the chart from `ghcr.io`:

```bash
helm pull oci://ghcr.io/<your-org>/<chart-name> --version <version>
```

## How to Use

1. Make sure you have Helm installed. See the [installation guide](https://helm.sh/docs/intro/install/).
2. Deploy the chart into your Kubernetes cluster:
   ```bash
   helm install test-service ./charts/test-service
   ```