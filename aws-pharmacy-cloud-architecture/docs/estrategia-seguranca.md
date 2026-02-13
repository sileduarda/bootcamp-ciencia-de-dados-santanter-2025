# Estratégia de Segurança

## 1. Isolamento de Rede

- VPC dedicada
- Subnet pública para aplicação
- Subnet privada para banco de dados

## 2. Security Groups

### EC2
- HTTP (80)
- HTTPS (443)
- SSH (22) restrito por IP

### RDS
- Porta 3306
- Acesso permitido apenas pelo Security Group da EC2

## 3. Controle de Acesso

- Políticas IAM com princípio do menor privilégio
- Controle de acesso ao S3 via políticas específicas

## 4. Backup

- Backup automático no RDS
- Versionamento habilitado no S3
