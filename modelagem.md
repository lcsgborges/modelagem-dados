## O que é e para que serve a Modelagem de Dados:

A modelagem de dados envolve a criação de modelos conceituais, lógicos e físicos que descrevem como os dados estão relacionados entre si e como são armazenados e acessados dentro de um sistema.

## Objetivos da Modelagem de Dados:

### 1. Precisão dos Dados:
A modelagem de dados busca garantir que os dados armazenados em um sistema sejam precisos e livres de erros. Isso envolve a definição clara e precisa dos tipos de dados, formatos e restrições aplicáveis a cada campo.

### 2. Integridade dos Dados:
Os dados devem ser consistentes e confiáveis em todo o sistema, sem contradições ou inconsistências que possam comprometer sua utilidade ou confiabilidade.

### 3. Consistência dos Dados:
A consistência dos dados é crucial para garantir que diferentes partes de um sistema de informação interpretem e usem os dados de maneira uniforme e coerente. A modelagem de dados estabelece padrões e convenções para garantir essa consistência em toda a organização.

## Tipos de Modelagem de Dados:

### 1. Modelagem Conceitual:
A modelagem conceitual concentra-se na representação abstrata e independente de implementação dos dados.

Neste estágio, os principais elementos são entidades, atributos e os relacionamentos entre elas.

O objetivo é capturar os requisitos e conceitos do negócio de uma forma compreensível para os usuários finais e os stakeholders.

É comumente representada por meio de diagramas como o Diagrama de Entidade-Relacionamento (DER) ou Modelagem de Objetos.

### 2. Modelagem Lógica:
A modelagem lógica traduz a modelagem conceitual em uma estrutura mais detalhada e específica, mas ainda independente de plataforma.

Nesta fase, são definidos as chaves primárias, chaves estrangeiras e outras restrições.

O objetivo é criar um modelo que seja próximo o suficiente da implementação para guiar o desenvolvimento do banco de dados, mas ainda abstrato o bastante para ser independente de tecnologia.

É comumente representada por meio de diagramas como o Modelo de Dados Relacional.

### 3. Modelagem Física:
A modelagem física é o estágio final onde o modelo é implementado em um sistema de gerenciamento de banco de dados específico.

Aqui, são definidos os tipos dos dados e detalhes como a organização física dos dados, índices, particionamento e outros aspectos de desempenho são considerados.

O objetivo é otimizar o modelo para a plataforma específica e garantir um desempenho eficiente do banco de dados.

É representada através de scripts de criação de banco de dados específicos para o sistema de gerenciamento de banco de dados escolhido.


### Conclusão:
A modelagem conceitual estabelece os requisitos do negócio, a modelagem lógica traduz esses requisitos em uma estrutura de dados compreensível e a modelagem física finaliza a implementação detalhada no ambiente de banco de dados específico.

