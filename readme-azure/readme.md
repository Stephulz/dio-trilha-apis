# 🖥️ Criação e Configuração de uma Máquina Virtual no Microsoft Azure

## ✅ 1. Acessar o Portal do Azure
- Acesse: [https://portal.azure.com](https://portal.azure.com)
- Faça login com sua conta Microsoft.

---

## ✅ 2. Criar uma Máquina Virtual
1. No painel principal, clique em **"Criar um recurso"**
2. Selecione **"Máquina virtual"**

---

## ✅ 3. Configuração Básica

### a) Assinatura e Grupo de Recursos
- **Assinatura**: escolha a assinatura disponível.
- **Grupo de Recursos**: selecione um existente ou clique em *Criar novo*.

### b) Detalhes da Instância
- **Nome da VM**: ex. `vm-linux-web01`
- **Região**: selecione a mais próxima do seu público.
- **Opções de Disponibilidade**:
  - Zona de disponibilidade (opcional)
  - Conjunto de disponibilidade (alta disponibilidade)

### c) Imagem do Sistema Operacional
- Exemplos:
  - `Ubuntu Server 22.04 LTS`
  - `Windows Server 2022 Datacenter`

### d) Tamanho da Máquina
- Clique em **Selecionar tamanho**
- Exemplo: `Standard_B2s` (uso geral e baixo custo)

### e) Autenticação
- **Usuário e senha** (para Windows)
- **Usuário e chave SSH** (para Linux)

---

## ✅ 4. Disco
- Tipo do disco do sistema operacional:
  - `Padrão HDD`
  - `Padrão SSD`
  - `Premium SSD`
- Discos adicionais podem ser adicionados nesta etapa ou posteriormente.

---

## ✅ 5. Rede

### a) Rede Virtual
- Selecione uma existente ou crie uma nova.
- Configure a sub-rede.

### b) IP Público
- Habilite para permitir acesso externo.

### c) Portas de Entrada
- Marque as portas de acesso:
  - `22 (SSH)` para Linux
  - `3389 (RDP)` para Windows
  - `80`, `443` para aplicações web

---

## ✅ 6. Gerenciamento (Opcional)
- Habilitar opções como:
  - Diagnóstico de inicialização
  - Azure Monitor
  - Backup
  - Auto desligamento

---

## ✅ 7. Revisar + Criar
- Verifique o resumo da configuração.
- Clique em **“Criar”**.
- Aguarde a implantação da máquina (leva poucos minutos).

---

## ✅ 8. Acessar a Máquina Virtual

### Linux:
```bash
ssh azureuser@<IP-Público>
