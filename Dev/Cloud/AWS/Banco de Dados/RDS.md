## O que o Amazon RDS faz?

O Amazon Relational Database Service (Amazon RDS) é um serviço gerenciado de banco de dados relacional distribuído. Baseado na nuvem, ele foi projetado para simplificar a configuração, a operação e a escalabilidade dos bancos de dados relacionais. Processos administrativos como aplicação de patches, backup de bancos de dados e ativação de recuperação point-in-time são gerenciados automaticamente.

## Qual problema o Amazon RDS resolve?

O Amazon RDS resolve o problema de precisar comprar um banco de dados com capacidade muito grande ou muito pequena para usá-la ao longo do tempo. Com o Amazon RDS, você pode expandir ou reduzir verticalmente a escola com base nas necessidades de capacidade do banco de dados. Desse modo, você nunca pagará por uma capacidade de banco de dados superior à que precisa.

## Quais são os benefícios do Amazon RDS?

- O Amazon RDS é fácil de administrar e não requer provisionamento de infraestrutura nem instalação e manutenção de software de banco de dados. Com alguns cliques no mouse ou uma chamada de API, você pode dimensionar os recursos de computação e armazenamento do banco de dados conforme a necessidade.
- O Amazon RDS é rápido e comporta as aplicações de banco de dados mais exigentes. Você pode executar suas instâncias de banco de dados no Amazon Virtual Private Cloud (Amazon VPC), o que permite isolar suas instâncias de banco de dados. Ou você pode conectar suas instâncias de banco de dados à sua infraestrutura de TI existente por meio de uma rede privada virtual (VPN) IPsec criptografada padrão do setor.

## Como posso projetar uma solução de nuvem usando o Amazon RDS?

Você pode projetar uma solução para criar tolerância a falhasconfigurando o Amazon RDS para implantação multi-AZ. Para realizar essa tarefa, você coloca a instância primária do RDS em uma zona de disponibilidade e uma réplica standby da primária em outra zona de disponibilidade. Se a primária apresentar falha, a instância standby se tornará automaticamente a nova instância primária e seu sistema permanecerá ativo.

![[Pasted image 20250308180608.png]]

## O que mais devo ter em mente ao usar o Amazon RDS?

O Amazon RDS é totalmente gerenciado. “Totalmente gerenciado" significa que a AWS automatiza a manutenção e a segurança da instância do banco de dados sem que você faça nada. No entanto, você pode precisar de acesso para gerenciar o sistema operacional e atualizar os patches de segurança por conta própria. Nesse caso, você pode provisionar uma instância do EC2 e usá-la para hospedar seu próprio banco de dados.Suponha que você decida hospedar seu próprio banco de dados em uma instância do EC2. Nesse caso, você é responsável por várias das tarefas automatizadas que o Amazon RDS executaria automaticamente para você.

## Quanto custa o Amazon RDS?

O preço do Amazon RDS segue o modelo de pagamento somente pelo que você usa. Não há taxa mínima. Você pode pagar pelo Amazon RDS usando Instâncias On-Demand ou reservadas, de modo semelhante ao que você aprendeu sobre as opções do Amazon EC2.
O Amazon RDS disponibiliza uma seleção de tipos de instância otimizados para atender a diferentes casos de uso de bancode dados relacional.