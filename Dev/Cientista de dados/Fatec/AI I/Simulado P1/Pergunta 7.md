#### Enunciado
Suponha um problema que pode ser representado como um espaço de 11 estados (designados pelas letras A até K). Considere o seguinte grafo, que representa os sucessores possíveis para cada estado. Os nodos representam os estados e as arestas o custo para passar de um estado a outro estado. A direção da flecha indica o estado resultante. Por exemplo, é possível atingir o estado H a partir do estado F com um custo de 15. Suponha agora que A é o estado inicial e E o estado final. Responda as seguintes perguntas

![[Pasted image 20250415223953.png]]
#### a) Mostre a árvore de busca em largura e a sequência dos nodos visitados (ordem de visita) 
Expande **nível por nível**.

### **Árvore de busca (níveis):**

1. A
2. B, F, I
3. C (de B), G, H (de F), J (de I)
4. D (de C), E (de G e H), K (de J)
5. E (de K)

> **Ordem de visita dos nós (por nível):**  
> **A, B, F, I, C, G, H, J, D, E, K**

> **Caminho possível encontrado até E:**  
> **A → F → G → E**

(Esse é o primeiro caminho até E que aparece em largura)
#### b) Mostre a árvore de busca em profundidade e a sequência dos nodos visitados (ordem de visita) 
Explora **o caminho mais fundo primeiro**.  
Assumindo que seguimos a ordem das conexões como estão escritas:

### Caminho de exploração:

1. A
2. B
3. C
4. D
5. E → **objetivo alcançado**

> **Ordem de visita:**  
> **A, B, C, D, E**

> **Caminho:**  
> **A → B → C → D → E**
#### c) Explique o que falta para conseguirmos fazer, com o mapa acima, uma busca como a A*
Para aplicar o **algoritmo A***, precisamos de uma **função heurística h(n)** que estime o custo de cada nó até o objetivo **E**.

- Um grafo com **custos nas arestas**  
    ✔️ Temos! Você forneceu os pesos (ex: A → B = 30, etc.).
- Um **estado inicial e um estado objetivo**  
    ✔️ Temos! Inicial = A, Objetivo = E
- Uma **função heurística h(n)** que estima o custo até o objetivo  
    ❌ **Esse é o item que está faltando.**