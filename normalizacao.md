# Normalização de Dados e Anomalias em Bancos de Dados

A modelagem de dados é essencial para representar com precisão a estrutura e as relações de um sistema. No entanto, anomalias podem surgir, comprometendo a integridade dos dados. Para evitar esses problemas, utiliza-se o processo de normalização, que organiza os dados de forma eficiente e sem redundâncias.

## Tipos de Anomalias
1. **Anomalias de Inserção**: Dificuldade em inserir novos dados devido a restrições ou inconsistências.
2. **Anomalias de Atualização**: Inconsistências ao atualizar dados em uma tabela.
3. **Anomalias de Exclusão**: Perda de informações importantes ao excluir registros.

## Normalização de Dados
A normalização organiza as tabelas do banco de dados para evitar redundâncias e anomalias. Isso é feito por meio das formas normais:

### Primeira Forma Normal (1NF)

A Primeira Forma Normal é o primeiro nível de normalização e um passo fundamental para qualquer esquema de banco de dados. Uma tabela está na 1FN se todos os seus atributos forem atômicos, ou seja, indivisíveis em partes menores dentro do contexto do banco de dados.

- Cada célula deve conter um único valor atômico.
- Exemplo: Separar listas de disciplinas cursadas em uma tabela própria.

### Segunda Forma Normal (2NF)

Uma tabela está na Segunda Forma Normal se, e somente se, ela estiver na Primeira Forma Normal (1FN) e todos os seus atributos não chave forem totalmente dependentes da chave primária inteira, ou seja, não deve haver dependências parciais.

- A tabela deve estar na 1NF e todos os atributos não chave devem depender completamente da chave primária.
- Exemplo: Criar uma tabela separada para registrar notas de alunos.

### Terceira Forma Normal (3NF)

Uma tabela está na Terceira Forma Normal se ela já está na Segunda Forma Normal e todos os seus atributos não chave são dependentes apenas das chaves primárias, não de outros atributos não chave. Em outras palavras, a 3FN é alcançada eliminando dependências transitivas.

- A tabela deve estar na 2NF e todos os atributos não chave devem depender apenas da chave primária.
- Exemplo: Separar informações de professores das disciplinas.

### Quarta Forma Normal (4NF)

A 4FN é aplicada para resolver situações onde a associação independente de dois atributos a um terceiro pode levar a redundâncias desnecessárias. A aplicação da 4FN garante que as relações multivaloradas sejam divididas em tabelas separadas para evitar essas redundâncias.

- Elimina dependências multivaloradas.
- Exemplo: Criar uma tabela separada para representar produtos de interesse de clientes.

### Quinta Forma Normal (5NF)

Lida com casos onde as tabelas envolvem várias dependências de junção. Uma tabela está na 5FN se e somente se ela não puder ser decomposta em outras tabelas sem perder informações ou gerar redundâncias. Isso ocorre tipicamente em estruturas de dados complexas com múltiplas entidades inter-relacionadas, garantindo que o banco de dados esteja livre de todas as redundâncias possíveis decorrentes das relações de junção.

- Elimina anomalias de junção.
- Exemplo: Separar cursos e professores para evitar erros na junção de tabelas.

### Forma Normal de Boyce-Codd (BCNF)

A FNBC é uma extensão da Terceira Forma Normal que exige que todos os determinantes em uma tabela sejam chaves candidatas. Isso significa que qualquer atributo que determine outro deve ser uma chave única por si só, eliminando assim anomalias e redundâncias mais sutis que a 3FN pode deixar passar.

A FNBC é particularmente útil em esquemas onde existem várias chaves candidatas e garante que todas as dependências funcionais sejam entre superchaves.

- Mais rigorosa que a 3NF, elimina dependências funcionais não triviais.

## Resumo
A normalização de dados é um processo sistemático utilizado na modelagem de bancos de dados para reduzir redundâncias e melhorar a integridade, organizando os dados em tabelas de acordo com regras chamadas formas normais.

As diretrizes informais são critérios práticos para avaliar a qualidade das tabelas, visando assegurar esquemas claros e fáceis de entender, minimizar informações redundantes, reduzir valores NULL e evitar inconsistências.

Dependências no contexto dos bancos de dados, referem-se às relações onde um ou mais atributos determinam outros atributos dentro de uma tabela, influenciando como os dados são organizados para manter a integridade e reduzir redundâncias.

Formas normais são padrões que garantem níveis crescentes de rigor na organização de dados. Cada forma normal, da Primeira à Quinta, aborda tipos específicos de redundância e dependência, ajudando a estruturar o banco de dados de forma lógica e eficiente para facilitar operações e manutenção.
