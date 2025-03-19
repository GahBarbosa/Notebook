###  O que é:

- O modelo aprende a partir de **exemplos rotulados** (dados + respostas corretas).
- A máquina tenta **prever um rótulo ou valor** baseado nos exemplos que viu.

###  Exemplo:

| Entrada              | Saída esperada                   |
| -------------------- | -------------------------------- |
| Foto de um animal    | "Cachorro"                       |
| Temperatura, umidade | "Vai chover" ou "Não vai chover" |

###  Quando usar:

- Classificação (Spam ou Não Spam)
- Regressão (Previsão de preço de uma casa)

### Classificação com Regressão Logística
```python
from sklearn.datasets import load_iris
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split

# Carregar dataset Iris (flores)
X, y = load_iris(return_X_y=True)

# Dividir em treino e teste
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)

# Treinar o modelo supervisionado
model = LogisticRegression(max_iter=200)
model.fit(X_train, y_train)

# Fazer uma previsão
print(model.predict(X_test[:5]))
```

