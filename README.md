# Projeto de estudo de kubernetes

### Comandos Kubectl

* _Exibir pods_: 
```
kubectl get pods
```

* _Criar um recurso a partir de um arquivo_:
```
kubectl apply -f .\arquivo.yaml
```

* _Deletar um pod_:
```
kubectl delete pod nome-pod
```

* _Entrar em um pod_:
```
kubectl exec -it nome-pod -- bash
```

* _Após entrar em um pod de aplicação, consegue exibir arquivos do pod_:
```
ls
```

* _Sair do pod_:
```
kubectl exec -it nome-pod -- bash
```

* _Deletar todos os pods_:
```
kubectl delete pods --all
```
## Links

É possivel criar services (ClusterIP, NodePorts), replicas e deployments a partir de arquivos 

* _Criar/ Alterar deployment com versão_:
```
kubectl apply -f .\arquivo-deployment.yaml --record
```

* _Mostrar histórico de versionamento de deployment_:
```
kubectl rollout history deployment nome-deployment
```

* _Renomear versão de deployment_:
```
kubectl annotate deployment nome-deployment kubernetes.io/change-cause="defindo versão"
```

* _Voltar pod para uma versão especifica_:
```
kubectl rollout undo deployment nome-deployment --to-revision=1
```


