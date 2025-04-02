<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
<h3>Sistema de Gestão para a Farmácia Vida Saudável</h3>
</center></font>

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

* <b>Andre Drumond - 10724048</b>
* <b>Eduardo Rodrigues - 10727042</b>
* <b>Gabriel Henrique - 10439251</b>
* <b>Isaac Koga - 10723323</b>


# Descrição do Projeto

O projeto visa desenvolver um sistema informatizado para a Farmácia Vida Saudável, otimizando vendas, controle de estoque e cadastro de clientes, substituindo o processo manual que causa erros e dificuldades na gestão financeira. 

O sistema permitirá o registro de medicamentos, clientes e vendas, atualizando automaticamente o estoque e gerando relatórios gerenciais. Além disso, contará com controle de acesso para atendentes e administradores. Seguindo diretrizes de modelagem UML, o desenvolvimento incluirá análise de requisitos e diagramas estruturais, garantindo maior precisão, rapidez e eficiência nas operações da farmácia.

# Análise de Requisitos Funcionais e Não-Funcionais
<h3>Requisitos Funcionais (RF)</h3>

<h4>São os requisitos que definem as funcionalidades e comportamentos esperados do sistema:</h4>

<b>RF01 | Cadastro de Clientes:</b> O sistema deve permitir o cadastro de clientes com as seguintes informações: nome completo, CPF, CEP e telefone. Esses dados serão utilizados para histórico de compras e geração de relatórios. 

<b>RF02 | Cadastro de Produtos (Medicamentos):</b> O sistema deve permitir o registro de produtos, contendo nome, lote, data de validade, quantidade em estoque e fabricante. Também deve ser possível informar o preço de venda de cada item. 

<b>RF03 | Realização de Vendas:</b> O sistema deve permitir que um atendente registre uma venda, vinculando os produtos comprados a um cliente previamente cadastrado. 

<b>RF04 | Cálculo de Descontos:</b> Durante a venda, o sistema deve calcular o valor total da compra e aplicar descontos, caso estejam disponíveis ou previstos por regras do sistema (ex: promoções, quantidade, validade próxima, etc.). 

<b>RF05 | Pagamento:</b> O sistema deve registrar o pagamento da compra, aceitando métodos como crédito e débito, e gerar um recibo após a finalização. 

<b>RF06 | Atualização de Estoque:</b> O sistema deve atualizar automaticamente o estoque com base nas quantidades vendidas, garantindo que os dados estejam sempre sincronizados. 

<b>RF07 | Controle de Produtos Próximos da Validade:</b> O sistema deve verificar periodicamente a validade dos produtos e alertar o administrador caso estejam próximos do vencimento. 

<b>RF08 | Histórico de Compras:</b> Cada cliente deve ter um histórico de compras atualizado automaticamente após cada venda, com data, produtos comprados e valor total. 

<b>RF09 | Relatórios de Vendas:</b> O sistema deve gerar relatórios de vendas diárias, semanais e mensais, incluindo informações como produtos mais vendidos e clientes mais frequentes. 

<b>RF10 | Controle de Acesso por Perfil de Usuário:</b> O sistema deve permitir autenticação de usuários com perfis distintos: Atendentes: podem consultar produtos, realizar vendas e acessar o estoque. Administradores: podem cadastrar produtos, gerar relatórios, visualizar histórico e controlar acesso. 


</br>
<h3>Requisitos Não-Funcionais (RNF)</h3> 

<h4>Estes requisitos definem restrições, qualidades e condições do sistema:</h4> 

<b>RNF01 | Usabilidade:</b> O sistema deve possuir uma interface amigável e intuitiva, que facilite o uso por funcionários com diferentes níveis de conhecimento técnico. 

<b>RNF02 | Desempenho:</b> As operações do sistema, como consulta de estoque e finalização de venda, devem ser realizadas em até 2 segundos, garantindo fluidez no atendimento. 

<b>RNF03 | Segurança:</b> Deve haver autenticação de usuários, proteção dos dados pessoais dos clientes e registros das ações feitas no sistema. 

<b>RNF04 | Escalabilidade:</b> O sistema deve estar preparado para crescer em volume de usuários, produtos e vendas, sem perda significativa de desempenho. 

<b>RNF05 | Confiabilidade:</b> O sistema deve garantir a integridade dos dados armazenados, evitando perdas ou duplicações em casos de falhas ou reinicializações. 

<b>RNF06 | Compatibilidade:</b> O sistema deve funcionar em diferentes navegadores modernos e ser compatível com dispositivos desktop e tablets utilizados na farmácia.


</br>

# Diagrama de Atividades

<img src="diagram_atvd.png" alt="atividades">


# Diagrama de Casos de Uso

<img src="diagram_uc.png" alt="caso_uso">

# Descrição dos Casos de Uso

## UC1 - Cadastrar Cliente

| **Código do Caso de Uso** | UC1 - Cadastrar Cliente |
|---|---|
| **Ator Principal** | Atendente |
| **Resumo** | Permite que o atendente registre novos clientes no sistema. |
| **Pré-condições** | O atendente deve estar autenticado no sistema. |
| **Pós-condições** | O cliente é cadastrado e os dados são armazenados no banco de dados. |

