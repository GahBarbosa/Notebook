O algoritmo de criptografia Rivest-Shamir-Adleman (RSA) é um algoritmo de criptografia que usa [[Chave Pública Assimétrica]] amplamente utilizado em muitos produtos e serviços. A criptografia assimétrica usa um par de chaves matematicamente vinculado para criptografar e descriptografar dados. 
É considerado dos mais seguros, já que mandou por terra todas as tentativas de quebrá-lo. Foi também o primeiro algoritmo a possibilitar criptografia e assinatura digital.
#### Geração das chaves
No RSA as chaves são geradas desta maneira:

1. Escolha de forma aleatória dois [[Número primo]] grandes , da ordem de $10^{100}$ no mínimo.
2. Calcule $n = p q$
3. Calcule a função [[Função totiente de Euler]] em $\phi(n) = (p-1)(q-1)$
4. Escolha um inteiro $e$ tal que $1 < e < \phi(n)$ , de forma que $e$ e $\phi(n)$ sejam relativamente primos entre si.
5. Calcule $d$ de forma que $de = 1 (mod \phi(n)$, ou seja, $d$ seja o [[inverso multiplicativo]] de $e$ em $(mod \phi(n))$.

Por final temos:

A chave pública: o par $(n, e)$

A chave privada: a tripla $(p, q, d)$. (De fato, para desencriptar, basta guardar $d$ como chave privada, mas os primos $p ,q$ são usados para acelerar os cálculos)

#### Encriptação

Para transformar uma mensagem $m$, onde $1 < m < n - 1$, numa mensagem $c$ cifrada usando a chave pública do destinatário $n$ e $e$ basta fazer uma potenciação modular:

$$ m^e = c \space mod \space n$$

A mensagem então pode ser transmitida em canal inseguro para o receptor. 

#### Decriptação

Para recuperar a mensagem $m$ da mensagem cifrada $c$ usando a respectiva chave privada do receptor $n \space d$, basta fazer outra potenciação modular:

$$ c^d = m \space mod \space n $$