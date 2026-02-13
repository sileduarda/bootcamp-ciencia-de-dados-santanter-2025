# 💊 AWS Pharmacy Cloud Architecture

Projeto desenvolvido como desafio de bootcamp com objetivo de projetar a arquitetura em nuvem de uma farmácia virtual utilizando serviços da AWS.

## 🎯 Objetivo

Projetar uma arquitetura escalável, segura e de baixo custo utilizando:

- Amazon EC2
- Amazon S3
- Amazon RDS

Foco principal:
- Redução de custos operacionais
- Alta disponibilidade
- Escalabilidade sob demanda
- Segurança de dados

---

## 🏗️ Arquitetura da Solução

A arquitetura é composta por:

Usuário → EC2 (Aplicação Web) → RDS (Banco de Dados)
                              ↓
                             S3 (Armazenamento)

### Serviços Utilizados

- Amazon EC2 — Servidor de aplicação
- Amazon RDS — Banco de dados relacional gerenciado
- Amazon S3 — Armazenamento de objetos

---

## 💰 Estratégia de Redução de Custos

- Eliminação de servidores físicos
- Modelo pay-as-you-go
- Classes de armazenamento no S3 otimizadas para custo
- Banco de dados gerenciado reduzindo custo operacional

---

## 📊 Diagrama de Arquitetura

O diagrama pode ser encontrado na pasta:

architecture/

---

## 👩‍💻 Autora

Maria Eduarda Souza Silva
- [LinkedIn](https://www.linkedin.com/in/sileduarda/)