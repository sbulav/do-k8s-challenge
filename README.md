# do-k8s-challenge
 Digital Ocean Kubernetes Challenge repo


## Introduction

This repo contains Helm values and Github actions for the installation of the
[kyverno](https://github.com/kyverno/kyverno).

Initial installation of the Kyverno is triggered by the manual pipeline.
Any changes to the Helm values will trigger Helm upgrade.

Policies located in the
[Policies](https://github.com/sbulav/do-k8s-challenge/policies) directory and
will be updated automatically if any policy has changed.

Main branch is write protected and all changet should be done through the
Pull Request. Each PR is linted and validated.

## Prerequisites

- [DOKS cluster](https://docs.digitalocean.com/products/kubernetes/quickstart/) - Digital Ocean Kubernetes Cluster Created
- [Personal access token](https://docs.digitalocean.com/reference/api/create-personal-access-token/)


## Initialization

Steps required to set up GitHub Actions:

1. Set up Github secret with DO personal access token with name `DO_K8S_TOKEN`
2. Set up Github secret with DO k8s cluser name with name `DO_K8S_CLUSTER_NAME`
3. Trigger the manual pipeline `NAME` for the initial installation of `kyverno`
