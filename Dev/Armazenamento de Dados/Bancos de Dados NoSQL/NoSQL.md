O NoSQL é uma tecnologia de banco de dados que armazena dados em esquemas flexíveis que escalam facilmente. Durante décadas, o modelo de dados predominante no desenvolvimento de aplicações foi o modelo de dados relacional que armazenava dados em tabelas feitas de linhas e colunas. A linguagem de consulta estruturada (SQL) foi usada para criar e editar essas tabelas relacionais. Somente em meados dos anos 2000 que outros modelos de dados flexíveis começaram a ser adotados e ter um uso mais significativo. Para diferenciar e categorizar essas novas classes de bancos e modelos de dados, o termo NoSQL foi criado. NoSQL significa _não apenas SQL ou não SQL_. Muitas vezes, o termo NoSQL é usado de forma intercambiável com _não relacional_.

## Quais são as vantagens dos bancos de dados NoSQL

As aplicações modernas enfrentam vários desafios que podem ser resolvidos pelos bancos de dados NoSQL. Por exemplo, as aplicações processam um grande volume de dados de fontes diferentes, como mídias sociais, sensores inteligentes e bancos de dados de terceiros. Todos esses dados díspares não se encaixam perfeitamente no modelo relacional. A aplicação de estruturas tabulares pode levar a problemas de redundância, duplicação de dados e desempenho em grande escala.

Os bancos de dados NoSQL são desenvolvidos especificamente para modelos de dados não relacionais e possuem esquemas flexíveis para a construção de aplicações modernas. Eles são amplamente reconhecidos por sua facilidade de desenvolvimento, funcionalidade e performance em escala. Os benefícios dos bancos de dados NoSQL estão listados abaixo.

### Flexibilidade

Os bancos de dados NoSQL geralmente fornecem esquemas flexíveis que permitem um desenvolvimento mais rápido e iterativo. O modelo de dados flexível torna os bancos de dados NoSQL ideais para dados semiestruturados e não estruturados.

### Escalabilidade

Os bancos de dados NoSQL são normalmente projetados para aumentar a escala horizontalmente usando clusters distribuídos de hardware, em vez de serem ampliados adicionando servidores caros e robustos. Alguns provedores de nuvem lidam com essas operações nos bastidores como um serviço totalmente gerenciado.

### Alto desempenho

Os bancos de dados NoSQL são otimizados para modelos de dados e padrões de acesso específicos. Eles permitem um desempenho maior do que se você estivesse tentando obter uma funcionalidade semelhante com bancos de dados relacionais.

### Altamente funcional

Os bancos de dados NoSQL fornecem APIs e tipos de dados altamente funcionais criados especificamente para cada um de seus respectivos modelos de dados.

## Quais são os casos de uso dos bancos de dados NoSQL

Você pode usar bancos de dados NoSQL para criar uma grande variedade de aplicações móveis, de Internet das Coisas (IoT), de jogos e da web de alto desempenho que oferecem excelentes experiências de usuário em grande escala. A variedade de bancos de dados NoSQL e seus respectivos casos de uso são amplos. Embora seja difícil apresentar um conjunto representativo de casos de uso, abaixo, fornecemos alguns exemplos ilustrativos para começar a pensar e incentivamos você a aprender mais sobre cada banco de dados NoSQL e seus respectivos casos de uso.

### Gerenciamento de dados em tempo real

Você pode fornecer recomendações em tempo real, personalização e experiências de usuário aprimoradas com bancos de dados NoSQL. Por exemplo, o Disney+ oferece sua extensa biblioteca de conteúdo digital para mais de 150 milhões de assinantes usando a tecnologia de banco de dados NoSQL. Ele pode escalar e fornecer recursos populares, como Continuar assistindo, Watchlist e recomendações personalizadas com o Amazon DynamoDB.

### Segurança na nuvem

Você pode usar bancos de dados de grafos para descobrir rapidamente relacionamentos complexos em seus dados. Por exemplo, a Wiz reinventou a segurança na nuvem como um gráfico usando o Amazon Neptune. A Wiz ajuda seus clientes a melhorar sua postura de segurança identificando e corrigindo rapidamente os riscos mais críticos. Eles usam o modelo gráfico armazenado no Amazon Neptune para descobrir a combinação tóxica de fatores de risco que representam riscos críticos. Os mecanismos de risco da Wiz percorrem o gráfico e, em segundos, unem uma série de fatores de risco interconectados em um gráfico de segurança.

### Aplicações de alta disponibilidade

Os bancos de dados NoSQL distribuídos são excelentes para criar aplicações de alta disponibilidade e baixa latência para mensagens, mídias sociais, compartilhamento de arquivos e muito mais. Por exemplo, o Snapchat possui mais de 290 milhões de usuários enviando bilhões de fotos e mensagens de vídeo diariamente. Ele usa sistemas de banco de dados NoSQL para reduzir a latência média do envio de mensagens em 20%.

