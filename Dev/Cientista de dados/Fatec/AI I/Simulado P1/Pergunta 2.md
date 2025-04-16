#### Enunciado
Suponha um problema que pode ser representado como um espaço de 9 estados (designados pelas letras A até K). Considere o seguinte grafo, que representa os sucessores possíveis para cada estado
Os nodos representam os estados e as arestas o custo para passar de um estado a outro estado. A di reção da flecha indica o estado resultante. Por exemplo, é possível atingir o estado A a partir do estado G com um custo de 10. Suponha agora que G é o estado inicial e K o estado final. Mostre a árvore de busca e a sequência dos nodos visitados (ordem de visita) em cada uma das seguintes buscas:

![[Pasted image 20250415224344.png]]

```python
# Considerando-se o destino K 
h['A' ] = 28 
h['B' ] = 10 
h['C' ] = 19 
h['D' ] = 14 
h['E' ] = 10 
h['F' ] = 13 
h['G' ] = 23 
h['H' ] = 20 
h['K' ] = 0
```
#### a) Busca em largura (BFS)
**Expansão por nível (sem considerar custo):**

1. G
2. A, C
3. D, B, H (de A), D (de C)
4. G (de D), E (de D), F (de B), K (de H) ← Chegamos no objetivo aqui.

✔️ **Caminho encontrado:**  
G → A → H → K
#### b) Busca em profundidade (DFS)
**Explora o mais fundo possível antes de voltar.**

1. G
2. A
3. D
4. G
5. A (revisitado), volta
6. E
7. A (revisitado), volta
8. C
9. D (revisitado), volta
10. K ← objetivo encontrado!

✔️ **Caminho possível:**  
G → A → D → E → K  
(_Pode variar conforme a ordem dos filhos_)
#### c) Busca com Custo Uniforme (cega).
**Expande sempre o nó de menor custo acumulado.**

Vamos manter a tabela `g(n)` com o custo do caminho do início até o nó:

- G (0)
- G → C (5)
- G → C → D (5 + 5 = 10)
- G → C → D → E (15)
- G → C → D → E → K (25)

✔️ **Caminho de menor custo:**  
G → C → D → E → K  
**Custo total:** 25
#### d) Busca Gananciosa (heurística).
**Expande sempre o nó com menor heurística `h(n)` (não considera o custo real `g(n)`).**

Ordem das heurísticas:

- G (23)  
    → A (28), C (19)  
    → C tem menor h, então expande C  
    → D (14)  
    → E (10)  
    → K (0) ← melhor heurística

✔️ **Caminho possível:**  
G → C → D → E → K

📝 _Não garante o menor custo total, mas é rápida._
#### e) Busca A* (`f(n) = g(n) + h(n)`)

Calculamos os custos acumulados + heurística estimada:
1. G → C (g=5, h=19) → f=24
2. C → D (g=10, h=14) → f=24
3. D → E (g=15, h=10) → f=25
4. E → K (g=25, h=0) → f=25

✔️ **Caminho ótimo:**  
G → C → D → E → K  
**Custo total real:** 25  
**f(K) = 25**


## Resumo dos Caminhos Encontrados

|Algoritmo|Caminho Encontrado|Custo Total|
|---|---|---|
|**BFS**|G → A → H → K|30|
|**DFS**|G → A → D → E → K|25|
|**UCS**|G → C → D → E → K|25 ✅|
|**Gananciosa**|G → C → D → E → K|25*|
|**A***|G → C → D → E → K|25 ✅|

> _Nota: Gananciosa achou o mesmo caminho que A* e UCS nesse caso, mas isso não é garantido em geral._