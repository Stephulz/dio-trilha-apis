# 🛠️ Configurando uma Instância de Banco de Dados no Microsoft Azure (SQL Server)

Este guia apresenta as etapas para criar e configurar uma instância de banco de dados SQL Server no Azure, utilizando o serviço gerenciado **Azure SQL Database**.

---

## ✅ 1. Acessar o Portal do Azure
- Acesse: [https://portal.azure.com](https://portal.azure.com)
- Faça login com sua conta Microsoft.

---

## ✅ 2. Criar um Banco de Dados SQL

### a) Navegar até o serviço
- No menu lateral esquerdo, clique em **"Criar um recurso"**
- Vá até **Banco de Dados** > **Banco de Dados SQL**

### b) Configuração básica
- **Assinatura**: escolha a assinatura ativa.
- **Grupo de recursos**: selecione um existente ou crie um novo.
- **Nome do banco de dados**: ex: `meuBancoSql`
- **Servidor**: clique em **Criar novo** e preencha:
  - Nome do servidor (ex: `meuservidor123`)
  - Login de administrador (ex: `adminsql`)
  - Senha e confirmação de senha
  - Região (próxima dos usuários ou de menor custo)

---

## ✅ 3. Selecionar Plano e Preço (Camada de Serviço)

### a) Escolher tipo de compra
- **Uso baseado em DTU** (mais simples) ou **vCore** (mais controlado)

### b) Camada de serviço
- Exemplos:
  - **Básico** – até 2GB
  - **Standard** – até 250GB
  - **Premium** – IOPS e alta disponibilidade

> 💡 **Dica**: Use a calculadora do Azure para prever custos.

---

## ✅ 4. Configuração Adicional (opcional)
- **Colação**: define regras de ordenação e sensibilidade a maiúsculas/minúsculas.
- **Backup**: por padrão, o Azure já realiza backups automáticos.

---

## ✅ 5. Rede
- Configure o **acesso à rede**:
  - Permitir acesso de **serviços do Azure** (opcional)
  - Adicionar o IP do seu computador para conexão externa

---

## ✅ 6. Revisar + Criar
- Verifique todas as configurações.
- Clique em **“Criar”**.
- Aguarde a implantação (poucos minutos).

---

## ✅ 7. Conectar ao Banco de Dados

### a) Obter cadeia de conexão
- Acesse o recurso do banco criado.
- No menu lateral, vá em **"Cadeias de conexão"**.
- Copie a string de conexão adequada (ADO.NET, JDBC, ODBC, etc).
