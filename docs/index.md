<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
# Sistema de Gestão para a Farmácia Vida Saudável
</center></font>

**Conteúdo**

- [Autores](#autores)
- [Descrição do Projeto](#descrição-do-projeto)
- [Análise de Requisitos](#análise-de-requisitos-funcionais-e-não-funcionais)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Sequencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* Ana Clara Soares
* Dayô Araujo
* Enzo Viana


# Descrição do Projeto
Objetivo: Desenvolver um sistema para modernizar a gestão da Farmácia Vida Saudável, automatizando o controle de vendas, estoque e clientes.

Principais Funcionalidades:

* Cadastro de medicamentos, produtos e clientes.
* Registro de vendas com atualização automática do estoque.
* Geração de relatórios gerenciais.
* Controle de acesso para atendentes e administradores.
* Fluxo Básico: O atendente consulta produtos, registra a venda e o estoque é atualizado. O administrador pode acessar relatórios.

Fases do Projeto:
* Análise de requisitos
* Modelagem UML (casos de uso, atividades, classes, sequência e implantação).

# Análise de Requisitos Funcionais e Não-Funcionais

| ID | RF | DESCRIÇÃO |
|-----|----|----------|
|RF_01| Cadastro | Permitir o cadastro, edição de dados e exclusão de clientes, incluindo dados pessoais (CPF, Nome, Endereço e Telefone).|
|RF_02| Cadastro | Permitir o cadastro, edição de dados e exclusão de produtos e medicamentos, incluindo dados (Nome, Código, Descrição, Lote, Data de Validade, Quantidade de Estoque).|
|RF_03| Venda | Possibilitar a realização de vendas, associar o cliente e os produtos comprados, gerar um recibo digital/físico.|
|RF_04| Venda | Calcular automaticamente o total da compra e aplicar descontos, se houver. |
|RF_05| Consulta | Consultar o histórico de compras do cliente.|
|RF_06| Consulta | Consultar a disponibilidade de produtos por código ou nome.|
|RF_07| Estoque | O sistema deve enviar um alerta se houver produtos próximos da validade.|
|RF_08| Estoque | Gerenciamento de estoque, mostrar a quantidade de produtos em estoque.|
|RF_09| Relatório | Gerar relatório de vendas diárias, semanais e mensais.|
|RF_10| Relatório | Gerar relatório de medicamentos e produtos disponíveis.|
|RF_11| Pagamento | Integrar-se a um sistema de pagamento para processar cartões de crédito e débito.|

| ID | RNF | DESCRIÇÃO |
|-------|-------|-------|
|RNF_01|Disponibilidade|O sistema deve possuir uma alta Disponibilidade.|
|RNF_02|Acessibilidade|O sistema deve ser acessível para o maximo de dispositivos possiveis.|
|RNF_03|Desempenho|O tempo de resposta da consulta e respota do sitema deve ser ágil.|
|RNF_04|Segurança e Conformidade|Os dados dos clientes e das transações devem sert armazenados de forma segura, garantindo conformidade com a LGPD(Lei Geral de Poteção de Dados).|
|RNF_05|Segurança|O sistema deve exigir autenticação dos funcionários para acesso ás funções administrativas.|
|RNF_06|Segurança|O banco de dados deve ser preotegido com criptografia para evitar acessos não autorizados.|
|RNF_07|Escalabilidade|O sistema deve suportar um número razoável de usuários simultâneos sem degradação no desempenho.|
|RNF_08|Backup|O sitema deve realizar backups automáticos diariamente.|
|RNF_09|Usabilidade|A interface do usário deve ser intuitiva e responsiva, adaptando-se a diferentes dispositivos.|
|RNF_10|Auditoria de Log|O sistema deve permitir auditoria de todas as transações realizadas. Os logs devem ser armazenados por no minímo 05 anos e protegidos contra alteração ou exclusão.|

# Diagrama de Atividades

![Image](https://github.com/user-attachments/assets/37e94a2f-8ca2-4667-993b-38c87dca5488)

# Diagrama de Casos de Uso

![Image](https://github.com/user-attachments/assets/3236bc1c-2f41-47a5-b55b-e368e352120a)

# Descrição dos Casos de Uso

|Especificações de Casos de Uso||
|------------------------------|-|
|**Identificador:**|Login|
|**Nome:**|Realizar Login|
|**Atores:**|Atendente, Administrador|
|**Descrição:**|Permite que o usuário se autentique no sistema, fornecendo suas credenciais.|
|**Pré-condição:**|O usuário deve possuir uma conta previamente cadastrada no sistema.|
|**Pós-condição:**|O usuário é autenticado e acessa a área correspondente do sistema.|
|**Pontos de Inclusão:**|N/A|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal||
|---------------|-|
|**Ações do Ator**|**Ações do Sistema**|
|O ator insere seu nome de usuário e senha.||
||O sistema valida as credenciais.|
||O sistema autentica o ator e o direciona para a área correspondente de usuário comum.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso||
|------------------------------|-|
|**Identificador:**|Realizar vendas|
|**Nome:**|Realizar vendas|
|**Atores:**|Atendente|
|**Descrição:**|Permite que o atendente registre a venda de produtos para um cliente.|
|**Pré-condição:**|O atendente deve estar autenticado no sistema.|
|**Pós-condição:**|A venda é registrada no sistema.|
|**Pontos de Inclusão:**|Atualizar Estoque|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal||
|---------------|-|
|**Ações do Ator**|**Ações do Sistema**|
|O atendente seleciona os produtos a serem vendidos.||
||O sistema calcula o valor total da venda.|
|O atendente confirma a venda.||
||O sistema registra a venda e atualiza o estoque.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso||
|------------------------------|-|
|**Identificador:**|Consultar Estoque|
|**Nome:**|Consultar Estoque|
|**Atores:**|Atendente|
|**Descrição:**|Permite ao atendente visualizar as quantidades disponíveis de produtos em estoque.|
|**Pré-condição:**|O atendente deve estar autenticado no sistema.|
|**Pós-condição:**|O sistema exibe as informações sobre o estoque.|
|**Pontos de Inclusão:**|N/A|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal||
|---------------|-|
|**Ações do Ator**|**Ações do Sistema**|
|O atendente acessa a seção de estoque.||
||O sistema exibe a lista de produtos e suas quantidades disponíveis.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso||
|------------------------------|-|
|**Identificador:**|Cadastrar Cliente|
|**Nome:**|Cadastrar Cliente|
|**Atores:**|Atendente|
|**Descrição:**|Permite ao atendente registrar um novo cliente no sistema.|
|**Pré-condição:**|O atendente deve estar autenticado no sistema.|
|**Pós-condição:**|O cliente é registrado no banco de dados.|
|**Pontos de Inclusão:**|N/A|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal||
|---------------|-|
|**Ações do Ator**|**Ações do Sistema**|
|O atendente acessa a opção de cadastro de clientes.||
|O atendente insere os dados do novo cliente.||
||O sistema valida os dados e armazena as informações.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso| |
|------------------------------|--|
|**Identificador:**|Atualizar Estoque|
|**Nome:**|Atualizar Estoque|
|**Atores:**|Administrador|
|**Descrição:**|Permite que o administrador atualize a quantidade e o valor dos produtos disponíveis no estoque.|
|**Pré-condição:**|O administrador deve estar autenticado no sistema.|
|**Pós-condição:**|O estoque é atualizado com as novas quantidades e valores.|
|**Pontos de Inclusão:**|Relizar Vendas, Cadastrar Produtos|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal| |
|---------------|--|
|**Ações do Ator**|**Ações do Sistema**|
|O administrador acessa a opção de atualização de estoque.| |
|O administrador insere os novos valores de produtos.||
||O sistema atualiza as informações no banco de dados.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso| |
|------------------------------|--|
|**Identificador:**|Visualizar Histórico|
|**Nome:**|Visualizar Histórico|
|**Atores:**|Administrador|
|**Descrição:**|Permite ao administrador visualizar o histórico de vendas e atividades do sistema.|
|**Pré-condição:**|O administrador deve estar autenticado no sistema.|
|**Pós-condição:**|O sistema exibe o histórico solicitado.|
|**Pontos de Inclusão:**|N/A|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal| |
|---------------|--|
|**Ações do Ator**|**Ações do Sistema**|
|O administrador acessa a opção de histórico do sistema.||
||O sistema exibe as vendas e registros anteriores.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso| |
|------------------------------|--|
|**Identificador:**|Cadastrar Produtos|
|**Nome:**|Cadastrar Produtos|
|**Atores:**|Administrador|
|**Descrição:**|Permite que o administrador adicione novos produtos ao sistema.|
|**Pré-condição:**|O administrador deve estar autenticado no sistema.|
|**Pós-condição:**|O produto é cadastrado no banco de dados.|
|**Pontos de Inclusão:**|Atualizar Estoque|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal| |
|---------------|--|
|**Ações do Ator**|**Ações do Sistema**|
|O administrador acessa a seção de cadastro de produtos.| |
|O administrador insere os dados do novo produto.||
||O sistema valida e armazena as informações.|

<br/>
<br/>
<br/>

|Especificações de Casos de Uso| |
|------------------------------|--|
|**Identificador:**|Gerar Relatórios|
|**Nome:**|Gerar Relatórios|
|**Atores:**|Administrador|
|**Descrição:**|Permite que o administrador gere relatórios sobre vendas, estoque e clientes.|
|**Pré-condição:**|O administrador deve estar autenticado no sistema.|
|**Pós-condição:**|O relatório é gerado e exibido ao administrador.|
|**Pontos de Inclusão:**|N/A|
|**Pontos de Extensão:**|N/A|

|Fluxo Principal| |
|---------------|--|
|**Ações do Ator**|**Ações do Sistema**|
|O administrador acessa a opção de relatórios.||
|O administrador seleciona o tipo de relatório desejado.||
||O sistema gera e exibe o relatório.|


# Diagrama de Sequência

![Image](https://github.com/user-attachments/assets/4c7de7a6-061f-4eb2-a6ea-e641d5aede6a)

# Diagrama de Classes

![Image](https://github.com/user-attachments/assets/def32f81-223d-44bd-981d-bafff0364238)

# Diagrama de Estados

![Image](https://github.com/user-attachments/assets/d47bb5c5-45c0-435d-bd38-fc5764f9d751)

# Diagrama de Implantação

![Image](https://github.com/user-attachments/assets/929e4aa8-f5a9-4260-8b50-459d9082e3ea)

# Referências

*&lt;Lista de referências&gt;*
