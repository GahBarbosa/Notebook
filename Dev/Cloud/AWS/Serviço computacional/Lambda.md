## O que o AWS Lambda faz?

O AWS Lambda é um serviço computacional sem servidor que você pode usar para executar código de role sem provisionar nem gerenciar servidores. Você pode usar o Lambda para executar código de role para praticamente qualquer tipo de aplicação ou serviço de backend. Faça upload de seu código que o Lambda se encarrega de todos os itens necessários para executar e dimensionar seu código para alta disponibilidade.

## Qual problema o AWS Lambda resolve?

O AWS Lambda elimina toda a administração referente a serviços de aplicação ou backend que podem ser processados em trechos de código. Você faz upload de seu código como um arquivo .zip ou imagem de contêiner. Em seguida, o Lambda aloca de forma automática e precisa o poder computacional para executar seu código com base na solicitação ou no evento de entrada, para qualquer escala de tráfego. Você pode configurar seu código para que ele seja acionado automaticamente por mais de 200 serviços e aplicações de software como serviço (SaaS) ou chamá-lo diretamente usando qualquer aplicação Web ou aplicativo móvel.

## O que mais devo ter em mente ao usar o AWS Lambda?

O limite de tempo de execução do AWS Lambda para cada invocação é 15 minutos. Se suas necessidades de computação exigirem mais de 15 minutos de tempo de execução, você precisará usar uma instância do EC2, em vez de o Lambda.

## Quanto custa o AWS Lambda?

Com o AWS Lambda, você paga somente pelo que usa. Você é cobrado pelo número de solicitações de suas funções do Lambda e pela duração, pelo tempo que leva para que seu código seja executado.

O nível sempre gratuito do AWS Lambda inclui 1 milhão de solicitações gratuitas por mês e 400.000 GB/segundo de tempo de computação por mês.

Nenhuma cobrança é incorrida quando o código não está em execução.