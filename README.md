# argo-cd-ready-applications
ready to use argo-cd application with build-in best-practices to get full applications running in seconds (cert-manager, minecraft-server, ...)

## Requierments
* Kubernetes Cluster e.g. k3s
* [Argo-CD](https://github.com/argoproj/argo-cd/blob/master/manifests/install.yaml)
## Quick-Start
1. Connect to your kubernetes-cluster (Get Kubeconfig, etc.)
2. Clone this repo `git clone https://github.com/3deep5me/argo-cd-ready-applications.git` and change directory
3. Apply the argo-cd appproject `kubectl apply -f applications/project-argo-cd-ready-applications.yaml`
4. Install an app you want, for example an minecraft server `kubectl apply -f applications/app-minecraft.yaml`
5. Check the Status of the app with `kubectl get app -n argocd`

After a while it shold look like this:
```
$ kubectl get app -n argocd
NAME               SYNC STATUS   HEALTH STATUS
minecraft-server   Synced        Healthy
```
if not feel free to open an [issue](https://github.com/3deep5me/argo-cd-ready-applications/issues)
