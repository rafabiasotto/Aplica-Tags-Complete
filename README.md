# 🚀 Azure Governance Automation – TAGs & Policies via CSV

Este repositório contém um script em **PowerShell + Azure CLI** para **automatizar governança no Azure**, aplicando **TAGs**, criando **Policy Assignments** e executando **remediações**, tudo a partir de uma **planilha CSV**.

A solução foi criada para reduzir trabalho manual, padronizar ambientes e facilitar práticas de **FinOps, compliance e governança corporativa**, mesmo em ambientes com dezenas de Resource Groups e múltiplas assinaturas.

---

## ✨ Funcionalidades

- 📊 Leitura de dados a partir de arquivo **CSV**
- 🔁 Troca automática de **assinatura Azure**
- 🏷️ Aplicação de TAGs em **Resource Groups**
- 📜 Criação de **Policy Assignments** (herança de TAGs)
- 🛠️ Execução automática de **remediações**
- 🔄 Reexecução segura do script
- 📦 Suporte a múltiplas assinaturas no mesmo arquivo

---

## 📋 Pré-requisitos

Antes de executar o script, você precisa ter:

- **PowerShell 7+**
- **Azure CLI** instalado
- Login ativo no Azure
- Permissões mínimas:
  - `Contributor` no Resource Group
  - Permissão para criar **Policy Assignments** e **Remediações**
- A policy **“Inherit a tag from the resource group if missing”** já existente no tenant

---

## 🔐 Autenticação no Azure

Execute antes de rodar o script:

```powershell
az login
