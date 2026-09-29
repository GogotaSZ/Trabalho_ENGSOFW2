# Sistema de Monitoramento de Tempo Parado em Roteiros

MVP acadêmico para registrar e acompanhar o tempo parado de motoristas, motoboys ou transportadores durante seus roteiros diários desenvolvido na matéria de Engenharia de Software 2.

---

# Alunos

- Guilherme Henrique da Silva Teodoro
- Raphael Oliveira de Araujo
- Yasmin Torres Moreira dos Santos


# Objetivo

O sistema deverá permitir:

- cadastrar motoristas/motoboys;
- cadastrar usuários responsáveis pelo gerenciamento;
- criar roteiros associados a um motorista e a uma data;
- adicionar pontos em ordem sequencial ao roteiro;
- registrar chegada e saída em cada ponto;
- calcular automaticamente o tempo parado;
- desconsiderar o primeiro ponto do roteiro no cálculo de tempo parado;
- calcular o tempo total parado no roteiro;
- registrar distância e custo estimado do roteiro;
- consultar histórico por período;
- exibir gráficos de tempo parado por dia, mês e período;
- permitir alteração dos parâmetros básicos do sistema;
- controlar acesso por perfil.

---

# Tecnologias

## Frontend

| Tecnologia | Utilização |
|---|---|
| **React** | Construção da interface |
| **TypeScript** | Tipagem e organização do código |
| **Vite** | Criação e execução do projeto |
| **React Router** | Navegação entre páginas |
| **Recharts** | Gráficos do dashboard |

A estilização será feita com **CSS comum**, evitando adicionar bibliotecas de interface desnecessárias.

As chamadas para a API poderão ser feitas utilizando o próprio `fetch` do navegador.

---

## Backend

| Tecnologia | Utilização |
|---|---|
| **Java** | Linguagem do backend |
| **Spring Boot** | Criação da API REST |
| **Spring Data JPA** | Persistência e acesso ao banco |
| **Spring Security** | Login e controle de acesso |

A autenticação poderá utilizar token JWT, mas sem adicionar uma arquitetura complexa de autenticação.

O Spring Boot também já fornece suporte suficiente para validações, tratamento de requisições e testes básicos sem necessidade de muitas bibliotecas adicionais.

---

## Banco de dados

Será utilizado:

**PostgreSQL**

O banco será responsável pela persistência dos dados de:

- usuários;
- motoristas;
- roteiros;
- pontos;
- horários de chegada e saída;
- parâmetros;
- custos.

A estrutura relacional é adequada porque os dados possuem relacionamentos claros entre motorista, roteiro e pontos.

---

## Controle de versão

Será utilizado:

- **Git**
- **GitHub**

---

# Arquitetura

O projeto utilizará uma arquitetura simples em camadas.

```text
Frontend
React
   |
   | HTTP / REST
   v
Backend
Spring Boot
   |
   | JPA
   v
PostgreSQL
```

---

# Estrutura do repositório

```text
projeto/
|
├── backend/
│   └── src/
|
├── frontend/
│   └── src/
|
├── README.md
├── AGENTS.md
└── .gitignore
```

---

# Estrutura do backend

```text
backend/
└── src/main/java/
    └── br/com/projeto/
        ├── controller/
        ├── service/
        ├── repository/
        ├── entity/
        ├── dto/
        └── security/
```

---

# Estrutura do frontend

```text
frontend/
└── src/
    ├── components/
    ├── pages/
    ├── services/
    ├── routes/
    └── types/
```

---


# Regras de negócio principais

## Tempo parado

O primeiro ponto representa a saída do motorista e não conta como tempo parado.

```text
ordem == 1
tempoParado = 0
```

Nos demais pontos:

```text
tempoParado = horarioSaida - horarioChegada
```

O tempo total do roteiro será:

```text
tempoTotalParado =
soma dos tempos parados dos pontos
```

desconsiderando o ponto inicial.

---

## Custo estimado

```text
litrosConsumidos =
distanciaTotal / rendimentoKmLitro
```

```text
custoEstimado =
litrosConsumidos * valorCombustivel
```

---

# Planejamento em 2 Sprints

# Sprint 1 - Backend e funcionalidades principais

## Objetivo

Construir a base do sistema e implementar as principais regras de negócio.

## Atividades

### 1. Configuração do projeto

- Repositório, Spring Boot, PostgreSQL e estrutura inicial.

### 2. Modelagem do banco

- Entidades e relacionamentos principais.

### 3. Cadastro de motoristas

- CRUD de motoristas.

### 4. Autenticação

- Login, perfis e proteção de endpoints.

### 5. Roteiros

- Criar, consultar e organizar roteiros e pontos.

### 6. Registro de chegada e saída

- Registrar chegada e saída dos pontos.

### 7. Cálculo do tempo parado

- Calcular o tempo por ponto e o total, ignorando o primeiro ponto.

### 8. Parâmetros e custos

- Configurar jornada, combustível, rendimento e custo estimado.

### 9. Histórico

- Consultar histórico por período e motorista.

---


---

# Sprint 2 - Frontend, dashboard e finalização

## Objetivo

Criar a interface web e integrar todas as funcionalidades do backend.

## Atividades

### 1. Configuração do frontend

- Configurar React, TypeScript, Vite e rotas.

### 2. Login

- Tela de login e autenticação.

### 3. Layout principal

- Menu principal da aplicação.

### 4. Tela de motoristas

- CRUD de motoristas.

### 5. Tela de roteiros

- Criar, editar e visualizar roteiros e pontos.

### 6. Interface do motorista

- Tela responsiva para roteiro, chegada e saída.

### 7. Histórico

- Filtros e listagem do histórico.

### 8. Dashboard

- Gráficos de tempo parado e custos com Recharts.

### 9. Parâmetros

- Edição de jornada e combustível.

### 10. Testes principais

- Testar regras principais e controle de acesso.

### 11. Revisão final

- Validar funcionalidades, responsividade e persistência.

