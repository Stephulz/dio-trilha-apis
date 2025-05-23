# 🔍 Azure Cognitive Search: Utilizando AI Search para Indexação e Consulta de Dados

O **Azure Cognitive Search** é um serviço gerenciado de busca na nuvem que permite criar experiências avançadas de pesquisa com suporte a IA, como análise de linguagem natural, OCR e extração de conteúdo.

---

## 🧠 O que é AI Search?

**AI Search** combina as funcionalidades de busca do Azure com **recursos cognitivos** (Cognitive Services) para extrair, enriquecer e indexar dados não estruturados (PDFs, imagens, textos, etc.).

---

## 🎯 Principais Funcionalidades

- Indexação de dados estruturados e não estruturados
- Consultas full-text (busca por palavras-chave)
- Integração com Azure Cognitive Services (OCR, análise de sentimentos, PII, etc.)
- Enriquecimento de conteúdo via "skillsets"
- Facetas, filtros e rankings personalizados

---

## ✅ Pré-requisitos

- Conta ativa no Azure
- Recurso do tipo **Azure Cognitive Search** criado
- Fonte de dados (Azure Blob Storage, SQL Database, Cosmos DB, etc.)

---

## 🚀 Passo a Passo: Criando uma Solução com AI Search

### 1. Criar um serviço de Azure Cognitive Search

1. No [Portal Azure](https://portal.azure.com):
   - Acesse **"Criar recurso" > "Search"**
   - Selecione **Azure Cognitive Search**
   - Defina o nome, região e nível (Free, Basic, Standard)

---

### 2. Criar a Fonte de Dados

Você pode usar:
- Azure Blob Storage (ex: PDFs, docs, imagens)
- SQL Server, Cosmos DB ou qualquer base conectável

No menu do Search, vá em **"Data Sources"** e clique em **"Adicionar"**.

---

### 3. Criar um Skillset (opcional)

Os **skillsets** são fluxos de enriquecimento com IA. Exemplo de skills:
- OCR (leitura de texto de imagens)
- Detecção de entidades nomeadas
- Tradução
- Extração de linguagem-chave

Você pode combinar skills pré-definidos ou criar **skills customizadas com Azure Functions**.

---

### 4. Criar o Indexador

- Vá em **"Indexers" > "Adicionar indexador"**
- Escolha a fonte de dados e o skillset
- Defina a frequência (on-demand ou periódica)

---

### 5. Criar o Índice de Busca

- Vá em **"Indexes" > "Adicionar índice"**
- Configure os campos (ex: título, conteúdo, categoria)
  - Defina se cada campo será:
    - Pesquisável (`searchable`)
    - Filtrável (`filterable`)
    - Ordenável (`sortable`)
    - Facetável (`facetable`)

---

### 6. Consultar Dados com a API de Pesquisa

Você pode consultar via:
- **SDKs (C#, Python, JavaScript...)**
- **REST API**
- Ferramentas como **Postman** ou diretamente no portal

Exemplo de requisição:

```http
GET https://<nome-do-servico>.search.windows.net/indexes/<nome-do-indice>/docs?search=azure&api-version=2023-07-01-Preview
api-key: <sua-chave-de-admin>
