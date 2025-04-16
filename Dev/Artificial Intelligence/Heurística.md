Em algoritmos de busca, uma **heurística** é uma função que estima o **custo restante** (ou a distância) de um determinado estado até o objetivo.

Ela serve como um "palpite inteligente" para guiar a busca de forma mais eficiente, ajudando o algoritmo a priorizar caminhos que **parecem mais promissores**.

---

### Exemplo:

No problema de navegação em um mapa, uma heurística comum é a **distância em linha reta** (distância Euclidiana ou Manhattan) entre o ponto atual e o destino.  
Ela **não garante o caminho real**, mas **ajuda a tomar decisões rápidas e razoáveis** sobre por onde continuar a busca.

---

### Boas heurísticas devem ser:

- **Admissíveis**: nunca superestimam o custo real.
- **Consistentes (ou monótonas)**: a estimativa deve sempre ser menor ou igual ao custo de ir a um vizinho + a heurística do vizinho.