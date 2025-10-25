# FluxCD Example with  Kubernetes

This repository contains a basic example of using FluxCD with a Kubernetes cluster.

## Prerequisites

- Kubernetes enabled
- FluxCD CLI installed
- kubectl installed

## Setup Instructions

1. First, install Flux in your cluster:
   ```bash
   flux bootstrap github \
     --owner=$GITHUB_USER \
     --repository=fluxcd-example \
     --branch=main \
     --path=./clusters/local \
     --personal
   ```

2. Verify the installation:
   ```bash
   flux get all
   ```

3. The repository is configured to sync with https://github.com/kerobero/fluxc-example

4. Check the status of your GitRepository:
   ```bash
   flux get sources git
   ```

5. Check the status of your Kustomizations:
   ```bash
   flux get kustomizations

   ```
