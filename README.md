# demo-gitops

Desired state for the training demo app. No application code lives here, only manifests.

- `app/`: what Argo CD syncs into the `demo` namespace
- `argocd/application.yaml`: the Argo CD Application (applied once by hand)

The image tag in `app/deployment.yaml` is updated by the CI pipeline in
[haiderali30/demo](https://github.com/haiderali30/demo). Every deploy is one commit here;
to roll back, `git revert` that commit.
