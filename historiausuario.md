# Cadastro de medicamentos

**Como** administrador do sistema de gestão hospitalar, 

**Quero** realizar o cadastro estruturado de medicamentos, 

**Para que** eu possa garantir a padronização das informações e evitar inconsistências nos registros de medicamentos e princípios ativos.

# Critérios de Aceitação

1. O sistema deve permitir o cadastro de medicamentos com os seguintes campos obrigatórios:

  * Nome do medicamento
  * Combinação de princípios ativos (seleção a partir de um cadastro pré-existente)
  * Concentração de cada princípio ativo
  * Unidade de medida de cada princípio ativo
  * Forma de apresentação
  * Via de administração
  * Indicação se é um medicamento controlado
  * Nomes similares do medicamento


2. O sistema deve permitir a busca de medicamentos utilizando pelo menos os seguintes critérios:

  * Nome do medicamento
  * Princípio ativo 
  * Forma de apresentação 
  * Via de administração

3. O sistema deve garantir que a denominação dos princípios ativos seja padronizada conforme a Denominação Comum Brasileira (DCB).

4. O sistema deve alertar o usuário em caso de tentativa de cadastro de um medicamento já existente.

5. O sistema deve permitir a edição e exclusão de medicamentos já cadastrados.

# Cenários 

## Cenário 1: Cadastro de um novo medicamento

*** Dado que** o administrador acessa a funcionalidade de cadastro de medicamentos,
*** Quando ele** preenche todos os campos obrigatórios e clica em "Salvar",
*** Então** o sistema deve registrar o novo medicamento e exibir uma mensagem de sucesso.

## Cenário 2: Busca de um medicamento pelo nome

* Dado que o administrador acessa a funcionalidade de busca de medicamentos,
* Quando ele insere o nome do medicamento e clica em "Buscar",
* Então o sistema deve exibir uma lista de medicamentos que correspondem ao nome informado.

## Cenário 3: Tentativa de cadastro de um medicamento já existente

* Dado que o administrador tenta cadastrar um medicamento que já existe no sistema,
* Quando ele preenche os campos e clica em "Salvar",
* Então o sistema deve exibir uma mensagem de alerta informando que o medicamento já está cadastrado.

## Cenário 4: Edição de um medicamento

* Dado que o administrador acessa a funcionalidade de edição de um medicamento,
* Quando ele altera os campos desejados e clica em "Salvar",
* Então o sistema deve atualizar as informações do medicamento e exibir uma mensagem de sucesso.

# Protótipo
## Protótipo da Tela de Cadastro de Medicamentos  (link-para-o-prototipo)

# Descrição dos Campos
(link-descrição dos campos)

# Implementação da Funcionalidade

## Funcionalidade de Cadastro e Manutenção de Medicamentos

* **Manter Medicamentos:** Permite ao administrador cadastrar, editar e excluir medicamentos.
* Buscar Medicamentos: Permite ao administrador buscar medicamentos por diferentes critérios.
* Garantir Padronização: Valida os nomes dos princípios ativos conforme a Denominação Comum Brasileira (DCB).
* Prevenir Duplicidade: Alerta o usuário em caso de tentativa de cadastro de um medicamento já existente.

Com essas especificações, o cliente poderá realizar a manutenção de medicamentos de forma estruturada, garantindo a padronização das informações e facilitando a gestão dos medicamentos nos hospitais.

