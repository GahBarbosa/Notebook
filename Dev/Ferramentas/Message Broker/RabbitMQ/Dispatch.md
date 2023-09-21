## Round-robin dispatch
Round-robin é uma estratégia de balanceamento de carga usada no RabbitMQ. 
Quando dois *Consumers* estão conectados a uma única fila eles automaticamente entram em Round-robin que funciona distribuindo mensagens uniformemente entre os consumidores.

![[Pasted image 20230808041237.png]]
## Fair dispatch
Você deve ter notado que o dispatching ainda não funciona exatamente como queremos. Por exemplo, em uma situação com dois trabalhadores, quando todas as mensagens ímpares são pesadas e as mensagens pares são leves, um trabalhador estará constantemente ocupado e o outro dificilmente fará qualquer trabalho. Bem, RabbitMQ não sabe nada sobre isso e ainda enviará mensagens uniformemente.

Isso acontece porque o RabbitMQ apenas despacha uma mensagem quando a mensagem entra na fila. Ele não olha para o número de mensagens não confirmadas para um consumidor. Ele simplesmente despacha cegamente cada mensagem para os consumidores.

Para contornar isso, podemos usar o método de prefetch com o valor de 1. Isso diz ao RabbitMQ para não enviar mais de uma mensagem para um trabalhador por vez. Ou, em outras palavras, não despache uma nova mensagem para um trabalhador até que ele tenha processado e reconhecido a anterior. Em vez disso, ele o despachará para o próximo trabalhador que ainda não estiver ocupado.
```js
channel.prefetch(1);
```
![[Pasted image 20230808045146.png]]