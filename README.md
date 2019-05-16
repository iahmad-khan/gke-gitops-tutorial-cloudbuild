# GitOps-style Continuous Delivery For Kubernetes With Gitlab

GitOps is a Continuous Delivery approach [first described by Weaveworks](https://www.weave.works/blog/gitops-operations-by-pull-request) that is
popular in the Kubernetes community. A key part of GitOps is the idea of
"environments-as-code": describing your deployments declaratively by files (for
example, Kubernetes manifests) stored in a Git repository.

In this tutorial, you create a CI/CD pipeline that automatically builds a
container image from commited code, stores the image in Gitlab Registry, updates a Kubernetes manifest in a Git repository and triggers a
deployment to Kubernetes using that manifest.

In the end, you have a system where:
* You have a view of successful and failed deployments.
* You can rollback to any previous deployment by re-executing the corresponding
  job in Gitlab CI/CD pipeline.
