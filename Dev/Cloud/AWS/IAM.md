## O que o IAM faz?

O IAM é um sistema de gerenciamento de segurança centralizado incluído em todas as contas da AWS para controlar o acesso de identidade aos produtos da AWS. Ao anexar políticas de permissão do IAM a identidades, você pode gerenciar quais serviços cada identidade pode acessar e o tipo de ação que a identidade pode executar. As identidades no IAM são usuários, grupos e roles. Selecione cada uma para saber mais sobre elas.
##### Usuário
O usuário do IAM é uma entidade que voce cria na AWS. O usuário do IAM representa a pessoa ou o serviço que usa o usuário do IAM para interagir com a AWS.
##### Grupo
Grupo do IAM é um conjunto de usuários do IAM. Você pode usar grupos de usuários para especificar permissões para um conjunto de usuários, o que pode facilitar o gerenciamento dessas permissões para esses usuários.
##### Role 
Um role do IAM é uma identidade com politicas de permissão anexadas a ela. Um usuário ou serviço do IAM pode assumir essas politicas para obter temporariamente permissões diferentes para um atarefa especifica. 

## Qual problema o IAM soluciona?

O IAM resolve o problema dos usuários que têm maior acesso do que deveriam. O IAM foi projetado para usar o princípio do menor privilégio. Esse princípio prevê que uma identidade não terá acesso a nenhum produto da AWS enquanto você não conceder acesso à identidade. Por esse método, ninguém poderá provisionar ou acessar recursos aos quais você não concedeu acesso explícito.

Por exemplo, se você criar um novo usuário, ele não poderá acessar o painel do [[EC2]] por padrão. Você deve anexar uma política do IAM a esse usuário para lhe conceder acesso ao painel do [[EC2]].

## Como posso usar o IAM?

##### Controle minucioso do acesso
O IAM permite que os usuários controlem o acesso a recursos específicos e [[API]] de produtos da AWS. Você pode usar o IAM para adicionar condições específicas de como um usuário pode usar os recursos da AWS ou o endereço [[IP]] de origem. Essas condições também podem determinar se eles estão usando Secure Sockets Layer ([[SSL]]) ou se eles foram autenticados com um dispositivo de autenticação com multifatorial.
##### Autenticação com multifatorial
Com o IAM, você pode proteger seu ambiente da AWS usando a AWS Multi-Factor Authentication (MFA). A autenticação multifatorial (MFA) é um recurso de segurança disponível sem custo adicional que amplia as credenciais de nome de usuário e senha. A autenticação multifatorial (MFA) exige que os usuários provem a posse física de um [[token]] de hardware de MFA ou dispositivo móvel ativado por MFA por meio da disponibilização de um código de MFA válido.
##### Analisar o acesso
O IAM ajuda você a analisar o acesso em todo ambiente da [[AWS]]. Suas equipes e administradores de segurança podem realizar uma rápida validação para que suas políticas forneçam apenas o acesso público e entre contas aos seus recursos. Você também pode identificar e refinar facilmente suas políticas para permitir o acesso apenas aos serviços que estão sendo usados. Isso ajuda você a adotar da melhor forma o princípio do menor privilégio.
##### Integrar o seu diretório corporativo 
O IAM pode ser usado para conceder acesso federado aos funcionários e às aplicações ao Console de Gerenciamento da [[AWS]] e às [[API]] dos produtos da [[AWS]]. Ele usa seus sistemas de identidade existentes, como o Microsoft Active Directory. Você pode usar qualquer solução de gerenciamento de identidade compatível com o Security Assertion Markup Language ([[SAML]]) 2.0. Você também pode usar um dos exemplos de federação da [[AWS]], como autenticação única (SSO) do Console de Gerenciamento da [[AWS]] ou a federação de [[API]].
## Como posso projetar uma solução de nuvem usando o IAM?

Usando IAM roles, você pode conceder acesso á sua conta a alguém de uma conta da [[AWS]] diferente para que essa pessoa realize uma tarefa especifica.

![[Pasted image 20250313193155.png]]

No diagrama, um usuário na conta Dev esta assumindo um role na conta de produção. O role retorna uma credencial de segurança temporária. Ele concede ao usuário acesso temporário ao produto da [[AWS]] com base na politica anexada ao role.

## Quanto custa o IAM?

O IAM é um recurso oferecido gratuitamente.