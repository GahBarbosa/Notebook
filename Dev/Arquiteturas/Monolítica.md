Uma arquitetura monolítica é um modelo tradicional de software, construído como uma unidade unificada, independente e independente de outros aplicativos. Para fazer uma alteração nesse tipo de aplicativo, é necessário atualizar toda a pilha acessando a base de código e construindo e implantando uma versão atualizada da interface do lado do serviço. Isso torna as atualizações restritivas e demoradas.

Os monólitos podem ser convenientes no início da vida de um projeto para facilitar o gerenciamento de código, sobrecarga cognitiva e implantação. Isso permite que tudo no monólito seja liberado de uma só vez.

### Vantagens de uma arquitetura monolítica

#### Velocidade de Desenvolvimento Inicial 
Quando um aplicativo é construído com uma base de código, a principal vantagem é a rápida velocidade inicial de desenvolvimento devido à simplicidade de ter um aplicativo baseado em uma base de código.
#### Implantação inicial fácil
Por ser desenvolvido como um arquivo ou diretório facilita a implantação.
#### Desempenho
Em uma base de código e repositório centralizados, uma [[API]] geralmente pode executar a mesma função que várias [[API]] executam com [[Microsserviços]].
#### Testes simplificados 
Os testes ponta a ponta podem ser realizados mais rapidamente do que com um aplicativo distribuído.
#### Depuração fácil 
Com todo o código localizado em um só lugar, é mais fácil seguir uma solicitação e encontrar um problema.

### Desvantagens de uma arquitetura monolítica

Os aplicativos monolíticos podem ser bastante eficazes até que cresçam muito e o dimensionamento se torne um desafio. Fazer uma pequena alteração em uma única função requer compilar e testar toda a plataforma, o que vai contra a abordagem ágil preferida pelos desenvolvedores atuais.

#### Desenvolvimento de novas funcionalidades mais lenta
Um aplicativo grande e monolítico torna o desenvolvimento mais complexo tendo mais pontos sensíveis a serem pensados e portanto mais lento.
#### Escalabilidade 
Você não pode dimensionar componentes individuais para atingir demandas de recursos específicos.
#### Confiabilidade 
Se houver algum erro em algum módulo, isso poderá afetar a disponibilidade de toda a aplicação.
#### Falta de flexibilidade
Quaisquer alterações na estrutura, linguagem ou tecnologia usadas afetam todo o aplicativo, tornando as alterações muitas vezes caras e demoradas.
#### Implantação 
Uma pequena alteração em um aplicativo monolítico requer a reimplantação de todo o monólito.