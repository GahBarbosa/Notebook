GraphQL significa Graph Query Language, é uma linguagem de query assim como [[Dev/Armazenamento de Dados/Bancos de Dados Relacionais (RDBMS)/SQL]] (Structured Query Language) porém seu uso não envolve implementar banco de dados, mas ser uma alternativa para a arquitetura da Api [[REST]]

Com [[REST]], você precisa fazer três solicitações para diferentes endpoints para buscar os dados necessários. Você também está fazendo overfetching, pois os endpoints retornam informações adicionais que não são necessárias.![[Pasted image 20230807045301.png]]

Usando o GraphQL, o client pode especificar exatamente os dados de que precisa em uma consulta.![[Pasted image 20230807045342.png]]

## Apollo 
O [[Apollo]] GraphOS é a plataforma para criar, gerenciar e escalonar Graphs: uma rede de micro serviços e fontes de dados, tudo composto em uma única API.