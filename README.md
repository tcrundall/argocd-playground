# argocd-playground

A playground for me to try out argocd

## Helpful commands

Create an "app"
```
argocd app create my-app --repo https://github.com/tcrundall/argocd-playground.git --path my-app --dest-server https://kubernetes.default.svc --dest-namespace default

# portforward
kubectl port-forward svc/argocd-server -n argocd 8080:443 --address 0.0.0.0
```

```bash
argocd app sync my-app  # sync my app
```

Latest task: commit configuration to repo
