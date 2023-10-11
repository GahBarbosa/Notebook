Microsserviços são uma abordagem arquitetônica e organizacional do desenvolvimento de software na qual o software consiste em pequenos serviços independentes que se comunicam usando [[API]] bem definida. 

As arquiteturas de microsserviços facilitam a escalabilidade e agilizam o desenvolvimento de aplicativos, habilitando a inovação e acelerando o tempo de introdução de novos recursos no mercado.

#### Diferenças entre as arquiteturas monolítica e de microsserviços
Com as [[Arquitetura Monolítica]], todos os processos são altamente acoplados e executam como um único serviço. Isso significa que se um processo do aplicativo apresentar um pico de demanda, toda a arquitetura deverá ser escalada. A complexidade da adição ou do aprimoramento de recursos de aplicativos monolíticos aumenta com o crescimento da base de código. Essa complexidade limita a experimentação e dificulta a implementação de novas ideias. As arquiteturas monolíticas aumentam o risco de disponibilidade de aplicativos, pois muitos processos dependentes e altamente acoplados aumentam o impacto da falha de um único processo.

Com uma arquitetura de microsserviços, um aplicativo é criado como componentes independentes que executam cada processo do aplicativo como um serviço. Esses serviços se comunicam por meio de uma interface bem definida usando [[API]]. Os serviços são criados para recursos empresariais e cada serviço realiza uma única função. Como são executados de forma independente, cada serviço pode ser atualizado, implantado e escalado para atender a demanda de funções específicas de um aplicativo.

![monol&iacute;tica vs. microsservi&ccedil;os](https://d1.awsstatic.com/Developer%20Marketing/containers/monolith_1-monolith-microservices.70b547e30e30b013051d58a93a6e35e77408a2a8.png)

### Características dos microsserviços

#### Autônomos
Cada serviço do componente de uma arquitetura de microsserviços pode ser desenvolvido, implantado, operado e escalado sem afetar o funcionamento de outros serviços. Os serviços não precisam compartilhar nenhum código ou implementação com os outros serviços. Todas as comunicações entre componentes individuais ocorrem por meio de [[API]].
#### Especializados
Cada serviço é projetado para ter um conjunto de recursos e é dedicado à solução de um problema específico. 

### Benefícios dos microsserviços

#### Agilidade
Os microsserviços promovem uma organização de equipes pequenas e independentes. As equipes atuam dentro de um contexto pequeno e claramente compreendido e têm autonomia para trabalhar de forma mais independente e rápida. O resultado é a aceleração dos ciclos de desenvolvimento.
#### Escalabilidade flexível
Os microsserviços permitem que cada serviço seja escalado de forma independente para atender à demanda do recurso de aplicativo oferecido por esse serviço. Isso permite serem dimensionados corretamente as necessidades de infraestrutura com precisão e mantenham a disponibilidade quando um serviço experimenta um pico de demanda.  
### Fácil implantação
Os microsserviços permitem a integração e a entrega contínuas, o que facilita o teste de novas ideias e sua reversão caso algo não funcione corretamente. 
#### Liberdade tecnológica
As arquiteturas de microsserviços não seguem uma abordagem generalista. Podendo ser escolhido a melhor ferramenta para resolver problemas específicos.  
#### Código reutilizável
A divisão do software em módulos pequenos e bem definidos permite que as funções sejam usadas para várias finalidades. Um serviço criado para uma determinada função pode ser usado como componente básico para outro recurso. 
#### Resiliência
A independência do serviço aumenta a resistência a falhas do aplicativo. Em uma arquitetura monolítica, a falha de um único componente poderá causar a falha de todo o aplicativo. Com os microsserviços, os aplicativos lidam com a falha total do serviço degradando a funcionalidade, sem interromper todo o aplicativo.