### Fluxo Principal

| **Atendente** | **Sistema** |
|---|---|
| 1. O atendente insere os dados do cliente (nome completo, CPF, CEP, telefone). |  |
|  | 2. Valida os dados inseridos. |
|  | 3. Armazena os dados no banco de dados. |
|  | 4. Confirma o cadastro e exibe uma mensagem de sucesso. |

### Fluxo Alternativo

| **Atendente** | **Sistema** |
|---|---|
| 1a. O atendente insere um CPF já cadastrado. |  |
|  | 2a. O sistema exibe uma mensagem de erro e solicita um novo CPF. |
| 1b. O atendente não preenche um campo obrigatório. |  |
|  | 2b. O sistema exibe um alerta informando que o campo é obrigatório. |

---

## UC2 - Cadastrar Produto

| **Código do Caso de Uso** | UC2 - Cadastrar Produto |
|---|---|
| **Ator Principal** | Administrador |
| **Resumo** | Permite que o administrador registre novos produtos (medicamentos) no sistema. |
| **Pré-condições** | O administrador deve estar autenticado no sistema. |
| **Pós-condições** | O produto é cadastrado e os dados são armazenados no banco de dados. |

### Fluxo Principal

| **Administrador** | **Sistema** |
|---|---|
| 1. O administrador insere os dados do produto (nome, lote, data de validade, quantidade em estoque, fabricante, preço de venda). |  |
|  | 2. Valida os dados inseridos. |
|  | 3. Armazena os dados no banco de dados. |
|  | 4. Confirma o cadastro e exibe uma mensagem de sucesso. |

### Fluxo Alternativo

| **Administrador** | **Sistema** |
|---|---|
| 1a. O administrador insere um lote já cadastrado. |  |
|  | 2a. O sistema exibe uma mensagem de erro e solicita um novo lote. |

---

## UC3 - Realizar Venda

| **Código do Caso de Uso** | UC3 - Realizar Venda |
|---|---|
| **Ator Principal** | Atendente |
| **Resumo** | Permite que o atendente registre uma venda de produtos para um cliente. |
| **Pré-condições** | O cliente deve estar cadastrado no sistema e o atendente autenticado. |
| **Pós-condições** | A venda é registrada e o histórico de compras do cliente é atualizado. |

### Fluxo Principal

| **Atendente** | **Sistema** |
|---|---|
| 1. O atendente seleciona o cliente (cadastrado ou novo). |  |
|  | 2. Adiciona os produtos ao carrinho de compras. |
| 3. O atendente seleciona os produtos e suas quantidades. |  |
|  | 4. Calcula o total da venda. |

### Fluxo Alternativo

| **Atendente** | **Sistema** |
|---|---|
| 1a. O atendente tenta registrar uma venda sem cliente selecionado. |  |
|  | 2a. O sistema exibe um alerta solicitando a seleção de um cliente. |
| 1b. O atendente seleciona um produto sem estoque suficiente. |  |
|  | 2b. O sistema exibe uma mensagem de erro e impede a adição ao carrinho. |

---

## UC4 - Calcular Descontos

| **Código do Caso de Uso** | UC4 - Calcular Descontos |
|---|---|
| **Ator Principal** | Atendente |
| **Resumo** | Permite que o sistema calcule e aplique descontos durante a venda. |
| **Pré-condições** | A venda deve estar registrada, com produtos selecionados. |
| **Pós-condições** | O valor total da venda é atualizado com o desconto aplicado. |

### Fluxo Principal

| **Atendente** | **Sistema** |
|---|---|
| 1. O atendente verifica se existem descontos aplicáveis. |  |
|  | 2. Verifica se há descontos aplicáveis (promoções, quantidade, validade próxima). |
|  | 3. Calcula o valor do desconto. |
|  | 4. Aplica o desconto ao total da venda. |

### Fluxo Alternativo

| **Atendente** | **Sistema** |
|---|---|
| 1a. Não há descontos aplicáveis. |  |
|  | 2a. O sistema mantém o valor total da compra sem alterações. |

---

## UC5 - Registrar Pagamento

| **Código do Caso de Uso** | UC5 - Registrar Pagamento |
|---|---|
| **Ator Principal** | Atendente |
| **Resumo** | Permite que o atendente registre o pagamento da venda. |
| **Pré-condições** | A venda deve estar registrada e o total calculado. |
| **Pós-condições** | O pagamento é registrado e um recibo é gerado. |

### Fluxo Principal

| **Atendente** | **Sistema** |
|---|---|
| 1. O atendente seleciona o método de pagamento (crédito, débito). |  |
|  | 2. Processa o pagamento. |
| 3. O atendente insere os dados do pagamento. |  |
|  | 4. Gera um recibo de pagamento. |

### Fluxo Alternativo

| **Atendente** | **Sistema** |
|---|---|
| 1a. O pagamento não é aprovado pelo sistema de pagamento. |  |
|  | 2a. O sistema exibe uma mensagem de erro e solicita uma nova tentativa. |

