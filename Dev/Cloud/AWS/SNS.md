## O que faz o Amazon SNS faz?

O Amazon Simple Notification Service (Amazon SNS) é um serviço da Web que facilita a configuração, a operação e o envio de notificações usando a nuvem. Ele fornece aos desenvolvedores um recurso altamente escalável, flexível e econômico para publicar mensagens de uma aplicação e imediatamente entregá-las aos assinantes. Esses assinantes podem ser destinatários de notificação ou outras aplicações.

## Quais são os beneficios do Amazon SNS?

- Você pode usar o Amazon SNS para enviar mensagens ou notificações diretamente aos usuários em 200 países. As mensagens podem ser enviadas com mensagens de texto SMS, por push móvel nas plataformas Apple, Android e outras ou por e-mail (SMTP).
- O Amazon SNS usa várias estratégias que funcionam juntas para oferecer durabilidade de mensagem. Se um endpoint inscrito não estiver disponível, o Amazon SNS inicia uma política de nova tentativa de entrega de mensagem para reenviá-la.

## Como posso projetar uma solução de nuvem usando o Amazon SNS?

Você pode usar o Amazon SNS para criar uma solução para notifica-lo sobre falhas em sua arquitetura.

![[Pasted image 20250309112130.png]]

Neste diagrama, uma instância do Amazon EC2 apresenta falha e o Amazon CloudWatch é notificado. Em seguida, o CloudWatch desencadeia uma ação para criar uma nova instância por meio do AWS Auto Scaling. Ao mesmo tempo, o CloudWatch aciona o Amazon SNS para notificar os assinantes apropriados, para que eles possam investigar o problema mais detalhadamente.

## Como posso usar o Amazon SNS?

Você pode usar o Amazon SNS para criar tópicos. Tópico é um ponto de acesso que identifica um assunto ou tipo de evento específico. Os tópicos do SNS são definidos como tópicos padrão ou tópicos primeiro a entrar, primeiro a sair (FIFO). Escolha cada tópico para saber mais.

Os tópicos padrão podem ser usados em diversos cenários se sua aplicação puder processar as mensagens que chegam mais de uma vez e fora de ordem. Alguns exemplos são: distribuição de mensagens para codificação de mídia, detecção de fraudes, cálculo de impostos, índice de pesquisa e sistemas de alertas críticos.

Os tópicos FIFO foram criados para aprimorar o sistema de mensagens entre aplicações quando a ordem das operações e dos eventos for essencial ou não puder haver duplicatas. Alguns exemplos são: distribuição de mensagens para registro em log de transações bancárias, monitoramento de estoque, rastreamento de voos, gerenciamento de inventário e sistemas de atualização de preços.

## O que mais devo ter em mente ao usar o Amazon SNS?

O Amazon SNS não pode automatizar as mensagens por si só. Ele precisa funcionar com um serviço como o Amazon CloudWatch ou o AWS Lambda, que pode monitorar o que está ocorrendo em sua arquitetura. Esse serviço também precisa acionar o Amazon SNS para enviar uma notificação, com base nas configurações de seu sistema.

## Quanto custa o Amazon SNS?

O Amazon SNS nao tem taxas iniciai, compromissos obrigatórios nem contrato de longo prazo. Você paga apenas pelo que usa, conm base no tópico usado.