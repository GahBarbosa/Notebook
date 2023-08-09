Com o [[Message acknowledgment]] mesmo que o consumidor morra, a tarefa não é perdida. Mas nossas tarefas ainda serão perdidas se o servidor RabbitMQ parar.

Quando o RabbitMQ for encerrado ou travado, ele esquecerá as filas e mensagens, a menos que você diga para não fazê-lo. Duas coisas são necessárias para garantir que as mensagens não sejam perdidas: precisamos marcar a fila e as mensagens como duráveis.

Primeiro, precisamos ter certeza de que a fila sobreviverá a uma reinicialização do nó RabbitMQ. Para fazer isso, precisamos declará-los como durável:
```js
channel.assertQueue('hello', {durable: true});
```
```js
channel.sendToQueue(queue, Buffer.from(msg), {persistent: true});
```

Embora este comando esteja correto por si só, ele não funcionará em uma fila chamada existente com parâmetros diferentes e retornará um erro para qualquer programa que tente fazer isso.

#### Observação sobre persistência de mensagem
Marcar mensagens como persistentes não garante totalmente que uma mensagem não será perdida. Embora diga ao RabbitMQ para salvar a mensagem no disco, ainda há uma pequena janela de tempo quando o RabbitMQ aceitou uma mensagem e ainda não a salvou. Além disso, o RabbitMQ não faz fsync(2) para cada mensagem -- pode ser apenas salvo no cache e não realmente gravado no disco. As garantias de persistência não são fortes, mas são mais do que suficientes para nossa fila de tarefas simples. Se você precisar de uma garantia mais forte, poderá usar as  [publisher confirms](https://www.rabbitmq.com/confirms.html).
