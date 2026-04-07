# Projeto CI/CD e Infraestrutura AWS

## 📌 Visão Geral
Este repositório contém um projeto acadêmico com foco em **boas práticas de engenharia de software**, abordando:

- Licenciamento de software
- Integração Contínua e Deploy Contínuo (CI/CD)
- Infraestrutura em nuvem utilizando AWS

O objetivo é demonstrar organização de repositório, automação de pipeline e planejamento de infraestrutura segura e escalável.

---

## 🧩 Tecnologias Utilizadas

- **Node.js**
- **GitHub Actions** (CI/CD)
- **AWS EC2**
- **AWS RDS**
- **AWS VPC**
- **Git**
- **Docker** (opcional)

---

## 🔄 Pipeline CI/CD

O projeto utiliza **GitHub Actions** para automatizar o fluxo de desenvolvimento.

### Etapas do pipeline:
1. Checkout do código
2. Instalação das dependências
3. Execução de testes automatizados
4. Build da aplicação

O pipeline é executado automaticamente a cada `push` ou `pull request` para a branch `main`.

📁 Arquivo de configuração:  
`.github/workflows/ci-cd.yml`

---

## ☁️ Infraestrutura AWS

A infraestrutura foi planejada seguindo boas práticas de segurança e separação de responsabilidades.

### Componentes:
- **VPC** com sub-rede pública e privada
- **EC2** para hospedagem da aplicação
- **RDS (PostgreSQL)** acessível apenas internamente
- **Security Groups** com regras restritivas

### Destaques:
- A instância EC2 possui **Elastic IP**
- O banco RDS não é exposto à internet
- Acesso SSH restrito por IP

---

## 🔐 Segurança

- EC2:
  - Porta 22 (SSH) liberada apenas para IP autorizado
  - Porta 80 (HTTP) aberta para acesso público
- RDS:
  - Porta 5432 liberada apenas para a EC2

---

## 📂 Estrutura do Repositório
