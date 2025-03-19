### O que é:

- O modelo recebe **somente os dados de entrada, sem rótulos**.
- O objetivo é **encontrar padrões, agrupamentos ou estruturas ocultas**.

### Exemplo:

|Entrada|Saída (não existe um rótulo)|
|---|---|
|Dados de compras de clientes|Grupos de clientes semelhantes (cluster)|

### Quando usar:

- Agrupamento de clientes
- Redução de dimensionalidade
- Análise de padrões

## **Agrupamento (Clustering) com KMeans**
```python
from sklearn.datasets import load_iris
from sklearn.cluster import KMeans

# Carregar dataset Iris (sem usar os rótulos)
X, _ = load_iris(return_X_y=True)

# Aplicar KMeans para encontrar 3 grupos
kmeans = KMeans(n_clusters=3, random_state=0)
kmeans.fit(X)

# Mostrar a qual cluster pertence cada flor
print(kmeans.labels_[:5])
```