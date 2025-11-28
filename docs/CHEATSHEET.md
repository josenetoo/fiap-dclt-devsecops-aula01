# Aula 01 - Cheatsheet

## AWS CLI

```bash
# Configurar profile
aws configure --profile fiapaws

# Testar conexão
aws sts get-caller-identity --profile fiapaws

# Criar repositório ECR
aws ecr create-repository --repository-name devsecops-app --profile fiapaws

# Login no ECR
aws ecr get-login-password --profile fiapaws | docker login --username AWS --password-stdin <ACCOUNT_ID>.dkr.ecr.us-east-1.amazonaws.com
```

## Docker

```bash
# Build (amd64 para ECS)
docker build --platform linux/amd64 -t devsecops-app .

# Tag
docker tag devsecops-app:latest <ECR_URI>:latest

# Push
docker push <ECR_URI>:latest

# Run local
docker run -p 5000:5000 devsecops-app
```

## ECS

```bash
# Force deploy
aws ecs update-service \
  --cluster devsecops-cluster \
  --service devsecops-service \
  --force-new-deployment \
  --profile fiapaws

# Listar tasks
aws ecs list-tasks \
  --cluster devsecops-cluster \
  --profile fiapaws
```

## Secrets GitHub

| Secret | Origem |
|--------|--------|
| `AWS_ACCESS_KEY_ID` | Learner Lab > AWS Details |
| `AWS_SECRET_ACCESS_KEY` | Learner Lab > AWS Details |
| `AWS_SESSION_TOKEN` | Learner Lab > AWS Details |

## Valores do Lab

| Recurso | Valor |
|---------|-------|
| Region | `us-east-1` |
| Profile | `fiapaws` |
| Task Role | `LabRole` |
| VPC | default |
