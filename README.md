# desafio-kubernetes
Desafio Kubernetes: Seu deploy em containers da maneira certa

# Guia de Configuração da Aplicação

Este guia descreve o processo de configuração de uma aplicação e a execução dela localmente no localhost na porta 8080. O processo envolve a criação de um Dockerfile e um arquivo de deployment YAML, seguindo as instruções do instrutor.

## Passos para Configurar a Aplicação

Siga os passos abaixo para configurar e executar a aplicação:

### 1. Crie o Dockerfile

Um Dockerfile é um arquivo que descreve a configuração de um contêiner Docker. Você pode criar um Dockerfile para a sua aplicação com as seguintes instruções:

```Dockerfile
# Use uma imagem base apropriada, por exemplo:
# FROM node:versao

# Defina o diretório de trabalho no contêiner
# WORKDIR /app

# Copie os arquivos de sua aplicação para o contêiner
# COPY . .

# Instale as dependências, por exemplo:
# RUN npm install
# EXPOSE 8080

# Especifique o comando para iniciar a aplicação
# CMD [ "node", "server.js"]
```
### 2. Crie o Arquivo de Deployment YAML
Recursos YAML para implantar um banco de dados PostgreSQL e um aplicativo chamado "kubenews" no Kubernetes:
Para o Banco de Dados PostgreSQL:

Um Deployment para garantir que os Pods do PostgreSQL estejam em execução.
Um Service para direcionar o tráfego para os Pods do PostgreSQL na porta 5432.
Para o Aplicativo "kubenews":

Um Deployment com 10 réplicas para o aplicativo "kubenews".
Um Service para direcionar o tráfego para os Pods do aplicativo "kubenews" na porta 80, usando o NodePort 30000.
Ambos os Deployments e Services são definidos com rótulos para identificação e seleção de recursos no Kubernetes.

### 3. Execute a Aplicação Localmente
Depois de criar o Dockerfile e o arquivo de deployment YAML, você pode construir a imagem Docker e implantá-la localmente. Certifique-se de que o serviço da aplicação esteja ouvindo na porta 8080 para que você possa acessá-la em http://localhost:8080.
