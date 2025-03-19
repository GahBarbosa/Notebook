## O que a Amazon VPC faz?

O Amazon Virtual Private Cloud (Amazon VPC) é um serviço que permite executar recursos da AWS em uma rede virtual isolada logicamente definida por você. Como a Amazon VPC é um produto fundamental da AWS, ela facilita a personalização da configuração de rede da VPC. Você pode criar uma subnet voltada ao público para seus servidores Web com acesso à Internet. Você também pode usar a Amazon VPC para colocar seus sistemas backend, como bancos de dados ou servidores de aplicações, em uma sub-rede privada sem acesso à Internet. Com a Amazon VPC, você pode usar várias camadas de segurança para ajudar a controlar o acesso às instâncias do Amazon [[EC2]] em cada subnet. Essas camadas incluem security groups e listas de controle de acesso à rede (network ACLs).

## Qual problema a Amazon VPC resolve?

A Amazon VPC oferece recursos que você pode usar sob demanda para aumentar e monitorar a segurança da nuvem privada virtual (VPC). Portanto, você pode criar um datacenter conforme a necessidade e terminá-lo quando não precisar mais dele.

## Quais são os beneficios da Amazon VPC?

- A Amazon VPC oferece recursos de segurança avançados que você pode usar para filtragem de entrada e saída no nível da instância e da subnet.
- Com a configuração simples da Amazon VPC, você gasta menos tempo configurando, gerenciando e validando. Desse modo, você pode se concentrar na construção das aplicações executas em suas VPCs.
- A Amazon VPC ajuda você a controlar seu ambiente de rede virtual. Usando a Amazon VPC, você pode escolher seu próprio intervalo de endereços IP, criar suas próprias subnets e configurar tabelas de rotas para qualquer gateway disponível.

## Como posso projetar uma solução de nuvem usando a Amazon VPC?

O diagrama mostra como você pode usar uma VPC para criar uma solução que tenha uma subnet pública e uma sub-rede privada. A subnet pública tem uma instância do EC2 que hospeda uma aplicação Web com acesso à Internet. A sub-rede privada tem uma instância do [[RDS]] protegida contra acesso direto à Internet.

![[Pasted image 20250308164904.png]]

## Como posso usar a Amazon VPC?

- hospedar um site simples
- hospedar uma aplicação web multicamadas
- estender sua rede corporativa

## Quanto custa a Amazon VPC?


No nível básico, a Amazon VPC não tem nenhum custo. Na verdade, ao configurar sua conta da AWS, você recebe uma VPC padrão. Vários componentes que integram a VPC não custam nada para você, como subnets, tabelas de rotas, network ACLS, security groups e um internet gateway.

Entretanto, você também pode adicionar recursos à Amazon VPC, como um gateway NAT e IPs elásticos que têm cobranças correspondentes.

Além disso, qualquer serviço que você acrescentar à Amazon VPC, como o Amazon EC2, terá o custo correspondente a esse serviço.