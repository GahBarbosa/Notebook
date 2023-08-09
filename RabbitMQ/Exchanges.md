A suposição por trás de uma fila de trabalho é que cada tarefa é entregue a exatamente um trabalhador. Nesta parte, faremos algo completamente diferente, entregaremos uma mensagem a vários consumidores. Esse padrão é conhecido como "publicar/assinar".

## Tipos de Exchanges 
A ideia central no modelo de mensagens no RabbitMQ é que o produtor nunca envie nenhuma mensagem diretamente para uma fila. Na verdade, muitas vezes o produtor nem sabe se uma mensagem será entregue em alguma fila.

Em vez disso, o produtor só pode enviar mensagens para uma troca. Uma troca é uma coisa muito simples. De um lado recebe mensagens dos produtores e do outro lado os empurra para as filas. A troca deve saber exatamente o que fazer com uma mensagem que recebe. Deve ser anexado a uma fila específica? Deve ser anexado a muitas filas? Ou deve ser descartado. As regras para isso são definidas pelo tipo de troca.![[Pasted image 20230808055443.png]]

### Existem 6 tipo de Exchanges
Entre eles quatro deles são tipos básicos de troca do RabbitMQ, cada um dos quais usa diferentes parâmetros e ligações para rotear mensagens, são eles:
#### Direct Exchange
O tipo Direct usa uma chave de roteamento de mensagem para transportar mensagens para filas. A chave de roteamento é um atributo de mensagem que o produtor adiciona ao cabeçalho da mensagem. Você pode considerar a chave de roteamento como um “endereço” que a central usa para determinar a fila corresponde à chave de roteamento da mensagem.

A Exchange padrão da Direct Exchange é “amq.direct“, que os AMQP brokers devem oferecer para comunicação. 

#### Topic Exchange
O tipo Topic envia mensagens para filas dependendo das correspondências entre a chave de roteamento e o padrão de roteamento da ligação da fila. As mensagens são roteadas para uma ou mais filas. Uma lista de palavras separadas por um ponto deve ser usada como chave de roteamento (.).

A Exchange padrão da Topic Exchange, “amq.topic”.

#### Fanout Exchange
O tipo Fanout duplica e roteia uma mensagem recebida para quaisquer filas associadas, independentemente de chaves de roteamento ou correspondência de padrão.

A Exchange padrão da Fanout, “amq.fanout”.

#### Headers Exchange
O tipo de Headers usa argumentos com cabeçalhos e valores opcionais para rotear mensagens. As Headers Exchange são idênticas às Topic Exchange, exceto que, em vez de usar chaves de roteamento, as mensagens são roteadas com base nos valores do cabeçalho. 

Na ligação entre troca e fila, um argumento específico denominado “x-match” indica se todos os cabeçalhos devem corresponder ou apenas um. A propriedade “x-match” tem dois valores possíveis: “any” e “all”, sendo “all” o padrão. 

A Exchange padrão da Headers é “amq.headers”.

#### Além disso, existem mais dois tipos de Exchanges:

#### Default Exchange
A  Default Exchange é uma Direct Exchange declarada sem nome. Normalmente, uma string vazia é frequentemente usada para indicá-lo.

#### Dead Letter Exchange
Alguns consumidores podem não conseguir processar determinados alertas e a própria fila pode rejeitar mensagens como resultado de determinados eventos. Por exemplo, uma mensagem é descartada se não houver fila correspondente para ela. Nesse caso, Dead Letter Exchanges deve ser implementado para que essas mensagens possam ser salvas e reprocessadas posteriormente. O “Dead Letter Exchange” é um aprimoramento do AMQP fornecido pelo RabbitMQ. Essa Exchange tem a capacidade de capturar mensagens que não são entregues.