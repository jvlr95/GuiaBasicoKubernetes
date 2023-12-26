# Guia Pessoal para estudos da ferramenta MiniKube
O **Minikube** é uma ferramenta que facilita a execução de clusters Kubernetes locais. Ele é ideal para desenvolvimento, testes e aprendizado sobre o Kubernetes em um ambiente isolado. Abaixo estão os passos para instalação e alguns comandos úteis.

## Instalação do Minikube

### Linux

```bash
# Baixar o executável do Minikube
curl -Lo minikube https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

# Tornar o executável do Minikube executável
chmod +x minikube

# Mover o executável para um diretório no seu PATH
sudo mv minikube /usr/local/bin/
```

# Documentação do Minikube --> https://minikube.sigs.k8s.io/docs/start/

## Principais Comandos do Minikube

### Iniciar um Cluster Minikube

```bash
minikube start
```

### Verificar o Status do Cluster

```bash
minikube status
```

### Parar um Cluster Minikube

```bash
minikube stop
```

### Acessar o Dashboard Kubernetes

```bash
minikube dashboard
```

### Listar Perfis Minikube

```bash
minikube profile list
```

### Selecionar um Perfil Minikube

```bash
minikube profile <nome-do-perfil>
```

### Ajustar Configurações de Recursos

```bash
minikube config set memory 4096
minikube config set cpus 2
```

### Excluir um Cluster Minikube

```bash
minikube delete
```
