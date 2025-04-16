### Enunciado
O seu chefe quer desenvolver um sistema de logística para a empresa. Como ele ouviu dizer que você estuda Inteligência Artificial, ele decidiu designar a você a tarefa de projetar um sistema que encontre o menor caminho entre 2 pontos na cidade de São Paulo. Pede-se: 
#### a) Que informações (base de dados) seu sistema precisaria? Que campos essa base de dados deveria possuir? Descreva clara e objetivamente; respostas genéricas não servirão. 

- **Nós (interseções):**
    - ID do ponto
    - Coordenadas geográficas (latitude, longitude)
- **Arestas (ruas/conexões):**
    - ID do ponto de origem
    - ID do ponto de destino
    - Distância ou tempo estimado de deslocamento
    - Sentido (mão única ou dupla)

#### b) Que algoritmo você escolheria para tal função? Faça comentários sobre o desempenho computacional de tal algoritmo (poderia rodar num servidor e atender a várias requisições on-line?). 

Algoritmo escolhido Busca A* (A estrela)

- **Vantagens:** Combina o melhor da UCS (custo real) e da busca gananciosa (heurística).  Usa a função: `f(n) = g(n) + h(n)` Onde:
    
    - `g(n)` = custo do início até o nó atual
    - `h(n)` = estimativa do custo até o destino (heurística)

- **Desempenho:** Muito eficiente, especialmente com heurísticas (como distância euclidiana, tempo estimado de trajeto etc.)

O algoritmo A* apresenta um desempenho computacional muito eficiente. Por combinar o custo real acumulado com uma estimativa do custo restante até o destino, ele reduz significativamente o número de caminhos explorados em comparação a algoritmos cegos, como a busca de custo uniforme. Com a utilização de estruturas de dados otimizadas (como filas de prioridade) e técnicas de cache ou pré-processamento de rotas, é totalmente viável atender múltiplas requisições online com alta performance e baixo tempo de resposta.
#### c) Faça uma pequena simulação, passo-a-passo, para convencer seu chefe da viabilidade de seu projeto

**Simulação simplificada:** Suponha 4 pontos: A, B, C, D com conexões:
- A → B (2)
- A → C (4)
- B → D (7)
- C → D (1)

Heurística para D:
- h(A) = 5
- h(B) = 6
- h(C) = 2
- h(D) = 0

Rodando A*, caminho ótimo:  
A → C (4) + h(C)=2 → D (1) → total = 5 + 1 = 6