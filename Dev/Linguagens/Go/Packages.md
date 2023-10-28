 Os programas [[Go]] são organizados em pacotes. Um pacote é uma coleção de arquivos de origem no mesmo diretório que são compilados juntos. Funções, tipos, variáveis ​​e constantes definidas em um arquivo de origem são visíveis para todos os outros arquivos de origem do mesmo pacote.

Os pacotes permitem a reutilização, permitindo que você use seus próprios pacotes ou outros pacotes em seu código.

Por exemplo: Se você tiver um código que faz alguns cálculos para estatísticas e está sendo usado por mais de um código em seu programa, você colocaria esse código de cálculo em um pacote separado, talvez denominado como: estatísticas.

Qualquer código escrito em Go pertence a um pacote.
Os programas Go são compostos de um ou mais pacotes_._

Um pacote representa um único conceito.
Então, eles não são genéricos como: comum, utilitário, auxiliar etc. Eles são mais como: http, json, xml, crypto, fmt. Portanto, você não deve colocar nenhum código além do propósito exclusivo do pacote, e é importante nomear os pacotes de forma adequada.

A nomeação de um pacote acontece na primeira linha do arquivo, por exemplo:
```go
package main
```

Um pacote pode ser usado por outros pacotes.
E, claro, um pacote pode usar suas próprias funcionalidades, algumas das quais não estão disponíveis para outros pacotes e outras estão disponíveis apenas para o próprio pacote.

Um pacote importado apenas uma vez.
Você pode importar o mesmo pacote em vários pacotes e ele será importado apenas uma vez.