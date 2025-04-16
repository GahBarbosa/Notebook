#### Enunciado
Fornecemos duas heurísticas simples para o quebra cabeças de 8 peças: a quantidade de peças fora de lugar (H1) e a distância Manhattan (H2). Se usarmos o algoritmo A* para resolver o quebra cabeças com cada uma das heurísticas, ele achará a melhor resposta nas duas situações (com H1 e com H2)? Em outras palavras, essas heurísticas são admissíveis? Dê argumentos tanto pelo sim quanto o não.

#### Resposta
- **H1 (peças fora do lugar):** admissível, pois nunca superestima o custo real.
- **H2 (distância Manhattan):** também admissível.
- Ambas são **ótimas para A***, embora H2 seja geralmente mais informativa e eficiente, pois distingue melhor os estados.