## O que a Amazon EC2 faz?

O Amazon Elastic Compute Cloud (Amazon EC2) é um serviço da Web que disponibiliza capacidade computacional segura e redimensionável na nuvem. Ele foi projetado para facilitar a computação em nuvem na escala da Web para os desenvolvedores. Você pode usar a interface Web do Amazon EC2, que é simples, para obter e configurar a capacidade com o mínimo de atrito. Ele fornece controle completo sobre seus recursos de computação, e você pode executá-lo no ambiente de computação comprovado da Amazon.

## Qual o problema o Amazon EC2 resolve?

O Amazon EC2 resolver o problema de precisar prever as necessidades com antecipação. Portanto, ao configurar sua arquitetura, você não precisa saber a quantidade de capacidade computacional ou de volume de disco rígido que será necessária. Você pode expandir
e reduzir verticalmente a escala conforme a necessidade.

## Quais são os beneficios do Amazon EC2?

- Você pode provisionar uma instância do EC2 em apenas 5 minutos. Ele oferece opções para selecionar a CPU, o armazenamento e o sistema operacional adequados para suas necessidades específicas. 
- Com o Amazon EC2, você pode alterar o tamanho do volume e o tipo de instância sem terminar a instância.
- Você pode usar o Amazon EC2 para expandir e reduzir verticalmente
a escala para atender a necessidades sazonais. Você não precisa ter à disposição servidores extras que são usados apenas durante alguns meses do ano.

## Como posso projetar uma solução de nuvem usando o Amazon EC2?

Com o Amazon EC2, você pode projetar uma solução para criar uma aplicação multicamadas. Para construir essa solução, você cria uma instância em uma subnet pública que hospeda um site com um security group que permite a entrada e saída de tráfego da Internet. Em seguida, você pode criar outra instância que hospeda um banco de dados em uma sub-rede privada com um security group reforçado. Esse security group restringe o tráfego da Internet, mas permite que a instância do site acesse a instância do banco de dados.

![[Pasted image 20250308164904.png]]

## Como posso usar o Amazon EC2?

- hospedar um site simples
- hospedar uma aplicação web multicamadas
- computação sob demanda
- hospedar banco de dados
- backup e recuperação

## O que mais devo ter em mente ao usar o Amazon EC2?

Se você interromper uma instância, o volume do Amazon Elastic Block Store (Amazon EBS) anexado reterá seus dados. Mesmo assim você será cobrado pelo uso do volume. No entanto, se terminar a instância, todos os seus dados no volume serão excluídos permanentemente. O volume retornará à AWS para ser usado para outros clientes da AWS.

## Quanto custa o Amazon EC2?

##### Instância sob demanda

Com as Instâncias On-Demand, você paga pelas instâncias de acordo com o tempo que as utiliza. Não há necessidade de compromissos de longo prazo nem de pagamentos adiantados. Você pode aumentar ou diminuir sua capacidade computacional dependendo das demandas da aplicação e pagar apenas pelo tempo de uso.

**Caso de uso**: cargas de trabalho de computação de curto prazo que podem ser interrompidas e usuários que precisam de computação de baixo custo sem compromisso inicial ou de longo prazo.

##### Instância Spot

Você pode usar Instâncias Spot do Amazon EC2 para aproveitar a capacidade não utilizada do Amazon EC2 na Nuvem AWS para obter um desconto. Você pode economizar até 90% em comparação com os preços do On-Demand. Para obter uma Instância Spot, envie uma solicitação com as especificações da instância e o preço máximo que você está disposto a pagar por hora. Quando uma Instância Spot estiver disponível pelo preço enviado, você terá acesso a ela.

**Caso de uso**: cargas de trabalho que podem ser pausadas e reiniciadas quando os preços de computação atingem seu orçamento para Instâncias Spot.

##### Instância reservadas

As instâncias reservadas oferecem um desconto significativo (até 75%) em comparação ao preço da Instância On-Demand. Com as instâncias reservadas, você se compromete a pagar pela instância por um ou três anos, dependendo das condições com as quais você concordar ao comprá-las.

**Caso de uso**: necessidades de computação com uso constante de até um ano ou mais.