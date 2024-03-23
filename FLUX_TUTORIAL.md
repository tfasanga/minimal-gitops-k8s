Uses: Podman, Minikube, Kubectl, Kustomize, Flux (GitOps)

https://fluxcd.io/flux/get-started/

Install Flux CLI:

```shell
brew install fluxcd/tap/flux
```
Assuming your token is saved in file `~/.ssh/github`:

```
export GITHUB_TOKEN=<your-token>
export GITHUB_USER=<your-username>
```

```shell
flux check --pre
```

Run the bootstrap command.

The bootstrap will create a new repo in github.com.

List all k8s resources in namespace flux-system:

```shell
kubectl get all --namespace flux-system
```

Clone the repo:

```
git clone https://github.com/$GITHUB_USER/<REPO>
cd <REPO>
```

