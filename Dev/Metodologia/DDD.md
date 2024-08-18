> _The heart of software is its ability to solve domain-related problems for its user._ – Eric Evans

## Introdução

Domain-Driven Design (DDD) é um conjunto de princípios para projeto de software.

Os princípios defendidos por DDD têm, no seu conjunto, um objetivo central: permitir o desenvolvimento de sistemas cujo design é centrado em conceitos próximos e alinhados com um domínio de negócio.

O **domínio** de um sistema consiste da área e problema de negócio que ele pretende resolver. Para explicar DDD, vamos usar como exemplo um sistema para gerenciar uma biblioteca. Logo, esse problema, gerenciamento de bibliotecas, constitui o domínio do nosso sistema de exemplo.

DDD defende que os **desenvolvedores** devem ter um profundo conhecimento do domínio do sistema que eles desenvolvem. Esse conhecimento deve ser obtido por meio de conversas e discussões frequentes com **especialistas no domínio**. Portanto, o design do sistema deve ser norteado para atender ao seu domínio. E não, por exemplo, para se moldar a uma determinada tecnologia de programação. Portanto, o design é dirigido pelo domínio, e não por frameworks, arquiteturas, linguagens de programação, etc.

DDD defende que a separação entre domínio e tecnologia deve ser promovida e expressa na arquitetura do sistema. Para tanto, padrões como Arquitetura em Camadas, Arquitetura Limpa ou Arquitetura Hexagonal podem ser usados.

## Linguagem Ubíqua

**Linguagem Ubíqua** (ou **Linguagem Onipresente**) é um conceito central de DDD. Ela consiste de um conjunto de termos que devem ser plenamente entendidos tanto por especialistas no domínio (usuários do sistema) como por desenvolvedores (implementadores do sistema).

Para um projeto de software dar certo, DDD defende que esses dois papéis – especialistas no domínio e desenvolvedores – devem falar a mesma língua, que vai constituir a chamada Linguagem Ubíqua do sistema. 