## Como funcionam os bancos de dados NoSQL

Os bancos de dados NoSQL usam uma variedade de modelos de dados para acessar e gerenciar os dados. Há diferenças na implementação com base no modelo de dados. No entanto, muitos bancos de dados NoSQL usam Javascript Object Notation ([[JSON]]), um formato aberto de intercâmbio de dados que representa os dados como uma coleção de pares de nome-valor.

### Exemplo de banco de dados NoSQL

Considere este exemplo de modelagem do esquema para um banco de dados simples de livros:

- Em um banco de dados relacional, um registro de livro é normalmente desmontado (ou “normalizado”) e armazenado em tabelas separadas, e os relacionamentos são definidos por restrições de chave primária e externa. Neste exemplo, a tabela Livros possui colunas para ISBN, Título do Livro e Número da Edição; a tabela Autores possui colunas para ID do Autor e Nome do Autor; e por fim, a tabela Autor-ISBN possui colunas para ID do Autor e ISBN. O modelo relacional é projetado para permitir que o banco de dados imponha a integridade referencial entre as tabelas no banco de dados, normalizadas para reduzir a redundância e geralmente otimizadas para armazenamento.
- Em um banco de dados NoSQL, um registro de livro é normalmente armazenado como um documento. Para cada livro, o item, ISBN, Título do Livro, Número da Edição, Nome do Autor e ID do Autor são armazenados como atributos em um único documento. Neste modelo, os dados são otimizados para desenvolvimento intuitivo e escalabilidade horizontal.

### Terminologia do NoSQL

A tabela a seguir compara a terminologia usada pelos bancos de dados NoSQL selecionados com a terminologia usada pelos bancos de dados SQL.  

|**SQL**|**[[MongoDB]]**|**DynamoDB**|**Cassandra**|**Couchbase**|
|---|---|---|---|---|
|Tabela|Coleta|Tabela|Tabela|Bucket de dados|
|Linha|Documento|Item|Linha|Documento|
|Coluna|Campo|Atributo|Coluna|Campo|
|Chave primária|ObjectId|Chave primária|Chave primária|ID do documento|
|Índice|Índice|Índice secundário|Índice|Índice|
|Visualização|Visualização|Índice secundário global|Visualização materializada|Visualização|
|Tabela ou objeto aninhado|Documento incorporado|Mapa|Mapa|Mapa|
|Matriz|Matriz|Lista|Lista|Lista|

## Quais são os tipos de bancos de dados NoSQL

Existem vários sistemas de banco de dados NoSQL diferentes devido às variações na forma como gerenciam e armazenam dados sem esquema. Explicamos alguns dos tipos comuns abaixo.

### Bancos de dados de chave-valor

Os bancos de dados de chave-valor são altamente particionáveis e permitem o escalonamento horizontal em um nível que outros tipos de bancos de dados NoSQL talvez não alcancem. Um banco de dados de chave-valor armazena dados como um conjunto de pares de chave-valor em que uma chave funciona como um identificador exclusivo. As chaves e os valores podem ser qualquer coisa, desde objetos simples até objetos compostos complexos. Casos de uso como jogos, tecnologia de publicidade e IoT se prestam particularmente bem ao design de dados de armazenamento de chave-valor.

### Bancos de dados de documentos

Bancos de dados orientados a documentos têm o mesmo formato de modelo de documento que os desenvolvedores utilizam no código da aplicação. Eles armazenam dados como objetos JSON que são flexíveis, semiestruturados e de natureza hierárquica. O modelo banco de dados de documentos funciona bem com catálogos, perfis de usuários e sistemas de gerenciamento de conteúdo, onde cada documento é único e evolui com o passar do tempo.

### Bancos de dados de grafos

Os bancos de dados de grafos foram criados especificamente para possibilitar o armazenamento de relacionamentos e a navegação por eles. Eles usam nós para armazenar entidades de dados e bordas para armazenar os relacionamentos entre as entidades. Uma borda sempre tem um nó inicial, um nó final, um tipo e uma direção. Pode descrever relacionamentos, ações, propriedade entre pais e filhos e assim por diante. A quantidade e os tipos de relacionamentos que um nó pode ter são ilimitados. Você pode usar um banco de dados de [[GraphQL]] para criar e executar aplicações que funcionam com conjuntos de dados altamente conectados. Os casos de uso típicos de um banco de dados de grafos incluem redes sociais, mecanismos de recomendação, detecção de fraudes e gráficos de conhecimento.

### Bancos de dados na memória

