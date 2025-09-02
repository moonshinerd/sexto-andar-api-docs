# Arquitetura Selecionada

## Introdução

Este documento descreve a arquitetura escolhida para o sistema **Sexto Andar**, detalhando como os componentes se organizam e interagem para formar uma aplicação web robusta e escalável.

## Visão Geral

O sistema adota uma **arquitetura REST em camadas** combinada com o padrão **MVC (Model-View-Controller)** adaptado para APIs. Esta escolha garante separação clara de responsabilidades, facilita manutenção e permite escalabilidade horizontal.

### Características Principais:

- **API REST** como interface de comunicação
- **Arquitetura em camadas** para organização do código
- **Separação de responsabilidades** entre componentes
- **ORM** para abstração do banco de dados
- **Containerização** para deployment e portabilidade

## Componentes Principais

### 1. **Camada de Apresentação (Controller)**
Implementada pelos **routers do FastAPI**, é responsável por:

- Receber requisições HTTP (GET, POST, PUT, DELETE)
- Validar parâmetros e dados de entrada
- Chamar os serviços apropriados
- Retornar respostas HTTP formatadas
- Documentação automática da API (Swagger/OpenAPI)

### 2. **Camada de Serviços (Business Logic)**
Contém a **lógica de negócio** da aplicação:

- Processamento das regras de negócio
- Validações específicas do domínio
- Coordenação entre diferentes recursos
- Tratamento de exceções de negócio
- Implementação dos casos de uso do sistema

### 3. **Camada de Repositório (Data Access)**
Gerencia o **acesso aos dados** através do SQLAlchemy:

- Operações CRUD (Create, Read, Update, Delete)
- Queries personalizadas ao banco de dados
- Abstração da persistência de dados
- Implementação de padrões como Repository e Unit of Work

### 4. **Camada de Modelo (Entities)**
Define as **entidades do domínio**:

- **Models SQLAlchemy**: Mapeamento objeto-relacional das tabelas
- **Pydantic Models**: Validação e serialização de dados
- **DTOs (Data Transfer Objects)**: Objetos para transferência de dados
- Relacionamentos entre entidades

## Padrão MVC Adaptado

### **Model (Modelo)**

- **Entidades SQLAlchemy**: Representam as tabelas do banco
- **Pydantic Models**: Validação e serialização
- **Repositórios**: Acesso aos dados
- Responsável pela persistência e regras de dados

### **View (Visão)**

- **Frontend React**: Interface de usuário
- **Respostas JSON**: Dados formatados pela API
- **Documentação Swagger**: Interface de documentação
- Responsável pela apresentação dos dados

### **Controller (Controlador)**

- **FastAPI Routers**: Endpoints da API
- **Services**: Lógica de negócio
- **Middleware**: Interceptação de requisições
- Responsável pelo fluxo de controle da aplicação

## Utilização do ORM

O **SQLAlchemy** atua como camada de abstração entre a aplicação e o banco de dados PostgreSQL:

### **Mapeamento Objeto-Relacional**

- Classes Python mapeadas para tabelas do banco
- Relacionamentos declarativos entre entidades
- Lazy loading e eager loading de dados relacionados

### **Session Management**

- Gerenciamento automático de transações
- Connection pooling para performance
- Rollback automático em caso de erro

### **Query Builder**

- Queries expressivas em Python
- Proteção contra SQL injection
- Otimização automática de consultas

## Fluxo de Requisição

1. **Cliente** faz requisição HTTP para a API
2. **FastAPI Router** recebe e valida a requisição
3. **Service Layer** processa a lógica de negócio
4. **Repository** acessa dados via SQLAlchemy
5. **SQLAlchemy** executa queries no PostgreSQL
6. **Resposta** é formatada e retornada ao cliente

## Benefícios da Arquitetura

- **Manutenibilidade**: Código organizado em camadas
- **Testabilidade**: Cada camada pode ser testada isoladamente
- **Escalabilidade**: Componentes podem escalar independentemente
- **Flexibilidade**: Fácil alteração de implementações específicas
- **Reusabilidade**: Serviços podem ser reutilizados por diferentes controllers
