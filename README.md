# Aula 01 - Pipeline CI/CD Seguro

> **Repositório**: https://github.com/josenetoo/fiap-dclt-devsecops-aula01

## 🎯 Objetivo

Construir um pipeline CI/CD básico com GitHub Actions para deploy de uma aplicação containerizada no AWS ECS.

## 📹 Vídeos desta Aula

| Vídeo | Tema | O que você vai fazer |
|-------|------|---------------------|
| 01 | Setup do Laboratório | Conhecer a arquitetura e fazer deploy manual |
| 02 | Pipeline CI/CD Básico | Criar workflow GitHub Actions para deploy automático |
| 03 | Vetores de Ataque | Identificar vulnerabilidades no pipeline |

## 🏗️ Arquitetura

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│   GitHub     │────▶│   AWS ECR    │────▶│   AWS ECS    │
│   Actions    │     │   (Registry) │     │   (Fargate)  │
└──────────────┘     └──────────────┘     └──────────────┘
```

## 📁 Estrutura do Repositório

```
.
├── app.py                 # Aplicação Flask
├── requirements.txt       # Dependências Python
├── Dockerfile            # Container da aplicação
├── .github/
│   └── workflows/        # (Criado durante a aula)
└── docs/
    ├── HANDS-ON-01-01.md  # Vídeo 1.1 - Setup do Laboratório
    ├── HANDS-ON-01-02.md  # Vídeo 1.2 - Pipeline CI/CD
    ├── HANDS-ON-01-03.md  # Vídeo 1.3 - Vetores de Ataque
    └── CHEATSHEET.md     # Comandos rápidos
```

## Pré-requisitos

- [ ] Conta no GitHub
- [ ] Acesso ao AWS Academy Learner Lab
- [ ] AWS CLI instalado localmente

## 🚀 Como Usar

1. **Fork** este repositório
2. Siga os arquivos hands-on em `docs/HANDS-ON-01-*.md`
3. Configure os secrets no GitHub (instruções no passo a passo)

## 🔑 Secrets Necessários (AWS Learner Lab)

| Secret | Descrição |
|--------|-----------|
| `AWS_ACCESS_KEY_ID` | Access Key do Learner Lab |
| `AWS_SECRET_ACCESS_KEY` | Secret Key do Learner Lab |
| `AWS_SESSION_TOKEN` | Session Token (obrigatório!) |

## 📚 Documentação

| Vídeo | Hands-on |
|-------|----------|
| 01 - Setup do Laboratório | [HANDS-ON-01-01.md](docs/HANDS-ON-01-01.md) |
| 02 - Pipeline CI/CD | [HANDS-ON-01-02.md](docs/HANDS-ON-01-02.md) |
| 03 - Vetores de Ataque | [HANDS-ON-01-03.md](docs/HANDS-ON-01-03.md) |

**Referência rápida**: [Cheatsheet](docs/CHEATSHEET.md)

---

**FIAP - Pós Tech DevSecOps**
