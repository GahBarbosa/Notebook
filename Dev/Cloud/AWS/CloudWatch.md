## O que o Amazon CloudWatch faz?

O Amazon CloudWatch é um serviço de monitoramento e observação criado para engenheiros de DevOps, desenvolvedores, engenheiros de segurança de sites e gerentes de TI. O CloudWatch fornece dados e insights factíveis para monitorar suas aplicações, responder a mudanças de performance em todo o sistema e otimizar a utilização de recursos. Obtenha uma visão unificada da integridade operacional.

## Quais problemas o CloudWatch resolve?

O Amazon CloudWatch resolve o problema de responder a eventos e alarmes, à medida que eles ocorrem em sua arquitetura. O Amazon CloudWatch coleta dados operacionais e de monitoramento em forma de logs, métricas e eventos. Ele oferece uma visão unificada de serviços, recursos e aplicações da AWS executados na AWS e em servidores no local. Os clientes podem usar o CloudWatch para detectar comportamentos anômalos nos ambientes, definir alarmes e visualizar logs e métricas lado a lado. Eles podem executar ações automatizadas, solucionar problemas e descobrir insights para manter as aplicações funcionando ininterruptamente.

## Quais são os beneficios do Cloudwatch?

- O CloudWatch permite coletar métricas e logs de todos os recursos, aplicações e produtos da AWS executados nos servidores da AWS e no local. 
- Você pode monitorá-los usando uma única plataforma. Você pode usar o CloudWatch para manter a visibilidade de seus serviços, aplicações e infraestrutura, para que possa visualizar métricas importantes, como utilização de CPU e memória. 
- Você pode usar o CloudWatch para definir alarmes e realizar ações automatizadas. Ele libera recursos importantes para que você possa se concentrar na agregação de valor comercial.

## Como posso projetar uma solução de nuvem usando o CloudWatch?

Voce pode projetar uma solução usando o Amazon CloudWatch para monitorar a utilização da CPU e tomar medidas a respeito.

![[Pasted image 20250308181832.png]]

No diagrama, o CloudWatch recebe dados sobre a utilização da CPU da instância do EC2. Quando a CPU ultrapassa um percentual especificado, o CloudWatch aciona o Amazon EC2 Auto Scaling para provisionar uma instância adicional para ajudar a atender à carga de trabalho. Desse modo, a primeira instância não fica sobrecarregada.

## Como posso usar o CloudWatch?
 - Monitoramento e solução de problemas de infraestrutura
 - Otimização proativa de recursos
 - Monitoramento de aplicações

## O que mais devo ter em mente ao usar o CloudWatch?

Alguns serviços fornecem monitoramento básico do CloudWatch sem custo adicional, bem como a opção de upgrade para o monitoramento detalhado, para o qual há uma cobrança.Por exemplo, as instâncias do EC2 são habilitadas por padrão com o monitoramento básico do CloudWatch. Desse modo, os dados são disponibilizados automaticamente em períodos de 5 minutos. Se você decidir fazer upgrade para o monitoramento detalhado do CloudWatch em suas instâncias, os dados serão disponibilizados em períodos de 1 minuto, em vez de 5 minutos.

## Quanto custa o CloudWatch?

O Amazon CloudWatch não exige compromisso antecipado nem taxa mínima; você paga pelo que usar. Você é cobrado no final do mês com base no uso.

O Amazon CloudWatch cobra por alarmes, eventos personalizados, coleta de métricas e painéis que você configurou. Entretanto, você pode começar a usar o Amazon CloudWatch gratuitamente. A maioria dos produtos da AWS (Amazon EC2, Amazon S3, Amazon Kinesis e outros) envia métricas automaticamente para o CloudWatch sem custo adicional. Muitas aplicações conseguem operar de acordo com esses limites do nível gratuito.