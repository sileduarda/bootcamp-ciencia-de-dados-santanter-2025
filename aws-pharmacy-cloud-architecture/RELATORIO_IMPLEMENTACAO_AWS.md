# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 13/02/2026  
Empresa: Abstergo Industries  
Responsável: Maria Eduarda Souza Silva  

---

## 1. Introdução

Este relatório apresenta o processo de implementação de serviços em nuvem na empresa Abstergo Industries, com foco na construção da infraestrutura de uma farmácia virtual utilizando a Amazon Web Services (AWS).

O objetivo principal foi selecionar três serviços estratégicos da AWS com foco na redução imediata de custos operacionais, aumento da escalabilidade e melhoria da segurança da informação.

---

## 2. Objetivo do Projeto

- Migrar de modelo hipotético on-premises para nuvem
- Reduzir custos com infraestrutura física
- Garantir alta disponibilidade básica
- Implementar boas práticas de segurança em rede
- Criar base escalável para crescimento futuro

---

## 3. Serviços Implementados

### Etapa 1 – Camada de Aplicação

Serviço: Amazon EC2  
Foco: Computação em nuvem sob demanda  

#### Caso de Uso

O Amazon EC2 foi utilizado para hospedar o servidor de aplicação da farmácia virtual, responsável por:

- Processamento de requisições HTTP/HTTPS
- Autenticação de usuários
- Processamento de pedidos
- Comunicação com banco de dados

#### Benefícios

- Modelo pay-as-you-go
- Eliminação de servidores físicos
- Escalabilidade vertical sob demanda

---

### Etapa 2 – Camada de Dados

Serviço: Amazon RDS  
Foco: Banco de dados relacional gerenciado  

#### Caso de Uso

O Amazon RDS foi utilizado para armazenar:

- Cadastro de clientes
- Catálogo de medicamentos
- Histórico de pedidos
- Controle de estoque

O banco foi configurado em subnet privada para garantir isolamento de rede.

#### Benefícios

- Backup automático
- Atualizações gerenciadas
- Redução de custo operacional com DBA
- Alta disponibilidade opcional (Multi-AZ)

---

### Etapa 3 – Camada de Armazenamento

Serviço: Amazon S3  
Foco: Armazenamento de objetos escalável  

#### Caso de Uso

O Amazon S3 foi utilizado para:

- Armazenamento de imagens dos produtos
- Armazenamento de documentos fiscais
- Backup de arquivos da aplicação

#### Benefícios

- Alta durabilidade (11 noves)
- Versionamento
- Classes de armazenamento otimizadas para custo
- Escalabilidade automática

---

## 4. Arquitetura Implementada

A arquitetura foi estruturada com:

- 1 VPC
- 1 Subnet Pública (EC2)
- 1 Subnet Privada (RDS)
- Internet Gateway
- Security Groups restritivos

Fluxo de comunicação:

Usuário → Internet → EC2 → RDS  
EC2 → S3  

O banco de dados não possui acesso direto à internet, garantindo maior segurança.

---

## 5. Estratégia de Redução de Custos

- Eliminação de CapEx (hardware físico)
- Uso de instâncias sob demanda
- Banco de dados gerenciado reduzindo custo humano
- Utilização de classes de armazenamento S3 para arquivos frios
- Escalabilidade conforme demanda

---

## 6. Resultados Esperados

- Redução de custos operacionais imediatos
- Maior segurança da informação
- Arquitetura preparada para crescimento
- Alta confiabilidade da plataforma

---

## 7. Conclusão

A implementação dos serviços Amazon EC2, Amazon RDS e Amazon S3 permitiu a construção de uma arquitetura em nuvem segura, escalável e economicamente viável para a farmácia virtual da Abstergo Industries.

Recomenda-se como evolução futura:

- Implementação de Load Balancer
- Auto Scaling
- Multi-AZ
- Monitoramento com CloudWatch
- Políticas avançadas de IAM
