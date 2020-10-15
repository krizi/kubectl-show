
```
> k show pod --view overview,node
NAMESPACE   NAME                                            STATUS    RESTARTS   START                  NODE       HOSTIP
argocd      argocd-application-controller-786fcbb58-xlfl8   Running   3          2020-05-28T14:42:48Z   minikube   192.168.64.5
argocd      argocd-dex-server-7b5bd689fb-pnddq              Running   2          2020-05-28T15:54:15Z   minikube   192.168.64.5
argocd      argocd-redis-8c568b5db-c2wjn                    Running   2          2020-05-28T14:42:48Z   minikube   192.168.64.5
argocd      argocd-repo-server-59fddff8f8-gl5rn             Running   2          2020-05-28T14:42:48Z   minikube   192.168.64.5
argocd      argocd-server-d896cbbcb-xr2ht                   Running   2          2020-05-28T14:42:48Z   minikube   192.168.64.5
```

```
> k show pod --view name 
NAMESPACE   NAME
argocd      argocd-application-controller-786fcbb58-xlfl8
argocd      argocd-dex-server-7b5bd689fb-pnddq
argocd      argocd-redis-8c568b5db-c2wjn
argocd      argocd-repo-server-59fddff8f8-gl5rn
argocd      argocd-server-d896cbbcb-xr2ht
```
```
> k show pod --view name,mount
NAMESPACE   NAME                                            MOUNT                                                 MOUNTPATH
argocd      argocd-application-controller-786fcbb58-xlfl8   argocd-application-controller-token-p2vqc             /var/run/secrets/kubernetes.io/serviceaccount
argocd      argocd-dex-server-7b5bd689fb-pnddq              static-files,argocd-dex-server-token-9bgb5            /shared,/var/run/secrets/kubernetes.io/serviceaccount
argocd      argocd-redis-8c568b5db-c2wjn                    default-token-dxm5t                                   /var/run/secrets/kubernetes.io/serviceaccount
argocd      argocd-repo-server-59fddff8f8-gl5rn             ssh-known-hosts,tls-certs                             /app/config/ssh,/app/config/tls
argocd      argocd-server-d896cbbcb-xr2ht                   ssh-known-hosts,tls-certs,argocd-server-token-bktf4   /app/config/ssh,/app/config/tls,/var/run/secrets/kubernetes.io/serviceaccount
```
# Restrictions

