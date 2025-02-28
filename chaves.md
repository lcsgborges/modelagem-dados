## Chave Primária e Chave Estrangeira

### Chave Primária (Primary Key)
A **chave primária** é um atributo ou um conjunto de atributos que identifica de forma única cada registro dentro de uma tabela em um banco de dados. Sua principal função é garantir a integridade e a unicidade dos dados armazenados.

#### Características da Chave Primária:
- Deve possuir um valor único para cada registro.
- Não pode conter valores nulos (NULL).
- É utilizada para indexação e otimização de buscas no banco de dados.

#### Exemplo:
```sql
CREATE TABLE Cliente (
    id_cliente INT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100) UNIQUE
);
```
Neste caso, `id_cliente` é a chave primária, garantindo que cada cliente tenha um identificador único.

---

### Chave Estrangeira (Foreign Key)
A **chave estrangeira** é um atributo que estabelece um vínculo entre duas tabelas, referenciando a chave primária de outra tabela. Isso permite garantir a integridade referencial dos dados.

#### Características da Chave Estrangeira:
- Mantém a consistência dos dados entre tabelas relacionadas.
- Pode conter valores repetidos, desde que respeite as regras de relacionamento.
- Deve referenciar uma chave primária existente na tabela relacionada.
- Pode ser usada para criar relações do tipo **um para muitos (1:N)** e **muitos para muitos (N:N)**.

#### Exemplo:
```sql
CREATE TABLE Pedido (
    id_pedido INT PRIMARY KEY,
    id_cliente INT,
    data_pedido DATE,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id_cliente)
);
```
Neste exemplo, `id_cliente` em `Pedido` é uma chave estrangeira que referencia `id_cliente` na tabela `Cliente`, garantindo que um pedido sempre esteja associado a um cliente válido.

---

### Diferença entre Chave Primária e Chave Estrangeira
| Característica | Chave Primária | Chave Estrangeira |
|---------------|--------------|----------------|
| Função | Identifica unicamente um registro na tabela | Relaciona duas tabelas |
| Valores | Sempre únicos e não nulos | Pode ter valores repetidos e nulos (dependendo da relação) |
| Uso | Garantia de unicidade | Garantia de integridade referencial |
| Referência | Pertence à própria tabela | Referencia uma chave primária de outra tabela |

O uso adequado de chaves primárias e estrangeiras é essencial para projetar bancos de dados bem estruturados e garantir a integridade e confiabilidade dos dados.

### Chave Candidata
Qualquer coluna ou conjunto de colunas que possam qualificar como chave primária.

### Chave Alternativa
Uma chave candidata não escolhida como chave primária.

### Chave Composta
Uma chave primária ou chave estrangeira formada por dois ou mais campos, usada quando um único campo não é suficiente para garantir a unicidade ou estabelecer o relacionamento necessário.

## Índices

Índices são estruturas auxiliares que aceleram operações de busca, inserção, atualização e exclusão de registros em um banco de dados. Eles atuam como atalhos para recuperar dados mais rapidamente.

### Tipos de Índices

- **Índice Primário**: Criado automaticamente na chave primária de uma tabela, otimizando buscas por essa chave.
- **Índice Secundário**: Criado em colunas que não são parte da chave primária, útil para buscas em outros campos.
- **Índice Único**: Garante que os valores de uma coluna (ou combinação de colunas) sejam únicos.
- **Índice Composto**: Inclui múltiplas colunas, ideal para consultas com múltiplos filtros.
- **Índice Completo de Texto**: Otimiza buscas em campos de texto, como nomes e descrições.

### Diferenças Fundamentais

- **Propósito**: Chaves garantem integridade e relações entre tabelas, enquanto índices melhoram a performance das consultas.
- **Impacto na Escrita de Dados**: Chaves, especialmente estrangeiras, garantem integridade referencial sem afetar diretamente a velocidade de escrita. Já os índices podem desacelerar a escrita, pois precisam ser atualizados com cada modificação nos dados.

### Implementação no Modelo Físico

Os índices são definidos no modelo físico junto com as tabelas. A escolha das colunas a serem indexadas deve considerar a necessidade das consultas e o desempenho do banco de dados. A implementação é feita com comandos SQL, e sua eficiência deve ser monitorada para evitar impactos negativos na escrita dos dados.

Um bom entendimento de chaves e índices permite projetar bancos de dados eficientes, garantindo integridade e alto desempenho nas consultas.
