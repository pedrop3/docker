# Kubernetes README

Este README fornece instruções básicas para o uso do comando `kubectl` no Kubernetes. Certifique-se de ter o `kubectl` e o `minikube` instalados antes de prosseguir.

## 1. Aplicar um arquivo de configuração

Use o seguinte comando para aplicar um arquivo de configuração YAML no Kubernetes:

```bash
kubectl apply -f <filename>
```

Este comando aplica as configurações definidas no arquivo YAML especificado ao cluster Kubernetes.

## 2. Obter informações detalhadas sobre pods

Para visualizar informações detalhadas sobre os pods em execução no cluster, utilize o seguinte comando:

```bash
kubectl get pods -o wide
```

Isso exibirá uma lista de pods ativos, incluindo detalhes adicionais, como nome, status, IP, nós em que estão executando, etc.

## 3. Obter informações sobre serviços

Para listar os serviços em execução no cluster, use o comando:

```bash
kubectl get services
```

Este comando fornece informações sobre os serviços, incluindo nome, tipo, porta e IP externo (se aplicável).

## 4. Obter informações sobre deployments

Para listar os deployments no cluster, utilize o comando:

```bash
kubectl get deployments
```

Este comando exibe informações sobre os deployments, incluindo nome, desejado, atual e disponível número de réplicas.

## 5. Alterar a imagem de um contêiner em um pod

Para atualizar a imagem de um contêiner em um pod, use o seguinte comando:

```bash
kubectl set image <object-type>/<object-name> <container-name>=<new-image-to-use>
```

Substitua `<object-type>` pelo tipo do objeto (por exemplo, `deployment`), `<object-name>` pelo nome específico do objeto que contém o pod, `<container-name>` pelo nome do contêiner que deseja atualizar, e `<new-image-to-use>` pela nova imagem que você deseja usar.

## 6. Obter o IP do Minikube

Se estiver usando o Minikube, você pode obter o endereço IP do cluster com o seguinte comando:

```bash
minikube ip
```

Isso retornará o endereço IP que pode ser usado para acessar serviços hospedados no cluster Minikube.

## 7. Descrever um objeto específico

Para obter detalhes específicos sobre um objeto no Kubernetes, use o seguinte comando de descrição:

```bash
kubectl describe <object-type> <object-name>
```

Substitua `<object-type>` pelo tipo do objeto (por exemplo, `pod`, `service`) e `<object-name>` pelo nome específico do objeto que você deseja descrever.

## 8. Excluir recursos usando um arquivo de configuração

Para excluir recursos previamente criados com um arquivo de configuração YAML, utilize o seguinte comando:

```bash
kubectl delete -f <config-file>
```

Substitua `<config-file>` pelo nome do seu arquivo de configuração YAML. Isso removerá os recursos especificados no arquivo do cluster Kubernetes.

Certifique-se de personalizar os comandos conforme necessário para atender às suas necessidades específicas. Esses comandos fornecem uma introdução básica ao uso do Kubernetes e são úteis para interagir com o seu cluster local.