O Protocolo de transferência de hipertexto seguro (HTTPS) é a versão segura do [[HTTP]], que é o principal protocolo usado para enviar dados entre um navegador web e um site. O HTTPS é criptografado para aumentar a segurança da transferência de dados. Isso é particularmente importante quando usuários transmitem dados sensíveis, como quando fazem login em uma conta de banco, serviço de e-mail ou provedor de seguro saúde.

Todos os sites, especialmente os que requerem credenciais de login, devem usar HTTPS.

O HTTPS usa um protocolo de [[Criptografia]] para criptografar as comunicações. O protocolo é chamado de Transport Layer Security ([[TLS]]), embora anteriormente fosse conhecido como Secure Sockets Layer ([[SSL]]). Esse protocolo protege as comunicações usando o que é conhecido como infraestrutura de [[Chave Pública Assimétrica]].

O HTTPS evita que os sites tenham suas informações transmitidas de uma maneira que seja facilmente visualizada por qualquer pessoa que esteja espionando na rede. Quando as informações são enviadas por HTTP normal, as informações são divididas em pacotes de dados que podem ser facilmente “detectados” usando software livre. Isso torna a comunicação em um meio não seguro, como o Wi-Fi público, altamente vulnerável à interceptação. Na verdade, todas as comunicações que ocorrem por HTTP ocorrem em texto não criptografado, tornando-as altamente acessíveis a qualquer pessoa com as ferramentas corretas e vulneráveis a ataques [[On-path]].

Com o HTTPS, o tráfego é criptografado de modo que, mesmo que os pacotes sejam rastreados ou interceptados de outra forma, eles aparecerão como caracteres sem sentido. Vejamos um exemplo:

#### Antes da criptografia:

```
Esta é uma sequência de texto que é completamente legível
```

#### Após a criptografia:

```
ITM0IRyiEhVpa6VnKyExMiEgNveroyWBPlgGyfkflYjDaaFf/Kn3bo3OfghBPDWo6AfSHlNtL8N7ITEwIXc1gU5X73xMsJormzzXlwOyrCs+9XCPk63Y+z0=
```

Em sites sem HTTPS, é possível que provedores de internet (ISPs) ou outros intermediários injetem conteúdo em páginas web sem a aprovação do proprietário do site. Isso geralmente assume a forma de publicidade, onde um provedor que procura aumentar a receita injeta publicidade paga nas páginas web de seus clientes. Sem surpresa, quando isso ocorre, os lucros dos anúncios e o controle de qualidade desses anúncios não são de forma alguma compartilhados com o proprietário do site. O HTTPS elimina a capacidade de terceiros, não moderados, de injetar publicidade no conteúdo da web.

## Qual porta o HTTPS usa?

O HTTPS usa a porta 443. Isso diferencia o HTTPS do [[HTTP]], que usa a porta 80.