Um modelo de machine learning é o algoritmo treinado que é utilizado para identificar padrões nos seus dados. Um modelo é treinado a partir do processo de machine learning, e ele captura e armazena padrões. Quanto mais padrões um modelo armazenar, maior ele será. O tamanho de modelos de machine learning é geralmente descrito em megabytes. O propósito de um modelo é prever os resultados de novas entradas de dados com base em padrões observados previamente

Existem 3 tipos de modelos:
- [[Supervisionado]]
- [[Não Supervisionado]]
- [[Reforço]]

### Exemplo de um modelo
```python 
# Importando as bibliotecas
from sklearn.linear_model import LogisticRegression
import numpy as np

# Dados de exemplo (Temperatura em graus Celsius)
# X são as temperaturas
X = np.array([[10], [15], [20], [25], [30], [35]])
# y é a preferência (0 = Não gosta, 1 = Gosta)
y = np.array([0, 0, 1, 1, 1, 0])

# Criando o modelo de Regressão Logística
modelo = LogisticRegression()

# Treinando o modelo
modelo.fit(X, y)

# Fazendo uma previsão: pessoa gosta de sorvete se estiver 22°C?
temperatura_teste = np.array([[22]])
previsao = modelo.predict(temperatura_teste)

print(f'Previsão (1 = Gosta, 0 = Não gosta): {previsao[0]}')
```

