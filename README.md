# Azure Infrastructure Deployment (Bicep)

This project deploys a basic production-like infrastructure using Azure Bicep.

## ☁️ What It Deploys:
- Virtual Network (10.0.0.0/16)
- Subnet (10.0.0.0/24)
- Network Security Group (SSH allowed)
- Public IP + NIC
- Ubuntu Linux VM (Standard_B1s)
- Optional: Tagging and logging (coming next version)

## 🔧 Tools Used:
- Azure CLI
- Bicep
- Azure Resource Manager (ARM)

## 💡 Why It Matters:
This repo demonstrates core skills for a cloud engineer:
- Infrastructure-as-code (IaC)
- Azure networking and access control
- Secure Linux VM provisioning

## 🚀 Deployment

```bash
az login
az deployment sub create \
  --location eastus \
  --template-file main.bicep \
  --parameters @parameters.json
