Uses: Podman, Minikube, Kubectl, Kustomize, Flux (GitOps)

# Prerequisites

Install Flux cli tool: [FLUX_TUTORIAL.md](FLUX_TUTORIAL.md)

# Github

Run the bootstrap command to create repository `minimal-gitops-flux`:

```shell
flux bootstrap github \
  --owner=tfasanga \
  --repository=minimal-gitops-flux \
  --branch=main \
  --path=./clusters/my-cluster \
  --reconcile \
  --personal
```

The bootstrap will create a new repo [tfasanga/minimal-gitops](https://github.com/tfasanga/minimal-gitops)

Clone the repo:

```shell
git clone https://github.com/tfasanga/minimal-gitops-flux
cd minimal-gitops-flux
```

List all k8s resources in namespace flux-system:

```shell
kubectl get all --namespace flux-system
```
