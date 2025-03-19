#### *Objetivo:*
Mostra a estrutura estática do sistema, com suas classes, atributos, métodos e os relacionamentos entre elas. Esse diagrama é essencial para entender a arquitetura do sistema.

#### *Elementos:*
- *Classe*: Representa um objeto ou entidade do sistema. É mostrada como um retângulo dividido em três partes: nome da classe, atributos e métodos.
- *Atributos*: Variáveis ou propriedades da classe.
- *Métodos*: Funções ou comportamentos da classe.
- *Relacionamentos entre classes*:
  - *Associação*: Linha simples entre classes, indicando que elas têm uma relação. Pode ser de multiplicidade (1:1, 1:N, etc.).
  - *Herança (Generalização)*: Linha com triângulo apontando para a classe base (superclasse), indicando que uma classe herda características de outra.
  - *Agregação*: Linha com um losango vazio na extremidade, indicando que uma classe é composta por outras, mas as partes podem existir independentemente da classe.
  - *Composição*: Linha com losango sólido, indicando uma relação de "parte-todo" forte, onde a parte não pode existir sem o todo.
  - *Dependência*: Linha pontilhada com seta, indicando que uma classe depende de outra para funcionar.
  - *Realização*: Linha com um triângulo (como herança) e usada para mostrar que uma classe implementa uma interface.
