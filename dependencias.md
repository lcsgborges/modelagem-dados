# Dependências

## Dependência Funcional

A dependência funcional é um relacionamento entre dois atributos, ou conjuntos de atributos, dentro de uma tabela de banco de dados. Quando um atributo, chamado de determinante, tem a propriedade de determinar unicamente outro atributo, diz-se que há uma dependência funcional.

Por exemplo, em uma tabela de colaboradores, se cada colaborador é identificado por um número único de identificação (ID do colaborador), então o ID do colaborador pode determinar unicamente outros atributos como nome do colaborador, endereço, telefone e departamento. Aqui, o ID do colaborador é o determinante, e os atributos nome, endereço, telefone e departamento são dependentes deste ID.

## Dependência Parcial

Dependência Parcial ocorre quando um atributo em uma tabela depende apenas de parte de uma chave primária composta, e não da chave completa. Por exemplo, considere uma tabela que registra as horas trabalhadas de funcionários em diferentes projetos, onde a chave primária é composta por ID_Colaborador e ID_Projeto. Se a tabela também inclui o Nome_Colaborador, e este atributo depende apenas do ID_Colaborador (parte da chave primária), então temos uma dependência parcial. Este tipo de dependência pode levar a redundâncias, pois o nome do funcionário será repetido para cada projeto em que ele trabalha.

## Dependência Total

Dependência Total ocorre quando todos os atributos não chave em uma tabela dependem de toda a chave composta. Isso significa que para entender ou prever o valor de qualquer atributo não chave, precisamos conhecer todos os componentes da chave primária composta.

## Dependência Transitiva

A dependência transitiva ocorre quando um atributo em uma tabela depende de outro através de um terceiro atributo intermediário, formando uma cadeia de dependências.

Por exemplo, se temos uma tabela com os atributos ID_Colaborador, ID_Departamento e Localizacao_Departamento. Temos aqui que o ID_Colaborador determina ID_Departamento, que por sua vez determina Localizacao_Departamento, então Localizacao_Departamento é transitivamente dependente de ID_Colaborador através de ID_Departamento. Esta configuração pode causar problemas, pois alterações na localização de um departamento exigiriam atualizações múltiplas e poderiam levar a dados desatualizados ou inconsistentes se não forem gerenciadas corretamente.
