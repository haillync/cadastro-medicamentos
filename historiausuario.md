Cadastro de medicamentos
**Como** administrador do sistema de gestão hospitalar,
**Quero** realizar o cadastro estruturado de medicamentos,
**Para que** eu possa garantir a padronização das informações e evitar inconsistências nos registros de medicamentos e princípios ativos.


**Critérios de Aceitação**
1. O sistema deve permitir o cadastro de medicamentos com os seguintes campos obrigatórios:

    Nome do medicamento
    Combinação de princípios ativos (seleção a partir de um cadastro pré-existente)
    Concentração de cada princípio ativo
    Unidade de medida de cada princípio ativo
    Forma de apresentação
    Via de administração
    Indicação se é um medicamento controlado
    Nomes similares do medicamento

2. O sistema deve permitir a busca de medicamentos utilizando pelo menos os seguintes critérios:

    Nome do medicamento
    Princípio ativo
    Forma de apresentação
    Via de administração
   
3. O sistema deve garantir que a denominação dos princípios ativos seja padronizada conforme a Denominação Comum Brasileira (DCB).

4. O sistema deve alertar o usuário em caso de tentativa de cadastro de um medicamento já existente.

5. O sistema deve permitir a edição e exclusão de medicamentos já cadastrados.

**Cenários**
  **Cenário 1: Cadastro de um novo medicamento**
