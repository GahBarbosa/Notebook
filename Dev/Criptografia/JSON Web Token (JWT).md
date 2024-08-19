[Repositório com exemplos](https://github.com/GahBarbosa/Jwt-Node-PostgreSQL)

É um padrão (RFC 7519) que define uma maneira compacta e independente de transmitir informações com segurança entre as partes como um objeto JSON. Os JWTs podem ser assinados usando um segredo (com o algoritmo HMAC) ou um par de chaves pública/privada usando RSA ou ECDSA.

O JSON Web Token consiste em três partes separadas por pontos, que são Header, Payload, Signature, um JWT geralmente se parece com o seguinte:
```
 xxxxx.aaaa.zzzzz
```
## Header 
O cabeçalho geralmente consiste em duas partes: o tipo do token, que é JWT, e o algoritmo de assinatura usado, como HMAC SHA256 ou RSA. Examplo:
```json
{ "alg": "HS256", "tipo": "JWT" }
```
## Payload
A segunda parte do token, que contém as declarações são sobre uma entidade (normalmente, o usuário) e dados adicionais. Existem três tipos de reivindicações:  registradas, públicas e privadas
- Registradas: são um conjunto predefinido que não são obrigatórias, mas recomendadas, Alguns deles são: iss (emissor), exp (tempo de expiração), sub (assunto), aud (público)
- Públicas: podem ser definidas à vontade por aqueles que usam JWTs. Mas para evitar conflitos, eles devem ser utilizadas no padrão [IANA JSON Web Token Registry](https://www.iana.org/assignments/jwt/jwt.xhtml) 
- Privadas: criadas para compartilhar informações entre as partes que concordam em usá-las e não são reivindicações registradas ou públicas.
```json
{ "sub": "1234567890", "name": "John Doe", "admin": true }
```

## Signature
Para criar a parte da assinatura, você deve pegar o Header codificado, o Payload codificada, um segredo, o algoritmo especificado no cabeçalho e assiná-lo.
Por exemplo, se você deseja usar o algoritmo HMAC SHA256, a assinatura será criada da seguinte maneira:
```js
HMACSHA256( base64UrlEncode(header) + "." + base64UrlEncode(payload), secret)
```
O resultado são três Strings em Base64-URL separadas por pontos:
```
eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c
```

