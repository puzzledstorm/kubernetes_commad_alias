# kubernetes_commad_alias
k8s的一些命令简写

```
alias k=kubectl
alias kl="kubectl logs -f -n default"
alias kp="kubectl get po -n default"
alias ks="kubectl get svc -n default"
alias kc="kubectl get cm -n default"
alias kd="kubectl get deploy -n default"
alias ked="kubectl edit deploy -n default"
alias kes="kubectl edit svc -n default"
alias kec="kubectl edit cm -n default"
alias kdp="kubectl delete po -n default"
alias kds="kubectl delete svc -n default"
alias hu="helm uninstall -n default"
alias hl="helm list -n default"
alias hi="helm install -n default"
alias ke='_f(){ 
        kubectl -n default exec -it $1 -- /bin/bash; 
        if [ $? -ne 0 ] ;then
                kubectl -n default exec -it $1 -- /bin/sh;
        else
                echo "Error";
        fi
        }; _f'
alias de='_f(){ 
        docker exec -it $1 /bin/bash; 
        }; _f'
alias kb="kubectl describe po -n default"
```

## 添加到.bashrc里面
```
if [ -f ~/.alias_k8s ]; then
    . ~/.alias_k8s
fi
```
