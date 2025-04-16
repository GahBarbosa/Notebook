#### Enunciado
Qual das seguintes alternativas são falsas e quais são verdadeiras? Explique suas respostas. 
##### a. h(n) = 0 é uma heurística admissível para o quebra cabeças de 8 peças. 

**Verdadeiro** — h(n)=0 é admissível (trivial), embora ineficiente.
##### b. Assuma que a torre pode se mover em um tabuleiro de xadrez qualquer quantidade de quadrados em linha reta, verticalmente ou horizontalmente, mas não pode pular sobre as peças. A distância de Manhattan é uma heurística admissível para o problema de movimentar a torre do quadrado A para o B no menor número de movimentos.

Com obstáculos, **a torre não pode pular peças**. Isso significa que o caminho real pode ser **muito maior** do que a estimativa Manhattan — e **a heurística pode subestimar gravemente o custo real**.

**Ainda assim**, isso **não a torna inadmissível**, porque **ela continua não superestimando** o custo real — ela só subestima, o que é permitido em heurísticas admissíveis.