# 💬 Sistema de Comentários com Docker + Kubernetes

Projeto full stack com Frontend em HTML/CSS/JS, Backend em PHP e banco de dados MySQL, empacotado com Docker e orquestrado com Kubernetes via Minikube.

---

## 🚀 Tecnologias Utilizadas

- ✅ HTML5 + CSS3 + JavaScript
- ✅ PHP 7.4 (Apache)
- ✅ MySQL 5.7
- ✅ Docker e Docker Compose
- ✅ Kubernetes (Minikube)
- ✅ NGINX

---

## 📦 Estrutura do Projeto

```
meuapp-k8s/
├── backend/ # Código PHP + Dockerfile
├── frontend/ # HTML, CSS, JS + Dockerfile
├── database/ # Script SQL (init.sql)
├── k8s/ # Arquivos YAML do Kubernetes
├── docker-compose.yml
└── deploy.sh # Script de automação para Minikube
```

---

## 🧪 Como rodar localmente com Docker Compose

> ⚠️ Pré-requisitos: Docker e Docker Compose instalados

```bash
# Clone o repositório
git clone https://github.com/seuusuario/meuapp-k8s.git
cd meuapp-k8s
```
# Rode os containers
```
sudo docker-compose up --build
```
### 📍 Acesse no navegador:

- 🌐 Frontend: http://localhost:8080

-  🧠 Backend: http://localhost:8000

### ☸️ Como rodar no Kubernetes com Minikube <br> 

-  ⚠️ Pré-requisitos: Docker, Minikube e kubectl instalados
<br>
```
# Inicie o Minikube
minikube start

# Execute o script automático
./deploy.sh
```
📍 O script abrirá automaticamente a aplicação no navegador via porta NodePort (30001 por padrão).

### 🧠 Banco de Dados
O script ```init.sql``` é executado automaticamente ao subir o container MySQL:

```
CREATE DATABASE meubanco;

CREATE TABLE mensagens (
  id INT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100),
  comentario TEXT
);

## 📄 Licença
Este projeto está sob a licença MIT.
Veja o arquivo LICENSE para mais detalhes.

Desenvolvedor em transição de carreira, apaixonado por tecnologia, qualidade de código e boas práticas. Sempre aprendendo, sempre evoluindo. 🚀

## 👤 Desenvolvido por
Gustavo N. Bezerra - [LinkedIn](https://www.linkedin.com/in/gustavo-nunnes) | [GitHub](https://github.com/GNunnes) |<i>gustavonunnes@hotmail.com</i> 
