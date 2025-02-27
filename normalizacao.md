# Normalização de Dados e Anomalias em Bancos de Dados

A modelagem de dados é essencial para representar com precisão a estrutura e as relações de um sistema. No entanto, anomalias podem surgir, comprometendo a integridade dos dados. Para evitar esses problemas, utiliza-se o processo de normalização, que organiza os dados de forma eficiente e sem redundâncias.

## Dependência Funcional

A dependência funcional é um relacionamento entre dois atributos, ou conjuntos de atributos, dentro de uma tabela de banco de dados. Quando um atributo, chamado de determinante, tem a propriedade de determinar unicamente outro atributo, diz-se que há uma dependência funcional.

Por exemplo, em uma tabela de colaboradores, se cada colaborador é identificado por um número único de identificação (ID do colaborador), então o ID do colaborador pode determinar unicamente outros atributos como nome do colaborador, endereço, telefone e departamento. Aqui, o ID do colaborador é o determinante, e os atributos nome, endereço, telefone e departamento são dependentes deste ID.

## Tipos de Anomalias
1. **Anomalias de Inserção**: Dificuldade em inserir novos dados devido a restrições ou inconsistências.
2. **Anomalias de Atualização**: Inconsistências ao atualizar dados em uma tabela.
3. **Anomalias de Exclusão**: Perda de informações importantes ao excluir registros.
4. **Redundância de Dados**: Armazenamento duplicado, aumentando o espaço e dificultando a manutenção.
5. **Dependências Funcionais Indesejadas**: Relações mal definidas entre dados.
6. **Inconsistências de Dados**: Dados desatualizados ou conflitantes.
7. **Dependências Multivaloradas**: Um atributo determina vários valores de outro atributo.
8. **Anomalias de Junção**: Informações incorretas ao juntar tabelas mal estruturadas.

## Normalização de Dados
A normalização organiza as tabelas do banco de dados para evitar redundâncias e anomalias. Isso é feito por meio das formas normais:

### Primeira Forma Normal (1NF)

A Primeira Forma Normal é o primeiro nível de normalização e um passo fundamental para qualquer esquema de banco de dados. Uma tabela está na 1FN se todos os seus atributos forem atômicos, ou seja, indivisíveis em partes menores dentro do contexto do banco de dados.

- Cada célula deve conter um único valor atômico.
- Exemplo: Separar listas de disciplinas cursadas em uma tabela própria.

### Segunda Forma Normal (2NF)
- A tabela deve estar na 1NF e todos os atributos não chave devem depender completamente da chave primária.
- Exemplo: Criar uma tabela separada para registrar notas de alunos.

### Terceira Forma Normal (3NF)
- A tabela deve estar na 2NF e todos os atributos não chave devem depender apenas da chave primária.
- Exemplo: Separar informações de professores das disciplinas.

### Quarta Forma Normal (4NF)
- Elimina dependências multivaloradas.
- Exemplo: Criar uma tabela separada para representar produtos de interesse de clientes.

### Quinta Forma Normal (5NF)
- Elimina anomalias de junção.
- Exemplo: Separar cursos e professores para evitar erros na junção de tabelas.

### Forma Normal de Boyce-Codd (BCNF)
- Mais rigorosa que a 3NF, elimina dependências funcionais não triviais.

## Resumo
A normalização de dados é um processo sistemático utilizado na modelagem de bancos de dados para reduzir redundâncias e melhorar a integridade, organizando os dados em tabelas de acordo com regras chamadas formas normais.

As diretrizes informais são critérios práticos para avaliar a qualidade das tabelas, visando assegurar esquemas claros e fáceis de entender, minimizar informações redundantes, reduzir valores NULL e evitar inconsistências.

Dependências no contexto dos bancos de dados, referem-se às relações onde um ou mais atributos determinam outros atributos dentro de uma tabela, influenciando como os dados são organizados para manter a integridade e reduzir redundâncias.

Formas normais são padrões que garantem níveis crescentes de rigor na organização de dados. Cada forma normal, da Primeira à Quinta, aborda tipos específicos de redundância e dependência, ajudando a estruturar o banco de dados de forma lógica e eficiente para facilitar operações e manutenção.
