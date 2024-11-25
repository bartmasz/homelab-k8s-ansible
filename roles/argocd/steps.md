# Update admin password

```bash
brew install argocd

argocd admin initial-password -n argocd
argocd login << replace with your argocd url >>
argocd account update-password

kubectl -n argocd delete secret argocd-initial-admin-secret
```
