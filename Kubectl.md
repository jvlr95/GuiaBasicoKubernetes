# Guia Pessoal para estudos - Kubernetes -- kubectl!

## Instalação do kubectl

`kubectl` é a ferramenta de linha de comando do Kubernetes que permite interagir com clusters Kubernetes. Aqui estão as etapas básicas de instalação:

### Linux
## Documentação do Kubectl --> https://kubernetes.io/


```bash
# Baixar o binário do kubectl
sudo curl -Lo /usr/local/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl

# Tornar o binário executável
sudo chmod +x /usr/local/bin/kubectl

# Verificar a instalação
kubectl version --client
```

## Principais Comandos do kubectl

### Contextos e Clusters

- **Listar Contextos:**
  ```bash
  kubectl config get-contexts
  ```

- **Selecionar Contexto:**
  ```bash
  kubectl config use-context <nome-do-contexto>
  ```

- **Listar Clusters:**
  ```bash
  kubectl config get-clusters
  ```

### Pods

- **Listar Pods:**
  ```bash
  kubectl get pods
  ```

- **Detalhes do Pod:**
  ```bash
  kubectl describe pod <nome-do-pod>
  ```

- **Executar Comando Dentro do Pod:**
  ```bash
  kubectl exec -it <nome-do-pod> -- <comando>
  ```

### Deployments

- **Listar Deployments:**
  ```bash
  kubectl get deployments
  ```

- **Atualizar Imagem de Deployment:**
  ```bash
  kubectl set image deployment/<nome-do-deployment> <nome-do-container>=<nova-imagem>
  ```

- **Escalar Deployment:**
  ```bash
  kubectl scale deployment <nome-do-deployment> --replicas=<número-de-replicas>
  ```

### Serviços

- **Listar Serviços:**
  ```bash
  kubectl get services
  ```

- **Criar Serviço a partir de um Manifesto:**
  ```bash
  kubectl apply -f <arquivo-de-manifesto>
  ```

- **Acessar um Serviço:**
  ```bash
  kubectl port-forward service/<nome-do-serviço> <porta-local>:<porta-remota>
  ```
