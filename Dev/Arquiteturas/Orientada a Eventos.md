Uma Arquitetura orientada a eventos ( EDA ) usa eventos para acionamento e comunicação entre serviços desacoplados e é comum em aplicações modernas criadas com [[Microsserviços]]. Um evento é uma mudança ou uma atualização no estado, como um item adicionado a um carrinho de compras em um site de comércio eletrônico. Eventos podem conter o estado (o item comprado, o preço ou um endereço de entrega) ou podem ser identificadores (uma notificação de que um pedido foi despachado, por exemplo).

As arquiteturas orientadas por eventos têm três componentes: os produtores, os roteadores e os consumidores de eventos. Um produtor publica o evento no roteador, que filtra e envia os eventos aos consumidores. Serviços produtores e serviços consumidores são dissociados, o que permite que sejam escalados, atualizados e implantados de forma independente.

### Benefícios de uma arquitetura orientada por eventos

#### Escalabilidade e falha de maneira independentemente
Com o desacoplamento dos serviços, eles reconhecem apenas o roteador de eventos, e não uns aos outros. Isso significa que, mesmo que sejam interoperáveis, se um serviço apresentar uma falha, os serviços restantes continuarão em execução.

#### Desenvolvimento com agilidade
Você não precisa mais escrever código personalizado para pesquisar, filtrar e rotear eventos: o roteador de eventos filtrará e enviará eventos automaticamente aos consumidores. O roteador também elimina a necessidade de coordenação pesada entre serviços produtores e consumidores, acelerando assim o seu processo de desenvolvimento.  

#### Auditoria com facilidade
Um roteador de eventos atua como um local centralizado para auditar sua aplicação e definir políticas. Essas políticas podem restringir quem é capaz de publicar e assinar um roteador e controlam quais usuários e recursos têm permissão para acessar seus dados. Você também pode criptografar seus eventos em trânsito e em repouso.  

#### Redução dos custos
Arquiteturas orientadas por eventos são baseadas em push e, portanto, tudo acontece sob demanda à medida que o evento se apresenta no roteador. Dessa forma, não acontece pesquisas contínuas para verificar a presença de um evento. Isso significa menor consumo de largura de banda da rede, menos utilização de CPU, menos capacidade ociosa da frota e menos [[Handshake]] Secure Sockets Layer ([[SSL]])/Transport Layer Security ([[TLS]]).

![[Pasted image 20231009082241.png]]

### Quando usar essa arquitetura

#### Monitoramento e geração de alertas de estados de recursos
Em vez de conferir continuamente seus recursos, você pode usar uma arquitetura orientada por eventos para monitorar e receber alertas sobre anomalias, alterações e atualizações. 

Arquiteturas orientadas por eventos são ideais para aumentar a agilidade e a mobilidade. Geralmente, elas se encontram em aplicações modernas que usam [[Microsserviços]] ou em qualquer aplicação que tenha componentes desacoplados. Para adotar uma arquitetura orientada por eventos, talvez seja necessário repensar de que maneira você visualiza o design da aplicação. 