Enquanto outros bancos de dados não relacionais armazenam dados em disco ou SSDs, os armazenamentos de dados na memória são projetados para eliminar a necessidade de acessar discos. Eles são ideais para aplicações que exigem tempos de resposta de microssegundos ou têm grandes picos de tráfego. Você pode usá-los em aplicações de jogos e tecnologia de anúncios para recursos como tabelas de classificação, armazenamentos de sessões e análises em tempo real.

### Pesquisar bancos de dados

Um banco de dados de mecanismo de pesquisa é um tipo de banco de dados não relacional dedicado à pesquisa de conteúdo de dados. Ele usa índices para categorizar características semelhantes entre os dados e facilitar a capacidade de pesquisa. Os bancos de dados dos mecanismos de pesquisa são otimizados para classificar dados não estruturados, como imagens e vídeos. Eles podem fornecer visualizações e análises quase em tempo real indexando, agregando e pesquisando dados semiestruturados, como logs e métricas.

## Quais são as diferenças entre bancos de dados NoSQL e SQL

Os bancos de dados [[Dev/Armazenamento de Dados/Bancos de Dados Relacionais (RDBMS)/SQL]] modelam relacionamentos de dados como tabelas. As linhas na tabela representam uma coleção de valores relacionados de um objeto ou de uma entidade. Cada coluna na tabela representa um atributo de dados, e um campo (ou célula da tabela) armazena o valor real do atributo. Você pode usar um sistema de gerenciamento de banco de dados relacional (RDBMS) para acessar os dados de várias maneiras diferentes sem reorganizar as próprias tabelas do banco de dados. As principais diferenças entre bancos de dados relacionais e não relacionais são apresentadas na tabela abaixo.

|   |   |   |
|---|---|---|
||Bancos de dados relacionais|Bancos de dados NoSQL|
|Workloads ideais|Os bancos de dados relacionais são projetados para aplicações de processamento de transações on-line (OLTP) transacionais e altamente consistentes. Eles também são bons para processamento analítico on-line (OLAP).|Os bancos de dados do NoSQL são projetados para vários padrões de acesso aos dados que incluem aplicações de baixa latência. Os bancos de dados de pesquisa NoSQL são projetados para análise de dados semiestruturados.|
|Modelo de dados|O modelo relacional normaliza dados em tabelas, compostas por linhas e colunas. Um esquema define estritamente tabelas, colunas, índices, relações entre tabelas e outros elementos do banco de dados. O banco de dados impõe a integridade referencial nos relacionamentos entre as tabelas.|Os bancos de dados NoSQL fornecem uma variedade de modelos de dados, como chave-valor, documento, gráfico e coluna, que são otimizados para performance e escala.|
|Propriedades ACID|Bancos de dados relacionais fornecem propriedades de atomicidade, consistência, isolamento e durabilidade (ACID):<br><br>- A atomicidade exige uma transação para executar completamente ou não é executada de forma alguma.<br>- A consistência exige que os dados estejam em conformidade com o esquema do banco de dados quando uma transação for confirmada.<br>- O isolamento exige que as transações simultâneas sejam executadas separadamente umas das outras.<br>- A resiliência exige a capacidade de se recuperar de uma falha do sistema ou falta de energia inesperada para o último estado conhecido.|A maioria dos bancos de dados NoSQL oferece compensações ao relaxar algumas das propriedades ACID dos bancos de dados relacionais em favor de um modelo de dados mais flexível que pode ser escalado horizontalmente. Isso torna os bancos de dados NoSQL uma excelente opção para casos de uso de baixa latência e alto throughput que precisam ser escalados horizontalmente além das limitações de uma única instância.|
|Performance|A performance normalmente depende do subsistema do disco. A otimização de consultas, índices e estrutura de tabela é necessária para alcançar máxima performance.|A performance geralmente é uma função do tamanho do cluster do hardware subjacente, da latência de rede e da aplicação que faz a chamada.|
|Escala|Os bancos de dados relacionais geralmente escalam verticalmente o tamanho ao aumentar os recursos de computação do hardware, ou escalam horizontalmente o tamanho ao adicionar réplicas para workloads somente leitura.|Os bancos de dados NoSQL geralmente são particionáveis. Isso ocorre porque os padrões de acesso podem ser escalados horizontalmente usando a arquitetura distribuída para aumentar o throughput que fornece desempenho consistente em uma escala quase ilimitada.|
|APIs|As solicitações para armazenar e recuperar dados são comunicadas usando consultas compatíveis com uma Structured Query Language (SQL – Linguagem de consultas estruturadas). Essas consultas são analisadas e executadas pelo banco de dados relacional.|APIs baseadas em objetos permitem que desenvolvedores de aplicações armazenem e restaurem facilmente estruturas de dados. As chaves de partição permitem que as aplicações procurem pares de chave-valor, conjuntos de colunas ou documentos semiestruturados que contenham objetos e atributos de aplicações serializadas.|