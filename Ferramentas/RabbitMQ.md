RabbitMQ é um intermediário de mensagens: ele aceita e encaminha mensagens. Você pode pensar nisso como uma agência postal: quando você coloca a correspondência que deseja postar em uma caixa postal, pode ter certeza de que o carteiro acabará entregando a correspondência ao seu destinatário. Nessa analogia, RabbitMQ é uma caixa postal, uma agência postal e um carteiro.

Existem 3 entidades no RabbitMQ:
- Producer, um programa que envia mensagens é uma Producer
- Queue é o nome da caixa postal no RabbitMQ. Embora as mensagens fluam pelo RabbitMQ e seus aplicativos, elas só podem ser armazenadas dentro de uma fila. Uma fila é limitada apenas pelos limites de memória e disco do host, é essencialmente um grande buffer de mensagens. Muitos produtores podem enviar mensagens que vão para uma fila e muitos consumidores podem tentar receber dados de uma fila.
- Consumer é um programa que espera principalmente para receber mensagens

![[Pasted image 20230808034301.png]]

Please take a look at the rest of the [documentation](https://www.rabbitmq.com/documentation.html) before going live with your app. We particularly recommend the following guides: [Publisher Confirms and Consumer Acknowledgements](https://www.rabbitmq.com/confirms.html), [Production Checklist](https://www.rabbitmq.com/production-checklist.html) and [Monitoring](https://www.rabbitmq.com/monitoring.html).



[[Dispatch]]
[[Message durability]]
[[Message acknowledgment]]
[[Exchanges]]
[[Exchanges]]
[[Remote Call Response]]