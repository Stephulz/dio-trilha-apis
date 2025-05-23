# 🧠 Análise de Sentimentos com Language Studio no Azure AI

Este guia apresenta como realizar uma **análise de sentimentos** utilizando o **Azure AI Language Studio**, ferramenta da Microsoft para processamento de linguagem natural (NLP) na nuvem.

---

## 📌 O que é a Análise de Sentimentos?

A Análise de Sentimentos permite **avaliar automaticamente o tom emocional de textos**, classificando-os como:
- **Positivo**
- **Negativo**
- **Neutro**
- **Misto** (sentimentos contraditórios no mesmo texto)

---

## 🛠️ O que é o Azure AI Language Studio?

O **Language Studio** é uma interface gráfica baseada na web para testar e usar os recursos de linguagem do Azure AI, como:
- Análise de sentimentos
- Extração de entidades
- Reconhecimento de linguagem
- Resumo automático
- Tradução e muito mais

Acesse: [https://language.azure.com](https://language.azure.com)

---

## ✅ Pré-requisitos

- Conta Azure ativa
- Um recurso de **"Serviço de linguagem"** (Language Resource) criado no portal Azure
- Permissões para acessar o recurso via Language Studio

---

## 🚀 Passo a Passo – Análise de Sentimentos

### 1. Acesse o Language Studio
- Vá para [https://language.azure.com](https://language.azure.com)
- Faça login com sua conta da Azure

### 2. Selecione “Análise de Sentimentos”
- No painel lateral, clique em **"Análise de sentimentos"**
- Escolha a **linguagem** (Português é suportado)

### 3. Selecione o recurso de linguagem
- Escolha o recurso Azure Language que você criou previamente
- Ou clique em **"Criar novo recurso"** se ainda não tiver um

### 4. Insira o texto a ser analisado
Exemplo:
```text
Estou muito feliz com o atendimento! Mas a entrega atrasou.