---

## UC6 - Atualizar Estoque

| **Código do Caso de Uso** | UC6 - Atualizar Estoque |
|---|---|
| **Ator Principal** | Atendente, Administrador |
| **Resumo** | Permite que o sistema atualize o estoque com base nas vendas realizadas. |
| **Pré-condições** | A venda deve ser concluída e o pagamento registrado. |
| **Pós-condições** | O estoque é atualizado automaticamente com as quantidades vendidas. |

### Fluxo Principal

| **Atendente/Administrador** | **Sistema** |
|---|---|
| 1. O atendente ou administrador subtrai as quantidades vendidas do estoque. |  |
|  | 2. Atualiza os dados de estoque no banco de dados. |

### Fluxo Alternativo

|  | **Sistema** |
|---|---|
|  | 1a. O sistema não consegue atualizar o estoque devido a erro de conexão. |
|  | 2a. O sistema exibe um alerta informando falha na atualização. |

---

## UC7 - Controle de Produtos Próximos da Validade

| **Código do Caso de Uso** | UC7 - Controle de Produtos Próximos da Validade |
|---|---|
| **Ator Principal** | Administrador |
| **Resumo** | Permite que o sistema verifique a validade dos produtos e gere alertas. |
| **Pré-condições** | O administrador deve estar autenticado no sistema. |
| **Pós-condições** | O sistema gera alertas para os produtos próximos da validade. |

### Fluxo Principal

| **Administrador** | **Sistema** |
|---|---|
| 1. O administrador verifica a validade dos produtos. |  |
|  | 2. Verifica periodicamente a validade dos produtos. |
|  | 3. Gera alertas para os produtos próximos da validade. |

### Fluxo Alternativo

|  | **Sistema** |
|---|---|
| 1a. Não há produtos próximos do vencimento. |  |
|  | 2a. O sistema não gera alertas. |

---

## UC8 - Histórico de Compras

| **Código do Caso de Uso** | UC8 - Histórico de Compras |
|---|---|
| **Ator Principal** | Atendente |
| **Resumo** | Permite que o sistema gere o histórico de compras dos clientes. |
| **Pré-condições** | O cliente deve estar cadastrado no sistema e a venda registrada. |
| **Pós-condições** | O histórico de compras do cliente é atualizado automaticamente. |

### Fluxo Principal

| **Atendente** | **Sistema** |
|---|---|
| 1. O atendente registra as compras realizadas no histórico do cliente. |  |
|  | 2. Atualiza o histórico de compras do cliente. |

### Fluxo Alternativo

| **Atendente** | **Sistema** |
|---|---|
| 1a. O atendente tenta acessar o histórico de um cliente sem compras registradas. |  |
|  | 2a. O sistema exibe uma mensagem informando que não há histórico disponível. |

---

## UC9 - Gerar Relatórios de Vendas

| **Código do Caso de Uso** | UC9 - Gerar Relatórios de Vendas |
|---|---|
| **Ator Principal** | Administrador |
| **Resumo** | Permite que o sistema gere relatórios de vendas. |
| **Pré-condições** | O administrador deve estar autenticado no sistema. |
| **Pós-condições** | O relatório de vendas é gerado e exibido para o administrador. |

### Fluxo Principal

| **Administrador** | **Sistema** |
|---|---|
| 1. O administrador seleciona o período do relatório (diário, semanal, mensal). |  |
|  | 2. Gera o relatório com informações sobre produtos mais vendidos e clientes mais frequentes. |
|  | 3. Exibe o relatório. |

### Fluxo Alternativo

| **Administrador** | **Sistema** |
|---|---|
| 1a. O administrador seleciona um período sem vendas. |  |
|  | 2a. O sistema exibe um relatório vazio e informa que não há dados disponíveis. |

---

## UC10 - Controle de Acesso por Perfil de Usuário

| **Código do Caso de Uso** | UC10 - Controle de Acesso por Perfil de Usuário |
|---|---|
| **Ator Principal** | Administrador |
| **Resumo** | Permite que o administrador gerencie o acesso dos usuários ao sistema. |
| **Pré-condições** | O administrador deve estar autenticado no sistema. |
| **Pós-condições** | O sistema ajusta o acesso dos usuários conforme as permissões definidas. |

### Fluxo Principal

| **Administrador** | **Sistema** |
|---|---|
| 1. O administrador cadastra, edita ou exclui usuários. |  |
| 2. O administrador define os perfis de acesso dos usuários. | |
|  | 3. Ajusta o acesso dos usuários conforme as permissões definidas. |

### Fluxo Alternativo

| **Administrador** | **Sistema** |
|---|---|
| 1a. O administrador tenta excluir um usuário em uso. |  |
|  | 2a. O sistema impede a exclusão e exibe um alerta. |

# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

*&lt;Diagrama para permite modelar o comportamento interno de um determinado objeto, subsistema ou sistema global&gt;*

# Diagrama de Implantação

*&lt;Diagrama para exibir o relacionamento de hardware e software no projeto&gt;*

# Referências

*&lt;Lista de referências&gt;*
