## Callback Queue
Para receber uma resposta, precisamos enviar um endereço de fila de 'callback' com a solicitação com o parâmetro 'replyTo'. Podemos usar a Default Exchange:
```js 
channel.assertQueue('', {
  exclusive: true
});

channel.sendToQueue('rpc_queue', Buffer.from('10'), {
   replyTo: queue_name
});

# ... then code to read a response message from the callback queue ...
```
## Correlation
No método apresentado acima, sugerimos a criação de uma fila de retorno de chamada para cada solicitação RPC. Isso é bastante ineficiente, mas felizmente existe uma maneira melhor - vamos criar uma única fila de retorno de chamada por cliente.

Isso levanta um novo problema, tendo recebido uma resposta nessa fila, não está claro a qual solicitação a resposta pertence. É quando a propriedade correlation_id é usada. Vamos defini-lo com um valor exclusivo para cada solicitação. Mais tarde, quando recebermos uma mensagem na fila de retorno de chamada, veremos essa propriedade e, com base nela, poderemos corresponder uma resposta a uma solicitação. Se virmos um valor de correlation_id desconhecido, podemos descartar a mensagem com segurança - ela não pertence às nossas solicitações.

Você pode perguntar, por que devemos ignorar mensagens desconhecidas na fila de retorno de chamada, em vez de falhar com um erro? É devido à possibilidade de uma condição de corrida no lado do servidor. Embora improvável, é possível que o servidor RPC morra logo após nos enviar a resposta, mas antes de enviar uma mensagem de confirmação da solicitação. Se isso acontecer, o servidor RPC reiniciado processará a solicitação novamente. É por isso que no cliente devemos lidar com as respostas duplicadas normalmente, e o RPC deve ser idealmente independente.
![[Pasted image 20230809031854.png]]