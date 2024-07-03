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

* **Dado que** o administrador acessa a funcionalidade de cadastro de medicamentos,
* **Quando ele** preenche todos os campos obrigatórios e clica em "Salvar",
* **Então** o sistema deve registrar o novo medicamento e exibir uma mensagem de sucesso.

## Cenário 2: Busca de um medicamento pelo nome

* **Dado que** o administrador acessa a funcionalidade de busca de medicamentos,
* **Quando ele** insere o nome do medicamento e clica em "Buscar",
* **Então** o sistema deve exibir uma lista de medicamentos que correspondem ao nome informado.

## Cenário 3: Tentativa de cadastro de um medicamento já existente

* **Dado que** o administrador tenta cadastrar um medicamento que já existe no sistema,
* **Quando ele** preenche os campos e clica em "Salvar",
* **Então** o sistema deve exibir uma mensagem de alerta informando que o medicamento já está cadastrado.

## Cenário 4: Edição de um medicamento

* **Dado que** o administrador acessa a funcionalidade de edição de um medicamento,
* **Quando ele** altera os campos desejados e clica em "Salvar",
* **Então** o sistema deve atualizar as informações do medicamento e exibir uma mensagem de sucesso.

## Cenário 5: Exclusão de um medicamento

* **Dado que** o administrador acessa a funcionalidade de exclusão de um medicamento,
* **Quando ele** confirma que seu intenção é excluir clica em "Sim",
* **Então** o sistema deve excluir o medicamento e exibir uma mensagem de sucesso.

# Protótipo
## Protótipo da Tela de Cadastro de Medicamentos  (link-para-o-prototipo)
https://www.figma.com/proto/K8pXcHK4UHx8zHyjEkXz0M/HAILLYN-Manuten%C3%A7%C3%A3o-Busca-de-medicamentos?node-id=0-1&t=yy6a0CRrQ9RLgfKc-0&scaling=scale-down&content-scaling=fixed&starting-point-node-id=224%3A327&show-proto-sidebar=1

https://www.figma.com/proto/K8pXcHK4UHx8zHyjEkXz0M/HAILLYN-Manuten%C3%A7%C3%A3o-Busca-de-medicamentos?node-id=0-1&t=yy6a0CRrQ9RLgfKc-0&scaling=scale-down&content-scaling=fixed&starting-point-node-id=241%3A1191&show-proto-sidebar=1

https://www.figma.com/proto/K8pXcHK4UHx8zHyjEkXz0M/HAILLYN-Manuten%C3%A7%C3%A3o-Busca-de-medicamentos?node-id=0-1&t=yy6a0CRrQ9RLgfKc-0&scaling=scale-down&content-scaling=fixed&starting-point-node-id=253%3A1138&show-proto-sidebar=1

https://www.figma.com/proto/K8pXcHK4UHx8zHyjEkXz0M/HAILLYN-Manuten%C3%A7%C3%A3o-Busca-de-medicamentos?node-id=0-1&t=yy6a0CRrQ9RLgfKc-0&scaling=scale-down&content-scaling=fixed&starting-point-node-id=256%3A2284&show-proto-sidebar=1

https://www.figma.com/proto/K8pXcHK4UHx8zHyjEkXz0M/HAILLYN-Manuten%C3%A7%C3%A3o-Busca-de-medicamentos?node-id=0-1&t=yy6a0CRrQ9RLgfKc-0&scaling=scale-down&content-scaling=fixed&starting-point-node-id=258%3A5549&show-proto-sidebar=1


# Descrição dos Campos
## Detalhamento dos Campos:

   Nome do Medicamento
   Tipo: Texto
   Tamanho: 100 caracteres
   Máscara: Não aplicável
   Hint: "Informe o nome comercial do medicamento"
   
   Princípios Ativos
   Tipo: Multi-seleção
   Tamanho: -
   Máscara: Não aplicável
   Hint: "Selecione os princípios ativos do medicamento"
      Campos internos:
         Princípio Ativo
         Tipo: Seleção a partir de um cadastro pré-existente
         Tamanho: -
         Máscara: Não aplicável
         Hint: "Selecione o princípio ativo"
         Concentração
         Tipo: Numérico
         Tamanho: 10 caracteres
         Máscara: 99.99
         Hint: "Informe a concentração do princípio ativo"
         Unidade de Medida
         Tipo: Seleção
         Tamanho: -
         Máscara: Não aplicável
         Hint: "Selecione a unidade de medida"
      
   Forma de Apresentação
   Tipo: Seleção
   Tamanho: -
   Máscara: Não aplicável
   Hint: "Selecione a forma de apresentação"
   
   Via de Administração
   Tipo: Seleção
   Tamanho: -
   Máscara: Não aplicável
   Hint: "Selecione a via de administração"
   
   Medicamento Controlado
   Tipo: Checkbox
   Tamanho: -
   Máscara: Não aplicável
   Hint: "Marque se o medicamento é controlado"
   
   Nomes Similares
   Tipo: Texto
   Tamanho: 255 caracteres
   Máscara: Não aplicável
   Hint: "Informe nomes similares do medicamento"

# Implementação da Funcionalidade
## Funcionalidade de Cadastro e Manutenção de Medicamentos

* **Manter Medicamentos:** Permite ao administrador cadastrar, editar e excluir medicamentos.
* **Buscar Medicamentos:** Permite ao administrador buscar medicamentos por diferentes critérios.
* **Garantir Padronização:** Valida os nomes dos princípios ativos conforme a Denominação Comum Brasileira (DCB).
* **Prevenir Duplicidade:** Alerta o usuário em caso de tentativa de cadastro de um medicamento já existente.

Com essas especificações, o cliente poderá realizar a manutenção de medicamentos de forma estruturada, garantindo a padronização das informações e facilitando a gestão dos medicamentos nos hospitais.

