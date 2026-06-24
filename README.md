# 📦 TechStock - Sistema de Controle de Estoque

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![Node.js](https://img.shields.io/badge/Node.js-20.x-green)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16.x-blue)
![Docker](https://img.shields.io/badge/Docker-✓-2496ED)
![Grafana](https://img.shields.io/badge/Grafana-✓-F46800)
![Prometheus](https://img.shields.io/badge/Prometheus-✓-E6522C)

**Sistema completo de controle de estoque com monitoramento em tempo real, totalmente containerizado com Docker.**

---

## 📋 Índice

- [📦 TechStock - Sistema de Controle de Estoque](#-techstock---sistema-de-controle-de-estoque)
  - [📋 Índice](#-índice)
  - [Demonstração Rápida](#demonstração-rápida)
  - [Acesse os serviços](#acesse-os-serviços)
  - [✨ Funcionalidades](#-funcionalidades)
    - [📊 Dashboard Principal](#-dashboard-principal)
    - [📦 Gestão de Produtos](#-gestão-de-produtos)
    - [🔄 Movimentações](#-movimentações)
    - [🔔 Alertas](#-alertas)
    - [📈 Monitoramento (Grafana + Prometheus)](#-monitoramento-grafana--prometheus)
  - [🛠️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
    - [Backend](#backend)
    - [Frontend](#frontend)
    - [DevOps](#devops)
  - [📂 Estrutura do Projeto](#-estrutura-do-projeto)
  - [🚀 Guia de Instalação](#-guia-de-instalação)
    - [Pré-requisitos](#pré-requisitos)
    - [Passo a Passo](#passo-a-passo)
      - [1. Clone o repositório](#1-clone-o-repositório)
      - [2. Configure as variáveis de ambiente](#2-configure-as-variáveis-de-ambiente)
      - [3. Inicie os containers](#3-inicie-os-containers)
      - [4. Aguarde a inicialização](#4-aguarde-a-inicialização)
      - [5. Acesse o sistema](#5-acesse-o-sistema)
  - [🌐 Portas dos Serviços](#-portas-dos-serviços)
    - [📊 Dashboards](#-dashboards)
      - [1. TechStock API - Visão Geral](#1-techstock-api---visão-geral)
      - [2. DevOps - Containers](#2-devops---containers)
      - [3. Infraestrutura EC2](#3-infraestrutura-ec2)
      - [4. Observabilidade](#4-observabilidade)
      - [5. RDS - PostgreSQL](#5-rds---postgresql)
    - [🔧 Desenvolvimento](#-desenvolvimento)
    - [Use Live Server no Visual Studio Code](#use-live-server-no-vs-code)
      - [Ou sirva com Python](#ou-sirva-com-python)
    - [📚 API Endpoints](#-api-endpoints)
      - [📦 Produtos](#-produtos)
      - [🔄 Movimentações (API)](#-movimentações-api)
      - [🏷️ Categorias](#️-categorias)
      - [📊 Estatísticas](#-estatísticas)
    - [🔐 Segurança](#-segurança)
    - [📝 Variáveis de Ambiente](#-variáveis-de-ambiente)
    - [🐳 Comandos Docker](#-comandos-docker)
    - [🤝 Contribuição](#-contribuição)
      - [1. Fork o projeto](#1-fork-o-projeto)
      - [2. Crie sua branch](#2-crie-sua-branch)
      - [3. Commit suas alterações](#3-commit-suas-alterações)
      - [4. Push para a branch](#4-push-para-a-branch)
      - [5. Abra um Pull Request](#5-abra-um-pull-request)
    - [📄 Licença](#-licença)
    - [👥 Autor](#-autor)
  - [🙏 Agradecimentos](#-agradecimentos)
  - [Adicionar ao Git](#adicionar-ao-git)

---

## Demonstração Rápida

```bash
# Clone o repositório
git clone https://github.com/CrisisUp/techstock.git
cd techstock

# Inicie o sistema
docker-compose up -d
```

## Acesse os serviços

| Serviço | URL | Credenciais |
| ------- | --- | ----------- |
| API | [http://localhost:3001](http://localhost:3001) | - |
| Grafana | [http://localhost:3031](http://localhost:3031) | admin / admin |
| Prometheus | [http://localhost:9091](http://localhost:9091) | - |
| Node Exporter | [http://localhost:9101](http://localhost:9101) | - |

## ✨ Funcionalidades

### 📊 Dashboard Principal

- ✅ Métricas em tempo real: Total de produtos, alertas, valor em estoque e movimentações

- ✅ Itens críticos: Visualize produtos com estoque baixo

- ✅ Atualização automática: Dados sempre atualizados

### 📦 Gestão de Produtos

- ✅ CRUD completo: Crie, edite, visualize e inative produtos

- ✅ Busca avançada: Por nome ou código

- ✅ Filtro por categoria: Organize seu estoque

- ✅ Controle de estoque: Quantidade, preço de custo e localização

### 🔄 Movimentações

- ✅ Entrada e saída: Registre movimentações de estoque

- ✅ Histórico completo: Visualize todas as movimentações

- ✅ Filtros: Por tipo e por produto

- ✅ Auditoria: Rastreie quem realizou cada movimentação

### 🔔 Alertas

- ✅ Estoque baixo: Visualize produtos abaixo do mínimo

- ✅ Ações rápidas: Reponha estoque com um clique

### 📈 Monitoramento (Grafana + Prometheus)

- ✅ Métricas HTTP: Requisições por segundo, erros 5xx

- ✅ Performance do Node.js: Heap, Event Loop Lag, Garbage Collection

- ✅ Infraestrutura: CPU, RAM, Disco das instâncias

- ✅ Banco de dados: Conexões ativas, taxa de sucesso, throughput

## 🛠️ Tecnologias Utilizadas

### Backend

| Tecnologia | Descrição |
| ---------- | --------- |
| Node.js | Runtime JavaScript |
| Express | Framework web |
| PostgreSQL | Banco de dados relacional |
| Joi | Validação de dados |
| Prometheus Client | Métricas para monitoramento |

### Frontend

| Tecnologia | Descrição |
| ---------- | --------- |
| HTML5 | Estrutura |
| CSS3 | Estilização com variáveis CSS |
| JavaScript ES6+ | Interatividade |
| ARIA | Acessibilidade |

### DevOps

| Tecnologia | Descrição |
| ---------- | --------- |
| Docker | Containerização |
| Docker Compose | Orquestração de serviços |
| Grafana | Dashboards |
| Prometheus | Coleta de métricas |
| Node Exporter | Métricas do sistema |

## 📂 Estrutura do Projeto

```text
techstock/
├── backend/
│   ├── server.js           # API principal
│   ├── package.json        # Dependências
│   ├── schema.sql          # Schema do banco
│   └── .env.example        # Exemplo de variáveis
├── frontend/
│   ├── index.html          # Página principal
│   ├── app.js              # Lógica frontend
│   ├── config.js           # Configurações
│   └── style.css           # Estilos
├── docker/
│   ├── entrypoint.sh       # Script de inicialização
│   └── supervisord.conf    # Gerenciador de processos
├── prometheus/
│   └── prometheus.yml      # Configuração do Prometheus
├── grafana/
│   └── grafana.ini         # Configuração do Grafana
├── dashboards/             # Dashboards do Grafana
│   ├── dashboard_api.json
│   ├── dashboard_devops.json
│   ├── dashboard_infra.json
│   └── dashboard_rds.json
├── Dockerfile              # Imagem do container
├── docker-compose.yml      # Orquestração dos serviços
├── .gitignore              # Arquivos ignorados
└── README.md               # Documentação
```

## 🚀 Guia de Instalação

### Pré-requisitos

- Docker
- Docker Compose
- Git

### Passo a Passo

#### 1. Clone o repositório

  ```bash
  git clone https://github.com/CrisisUp/techstock2.git
  cd techstock2
  ```

#### 2. Configure as variáveis de ambiente

  ```bash
  cp backend/.env.example backend/.env
  # Edite o arquivo se necessário
  nano backend/.env
  ```

#### 3. Inicie os containers

  ```bash
  docker-compose up -d
  ```

#### 4. Aguarde a inicialização

Os logs mostrarão quando todos os serviços estiverem prontos:

  ```text
  ✅ TechStock Stack iniciada com sucesso!

  📋 Serviços disponíveis:
    📦 TechStock API:    [http://localhost:3001](http://localhost:3001)
    📊 Prometheus:       [http://localhost:9091](http://localhost:9091)
    📈 Grafana:          [http://localhost:3031](http://localhost:3031)
  ```

#### 5. Acesse o sistema

API: [http://localhost:3001](http://localhost:3001)

Frontend: Abra frontend/index.html ou sirva com Live Server

## 🌐 Portas dos Serviços

| Serviço | Porta | Descrição |
| ------- | ----- | --------- |
| TechStock API | 3001 | API do sistema |
| PostgreSQL | 5432 | Banco de dados |
| Prometheus | 9091 | Coleta de métricas |
| Grafana | 3031 | Dashboards |
| Node Exporter | 9101 | Métricas do sistema |

### 📊 Dashboards

#### 1. TechStock API - Visão Geral

Métricas da aplicação:

- Requisições por segundo
- Taxa de erros 5xx
- Heap Node.js usado
- Event Loop Lag p99
- Rotas mais acessadas

#### 2. DevOps - Containers

Saúde dos containers:

- Status da API e exportadores
- Uptime e restarts
- Métricas de recursos

#### 3. Infraestrutura EC2

Métricas do sistema:

CPU por instância

RAM disponível

Disco usado

Tráfego de rede

#### 4. Observabilidade

Saúde do Prometheus:

Séries temporais ativas

Taxa de ingestão

Targets UP

Tamanho TSDB

#### 5. RDS - PostgreSQL

Métricas do banco:

Conexões ativas

Throughput total

Erros de banco

### 🔧 Desenvolvimento

Backend (modo local)

  ```bash
  cd backend
  npm install
  npm run dev
  ```

Frontend (modo local)

  ```bash
  cd frontend
  ```

### Use Live Server no Visual Studio Code

#### Ou sirva com Python

python -m http.server 5500
Build da imagem Docker

  ```bash
  docker build -t techstock:latest .
  ```

### 📚 API Endpoints

#### 📦 Produtos

| Método | Endpoint | Descrição |
| ------ | -------- | --------- |
| GET | `/api/produtos` | Lista todos os produtos |
| GET | `/api/produtos?alerta=1` | Lista produtos com estoque baixo |
| GET | `/api/produtos?busca=nome` | Busca produtos por nome ou código |
| POST | `/api/produtos` | Cria um novo produto |
| PUT | `/api/produtos/:id` | Atualiza um produto existente |
| DELETE | `/api/produtos/:id` | Inativa (soft delete) um produto |

#### 🔄 Movimentações (API)

| Método | Endpoint | Descrição |
| ------ | -------- | --------- |
| GET | `/api/movimentos/:produto_id` | Lista histórico de movimentações de um produto |
| POST | `/api/movimentos` | Registra uma nova movimentação (entrada/saída) |

#### 🏷️ Categorias

| Método | Endpoint | Descrição |
| ------ | -------- | --------- |
| GET | `/api/categorias` | Lista todas as categorias |
| POST | `/api/categorias` | Cria uma nova categoria |

#### 📊 Estatísticas

| Método | Endpoint | Descrição |
| ------ | -------- | --------- |
| GET | `/api/stats` | Retorna métricas do sistema |
| GET | `/api/health` | Verifica a saúde da API (health check) |

### 🔐 Segurança

Autenticação
API Key: Configurável via .env

Grafana: Admin padrão (admin/admin)

Banco de Dados
SSL: Suportado para RDS

Pool: Conexões gerenciadas

Validação: Dados validados com Joi

### 📝 Variáveis de Ambiente

| Variável | Padrão | Descrição |
| -------- | ------ | --------- |
| `PORT` | `3000` | 🚪 Porta da API |
| `DB_HOST` | `localhost` | 🗄️ Host do PostgreSQL |
| `DB_PORT` | `5432` | 🔌 Porta do PostgreSQL |
| `DB_NAME` | `techstock` | 📦 Nome do banco de dados |
| `DB_USER` | `postgres` | 👤 Usuário do banco de dados |
| `DB_PASSWORD` | `postgres` | 🔒 Senha do banco de dados |
| `CORS_ORIGIN` | `*` | 🌐 Origens permitidas (CORS) |
| `API_KEY` | `""` | 🔑 Chave de autenticação da API |

### 🐳 Comandos Docker

```bash
# Ver todos os containers rodando
docker ps

# Ver logs do TechStock
docker logs -f techstock

# Ver logs de todos os serviços
docker-compose logs -f

# Parar todos os serviços
docker-compose down

# Subir novamente
docker-compose up -d

# Reiniciar um serviço específico
docker-compose restart techstock

# Acessar o container
docker exec -it techstock /bin/bash
```

### 🤝 Contribuição

#### 1. Fork o projeto

#### 2. Crie sua branch

  ```bash
  git checkout -b feature/nova-funcionalidade
  ```

#### 3. Commit suas alterações

  ```bash
  git commit -am 'Adiciona nova funcionalidade'
  ```

#### 4. Push para a branch

  ```bash
  git push origin feature/nova-funcionalidade
  ```

#### 5. Abra um Pull Request

### 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

### 👥 Autor

**Cristiano** - [CrisisUp](https://github.com/CrisisUp)

---

## 🙏 Agradecimentos

- [Express](https://expressjs.com/)
- [PostgreSQL](https://www.postgresql.org/)
- [Prometheus](https://prometheus.io/)
- [Grafana](https://grafana.com/)
- [Docker](https://www.docker.com/)

---

**⭐ Se este projeto te ajudou, considere dar uma estrela no GitHub!**

*Feito com ❤️ para controle de estoque eficiente.*

## Adicionar ao Git

  ```bash
  git add README.md
  git commit -m "📝 Adiciona README.md completo e bonitão"
  git push origin main
  ```
