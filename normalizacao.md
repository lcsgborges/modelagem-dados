# Normalização de Dados e Anomalias em Bancos de Dados

A modelagem de dados é essencial para representar com precisão a estrutura e as relações de um sistema. No entanto, anomalias podem surgir, comprometendo a integridade dos dados. Para evitar esses problemas, utiliza-se o processo de normalização, que organiza os dados de forma eficiente e sem redundâncias.

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
