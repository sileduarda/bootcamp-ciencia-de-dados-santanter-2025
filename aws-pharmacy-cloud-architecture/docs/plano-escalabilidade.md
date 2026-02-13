# Plano de Escalabilidade

## Situação Atual

- Arquitetura Single-AZ
- 1 instância EC2
- 1 instância RDS

## Evoluções Futuras

### 1. Auto Scaling
Permitir escalabilidade automática do EC2 conforme demanda.

### 2. Load Balancer
Distribuir requisições entre múltiplas instâncias.

### 3. Multi-AZ para RDS
Alta disponibilidade com failover automático.

### 4. CDN (CloudFront)
Melhorar performance global para imagens do S3.

---

## Objetivo Final

Transformar arquitetura básica em arquitetura altamente disponível, resiliente e escalável.
