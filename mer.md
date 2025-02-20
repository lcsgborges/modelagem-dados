## O que é MER:
O MER (Modelo Entidade Relacionamento) é utilizado para descrever os objetos do mundo real através de entidades, com suas propriedades que são os atributos e os seus relacionamentos.

### Entidades:
As entidades representam um objeto do mundo real e que possuem uma existência independente, como: pessoas, empresa, carro, casa, entre outras coisas que podem ser representadas por uma entidade. Podemos considerar que existem três tipos de entidades:

- **Entidades Fortes**: Não dependem de outras entidades para existirem.
- **Entidades Fracas**: Dependem de outras entidades para existir, ou seja, elas não possuem existência própria ou não possuem atributos próprios para identificação, dependendo assim, dos atributos chave das entidades fortes.
- **Entidades Associativas**: São utilizadas quando existe a necessidade de associar uma entidade a um relacionamento.

### Atributos:
Os atributos descrevem as propriedades das entidades. A entidade pessoa pode ter como atributo o nome, data de nascimento, idade, endereço. Como as entidades, também existem alguns tipos de atributos, que são:

- **Atributo Simples**: Indivisíveis, ou seja, são atributos atômicos. Exemplo: CPF.
- **Atributo Composto**: Podem ser divididos em partes menores, como o atributo endereço, que pode ser subdividido em cidade, estado, rua, CEP.
- **Atributo Multivalorado**: Pode ter um ou vários valores associados, como telefones de um cliente.
- **Atributo Derivado**: Dependem de outro atributo ou outra entidade para existir. Exemplo: a idade é derivada da data de nascimento.
- **Atributo Chave**: Identifica de forma única uma entidade. Exemplo: CPF.

### Relacionamentos:
As entidades podem se relacionar entre si, havendo assim uma associação, que conhecemos como relacionamento, que normalmente são representados por verbos. Como, por exemplo, “uma pessoa trabalha para uma empresa”.

Os relacionamentos podem ser classificados em três tipos:

- **Relacionamento UM PARA UM (1:1)**: Onde uma entidade X se associa unicamente a uma ocorrência da entidade Y.
- **Relacionamento UM PARA MUITOS (1:N)**: Onde uma entidade X se associa a várias ocorrências da entidade Y, porém, a entidade Y pode apenas se associar a uma ocorrência da entidade X.
- **Relacionamento MUITOS PARA MUITOS (N:N)**: Onde a entidade X pode se associar a várias ocorrências da entidade Y e a entidade Y pode também se associar a várias ocorrências da entidade X.
