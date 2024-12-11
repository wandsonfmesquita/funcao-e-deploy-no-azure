# Criando e Fazendo Deploy de Funções no Microsoft Azure

## Passo 1: Acesse o Portal do Azure
- Faça login no [Portal do Azure](https://portal.azure.com).

## Passo 2: Crie um Recurso de Funções
1. No menu lateral, clique em **"Criar um recurso"**.
2. Na barra de pesquisa, digite **"Azure Function"** e selecione-o.
3. Clique em **"Criar"**.

## Passo 3: Configure a Aplicação de Funções
1. **Grupo de Recursos**:
   - Selecione um grupo existente ou crie um novo.
2. **Nome da Função**:
   - Escolha um nome único para a aplicação de funções.
3. **Plano de Hospedagem**:
   - Opte pelo plano **"Consumo (Serverless)"** para pagar apenas pelo uso.
4. **Sistema Operacional**:
   - Escolha Windows ou Linux.
5. **Runtime Stack**:
   - Escolha a linguagem (ex: .NET, Node.js, Python).

Clique em **"Criar"** e aguarde a implantação.

## Passo 4: Crie uma Função
1. Acesse sua aplicação de funções no portal.
2. Clique em **"Funções" > "Adicionar"**.
3. Escolha um **gatilho** (ex: HTTP, Timer, Blob Storage).
4. Configure os detalhes da função e salve.

## Passo 5: Desenvolva e Faça o Deploy
1. **Desenvolvendo Localmente**:
   - Instale o [Azure Functions Core Tools](https://learn.microsoft.com/en-us/azure/azure-functions/functions-run-local).
   - Crie um projeto de função local com:
     ```bash
     func init MyFunctionApp
     cd MyFunctionApp
     func new
     ```
2. **Fazendo o Deploy**:
   - Faça login no Azure via CLI:
     ```bash
     az login
     ```
   - Faça o deploy da aplicação:
     ```bash
     func azure functionapp publish <NOME_DA_APLICACAO>
     ```

## Passo 6: Teste sua Função
- No portal do Azure, acesse a URL da função gerada.
- Teste os gatilhos (ex: HTTP) com ferramentas como Postman ou Curl.

Sua aplicação está agora publicada e funcional no Azure!

