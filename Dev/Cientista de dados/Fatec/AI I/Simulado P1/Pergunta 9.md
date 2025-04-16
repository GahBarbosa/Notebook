#### Enunciado
Assinale V (verdadeiro) ou F (falso) para as seguintes afirmativas:
##### a ( ) Busca é uma técnica da IA que serve para solucionar qualquer problema que possa ser visto como um espaço de busca, isto é, como um conjunto de estados e transições. Porém, em alguns problemas, esse espaço é difícil de ser definido. 
Verdadeiro
##### b ( ) Como a busca de custo uniforme sempre possibilita encontrar a melhor situação possível, ela é a mais usada em implementações práticas. 
**Falso** — Custo uniforme é eficaz, mas pode ser menos eficiente que A* em muitos casos práticos.
##### c ( ) Mesmo que minha implementação de busca em profundidade não cuide da detecção de ciclos, ela sempre consegue chegar a uma resposta, caso exista. 
**Falso** — Pode entrar em ciclos infinitos se não tratá-los.
##### d ( ) Se minha implementação de busca em largura não cuidar em detectar ciclos, ela pode chegar a uma resposta, se existir, caso as limitações de memória não sejam severas. 
**Verdadeiro** — Pode encontrar solução, mas depende da memória.
##### e ( ) Como a busca em largura percorre a árvore de busca nível a nível, ela sempre acha a melhor resposta possível. 
**Verdadeiro** — Busca em largura sempre encontra o caminho mais curto (menor número de passos).
##### f ( ) A busca gananciosa leva em conta somente a função heurística (estimativa de quanto falta para chegar ao estado objetivo) na priorização da expansão dos nós. 
**Verdadeiro** — Busca gananciosa usa só heurística.
##### g ( ) O uso de funções heurísticas amenizam o problema de explosão combinatória dos algoritmos de busca.
**Verdadeiro** — Heurísticas ajudam a reduzir o espaço de busca.