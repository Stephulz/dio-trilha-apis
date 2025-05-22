# Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

Este guia fornece um passo a passo para configurar os recursos (CPU, memória, disco) e dimensionamentos (escalabilidade, redimensionamento) de Máquinas Virtuais (VMs) no Microsoft Azure.

---

## 📌 Pré-requisitos

- Conta na Azure com permissões para criar/alterar recursos
- Grupo de recursos existente (ou crie um novo)
- Familiaridade com o [Azure Portal](https://portal.azure.com) ou CLI

---

## 🚀 Criando uma Máquina Virtual com recursos personalizados

### ✅ Usando o Portal Azure

1. Acesse [portal.azure.com](https://portal.azure.com).
2. Vá para **"Máquinas Virtuais"** e clique em **"Criar"** > **"Máquina Virtual"**.
3. Configure:
   - **Assinatura e Grupo de Recursos**
   - **Nome da VM**
   - **Região**
   - **Imagem** (ex: Ubuntu, Windows Server)
   - **Tamanho da VM** (clique em "Alterar tamanho" para escolher vCPU/RAM)
   - **Usuário/admin + autenticação**

4. Clique em **Avançar: Disco**, e configure:
   - Tipo de disco: SSD padrão, Premium SSD, HDD
   - Criptografia, caching e tamanho

5. Em **Rede**, configure:
   - Rede virtual e sub-rede
   - Endereço IP público
   - Grupo de segurança de rede (NSG)

6. Revise e clique em **Criar**.

---

### ✅ Usando CLI

```bash
az vm create \
  --resource-group MeuGrupo \
  --name MinhaVM \
  --image UbuntuLTS \
  --size Standard_B2s \
  --admin-username azureuser \
  --generate-ssh-keys