![A linguagem ubíqua representa o conhecimento compartilhado entre especialistas do negócio e desenvolvedores.](https://engsoftmoderna.info/artigos/figs/linguagem-onipresente.svg)

A linguagem ubíqua representa o conhecimento compartilhado entre especialistas do negócio e desenvolvedores.

A figura deixa claro que existem termos que só os especialistas de domínio conhecem. Já outros termos, de cunho tecnológico, são do conhecimento apenas dos desenvolvedores. Porém, existe um conjunto de termos que devem ser do conhecimento de ambos, os quais formam a Linguagem Ubíqua do sistema.

Os termos da Linguagem Ubíqua são usados com dois propósitos:

- Para possibilitar uma comunicação fluida entre desenvolvedores e especialistas no domínio.
- Para nomear entidades do código do sistema, como classes, métodos, atributos, pacotes, módulos, tabelas de bancos de dados, rotas de APIs, etc.

Além de clarificar o significado dos termos da linguagem ubíqua, é importante que se definam os **relacionamentos** e **associações** que existem entre eles.

**Exemplo**: no nosso sistema de bibliotecas, a Linguagem Ubíqua inclui termos como os seguintes:

> Livro, Exemplar, ISBN, Bibliotecária, Usuário, Acervo, Reserva, Empréstimo, Multa, Catálogo

Por outro lado, alguns termos são de domínio apenas dos desenvolvedores, tais como proxy, observadores, cache, camadas, rotas, dentre outros. Existem ainda termos que são do conhecimento apenas de bibliotecárias, como certos formatos para definição de ISBNs, que não são usados no Brasil.

Devemos definir também os relacionamentos e associações entre esses termos, como exemplificado a seguir:

- Um `Livro` pode ter um ou mais `Exemplares`.
- Uma `Reserva` pode ser feita para no máximo três `Livros`.
- Existem três tipos de `Usuário`: `Aluno`, `Professor` e `UsuárioExterno`.
- O `Acervo` da biblioteca é formado por um conjunto de `Livros`.

Para documentar esses relacionamentos pode ser usado um [[Diagrama de Classe]] de UML. No entanto, esse diagrama pode ser simples e leve. Ele não precisa, por exemplo, incluir todos os atributos e métodos de cada classe.

## Objetos de Domínio

DDD foi proposto pensando em sistemas implementados em linguagens com [[Orientada a Objetos]]. Então, quando se define o design desses sistemas, alguns tipos importantes de objetos se destacam. Dentre eles, DDD lista os seguintes:
- Entidades
- Objetos de Valor
- Serviços
- Agregados
- Repositórios

Esses tipos de objetos de domínio devem ser entendidos como as ferramentas conceituais que um projetista deve lançar mão para projetar com sucesso um determinado sistema. Por isso, eles são chamados também dos **building blocks** de DDD. Iremos comentar sobre cada um deles a seguir.

### Entidades e Objetos de Valor

Uma **entidade** é um objeto que possui uma identidade única, que o distingue dos demais objetos da mesma classe. Por exemplo, cada `Usuário` da nossa biblioteca é uma entidade, cujo identificador é o seu número de matrícula na universidade.

Por outro lado, **objetos de valor** (_value objects_) não possuem um identificador único. Assim, eles são caracterizados apenas por seu estado, isto é, pelos valores de seus atributos. Por exemplo, o `Endereço` de um `Usuário` da biblioteca é um objeto de valor. Veja que se dois `Endereços` tiverem exatamente os mesmos valores para `rua`, `número`, `cidade`, `CEP`, etc, eles serão idênticos.

Outros exemplos de objetos de valor incluem: `Moeda`, `Data`, `Fone`, `Email`, `Hora`, `Cor`, etc.

**Por que distinguir entre entidades e objetos de valor?** Entidades são objetos mais importantes e devemos, por exemplo, projetar com cuidado como eles serão persistidos e depois recuperados de um banco de dados. Devemos também tomar cuidado com o ciclo de vida de entidades. Por exemplo, podem existir regras que governam a criação e remoção de entidades. No caso da nossa biblioteca, não se pode remover um `Usuário` se ele tiver um `Empréstimo` pendente.

Já objetos de valor são mais simples. E também eles devem ser **imutáveis**, ou seja, uma vez criados, não deve ser possível alterar seus valores internos. Por exemplo, para alterar o `Endereço` de um `Usuário` devemos abandonar o objeto antigo e criar um objeto com o `Endereço` novo. 
### Serviços

Existem operações importantes do domínio que não se encaixam em entidades e objetos de valor. Assim, o ideal é criar objetos específicos para implementar essas operações. No jargão de DDD, esses objetos são chamados de **serviços**. Em alguns sistemas, é comum ver esses objetos sendo chamados também de gerenciadores ou controladores.

A assinatura das operações de um objeto de serviço pode incluir entidades e objetos de valor. No entanto, objetos de serviço não devem possuir estado, isto é, eles devem ser **stateless**. Por isso, eles não costumam ter atributos, mas apenas métodos.

**Exemplo**: no nosso sistema de bibliotecas, podemos ter um serviço que implementa as seguintes operações:

```
class ServicoDeEmprestimo {
  emprestarLivro(Usuario, Livro) {...}
  devolverLivro(Usuario, Livro)  {...}
}  
```

Na primeira operação, realiza-se o empréstimo de um `Livro` para um certo `Usuário`. Na segunda operação, um `Usuário` devolve um `Livro` que ele tenha sob empréstimo.

Ambas as operações não são específicas nem de `Usuário`, nem de `Livro`. Por isso, DDD recomenda criar um objeto de serviço para acomodá-las.

### Agregados

**Agregados** (_aggregates_) são coleções de entidades e objetos de valor. Ou seja, algumas vezes não faz sentido raciocinar sobre entidades e objetos de valor de forma individual. Em vez disso, temos que pensar em grupos de objetos para ter uma visão consistente com o domínio que estamos modelando.

Um agregado possui um objeto raiz, que deve ser uma entidade. Externamente, o agregado é acessado a partir dessa raiz. A raiz, por sua vez, referencia os objetos internos do agregado. Porém, esses objetos internos não devem ser visíveis para o resto do sistema, ou seja, apenas a raiz pode referenciá-los.

Como formam uma unidade coerente, agregados são persistidos em conjunto em bancos de dados. A deleção de um agregado, da memória principal ou de um banco de dados, implica na deleção da sua raiz e de todos os objetos internos.

Como eles são objetos mais complexos e com objetos internos, pode ser interessante implementar métodos especificamente para criação de agregados, os quais são chamados de **fábricas**. Ou seja, tais métodos são implementações do padrão de projeto de mesmo nome.

**Exemplo**: No sistema de bibliotecas, um `Empréstimo` possui um `Usuário` (que é uma entidade) e uma lista de `ItemEmpréstimo`. Cada `ItemEmpréstimo` contém informações sobre um certo `Livro` que foi emprestado.

Logo, `Empréstimo` e `ItemEmpréstimo` formam um agregado, como mostrado na figura. Isto é, uma entidade única do ponto de vista conceitual. `Empréstimo` é a raiz do agregado e `ItemEmpréstimo` é a classe dos objetos internos, os quais não podem ser manipulados sem passar antes pela raiz.

![Exemplo de agregado](https://engsoftmoderna.info/artigos/figs/ddd-agregado.png)

Exemplo de agregado

Observe que `ItemEmpréstimo` referencia `Livro`, porém essa última classe não faz parte do agregado, pois seus objetos têm vida própria, isto é, eles existem independentemente de estarem emprestados ou não.

### Repositórios

Para implementar certos serviços do domínio precisamos antes obter referências para determinados objetos.

Por exemplo, suponha um serviço que lista os `Empréstimos` realizados por um `Usuário`. Para implementá-lo, não podemos assumir que todos os agregados do tipo `Empréstimo` estão na memória principal. Na verdade, em qualquer sistema real, eles estão armazenados em um banco de dados.

Um **repositório** é então um objeto usado para recuperar outros objetos de domínio de um banco de dados. Seu objetivo é prover uma abstração que blinde os desenvolvedores de preocupações relacionadas com acesso a bancos de dados. Normalmente, repositórios são criados para recuperar entidades ou agregados.

Em outras palavras, um repositório oferece uma abstração para o banco de dados usado pelo sistema e, assim, permite que os desenvolvedores continuem focados no domínio, em vez de ter sua atenção desviada, em certos momentos, para uma tecnologia de armazenamento de dados. Em termos mais concretos, um repositório permite manipular objetos de domínio como se eles fossem listas (ou coleções) armazenadas na memória principal. A implementação interna do repositório cuida de ler e salvar essas listas no banco de dados.

**Exemplo:** No sistema de bibliotecas, existe um repositório com métodos para recuperar `Empréstimos` armazenados em um banco de dados:

```
class RepositorioDeEmprestimos {
  List<Emprestimo> findEmprestimosDeUsuario(Usuario u) {...}
  List<Emprestimo> findEmprestimosPorData(Data inicio, Data fim) {...}
  List<Emprestimo> findEmprestimosVencidos() {...}
}
```

Além dos métodos `find*`, um repositório pode implementar métodos para salvar, atualizar e remover objetos:

```
class RepositorioDeEmprestimos {

  // métodos find* (veja acima)
  
  void salvar(Emprestimo e) {...}
  void atualizar(Emprestimo e) {...}
  void remover(Emprestimo e) {...} 
}
```
## Contextos Delimitados

É irrealista imaginar que sistemas de organizações grandes e complexas vão possuir um modelo de domínio único e baseado na mesma linguagem ubíqua.

Em vez disso, é natural que tais organizações tenham sistemas que atendem a usuários com perfis e necessidades diferentes, o que complica a definição de uma linguagem ubíqua. A solução para esse problema consiste em quebrar tais domínios complexos em domínios menores, os quais em DDD são chamados de **Contextos Delimitados**.
## Camada Anticorrupção

Às vezes, temos que integrar sistemas que estão em contextos delimitados diferentes. Um sistema A precisa usar serviços de um sistema B, que pode inclusive ser um sistema externo, isto é, de uma outra organização. Para evitar que A tenha que se adaptar e usar, mesmo que parcialmente, a linguagem ubíqua de B, pode-se usar uma **Camada Anticorrupção** para mediar essa comunicação.

Essa camada é formada por dois tipos principais de classes:

- Classes de Serviço, cujos métodos serão chamados por A e que, portanto, seguem a linguagem ubíqua desse sistema.
- Classes Adaptadoras, que convertem o modelo e os tipos de dados de B para o modelo e tipos de dados de A. Ou seja, essas classes vão isolar elementos próprios de B e evitar que eles cheguem até o sistema A.


Logo, o fluxo costuma ser o seguinte:

```
Sistema A -> [ Serviços -> Adaptadores ] -> Sistema B
```

Nesse fluxo, as classes entre colchetes constituem a Camada Anticorrupção que foi construída para integrar os sistemas A e B.

