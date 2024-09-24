DTO (Data Transfer Object) é um padrão de software voltado para a transferência de dados entre as camadas de uma aplicação. Ele consiste basicamente no entendimento de como as informações trafegam dentro de um sistema.
#### Compatibilidade

A questão é que dados externos podem vir de diversas maneiras e formatos, como API [[REST]], [[CLI]], [[Dev/Protocolos/gRPC|gRPC]] ou sistemas de mensageria.

E como os dados não necessariamente chegam num formato compatível, as informações passam pelas camadas mais internas do sistema até chegarem ao nível de entidade, que são os fundamentos básicos de toda a aplicação.

Ocasionalmente recebemos informações que não são compatíveis com a nossa estrutura e mesmo nós, que criamos