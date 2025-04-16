Tratando-se de machine learning, você pode utilizar algoritmos de treinamento como ajuda para realizar tarefas empíricas que demandam algum tipo de inferência indutiva. Esse objetivo envolve indução porque utiliza dados para treinar algoritmos para fazer inferências generalizáveis. Assim, os algoritmos podem fazer previsões ou decisões estatisticamente confiáveis, ou concluir outras tarefas, quando aplicarem novos dados que não foram utilizados para treiná-los. Um algoritmo treinado por algoritmos identifica padrões em seus dados sem que sejam necessárias regras explícitas definidas manualmente.

Os **algoritmos de treinamento** podem ser classificados principalmente em **três tipos** com base no tipo de tarefa que realizam: aprendizado [[Supervisionado]], aprendizado [[Não Supervisionado]] e aprendizado por [[Reforço]]. Dentro de cada uma dessas categorias, existem diversos tipos de algoritmos que você pode usar, dependendo do problema em questão.

### 1. **Aprendizado Supervisionado (Supervised Learning)**

No aprendizado supervisionado, o modelo é treinado usando um conjunto de dados rotulado, ou seja, os dados de entrada vêm com a resposta esperada (rótulos). O objetivo do modelo é aprender a mapear entradas para as saídas corretas.

#### Tipos de Algoritmos Supervisionados:

- **Regressão**: Usada para prever valores contínuos.
    - [[Regressão Linear]] (Linear Regression)
    - [[Regressão Polinomial]] (Polynomial Regression)
    - [[Regressão Lasso e Ridge]]
    
- **Classificação**: Usada para prever categorias ou classes.
    - [[Árvore de Decisão]] (Decision Tree)
    - [[Máquinas de Vetores de Suporte]] (SVM)*(Support Vector Machine)
    - k-Vizinhos Mais Próximos ([[KNN]])
    - [[Redes Neurais]] (Artificial Neural Networks)
    - [[Naive Bayes]]
    - [[Random Forest]]
    - [[Gradient Boosting]] (XGBoost, LightGBM)

### 2. **Aprendizado Não Supervisionado (Unsupervised Learning)**

No aprendizado não supervisionado, o modelo é treinado com dados sem rótulos, ou seja, sem respostas esperadas. O objetivo é identificar padrões ou estruturas dentro dos dados.

#### Tipos de Algoritmos Não Supervisionados:

- **Clustering (Agrupamento)**: Agrupa os dados em clusters (grupos) baseados em características semelhantes.
    - **K-means**
    - **DBSCAN**
    - **Algoritmos Hierárquicos (Hierarchical Clustering)**
    
- **Redução de Dimensionalidade**: Reduz a quantidade de variáveis em um dataset para destacar os padrões mais importantes.
    - **PCA (Principal Component Analysis)**
    - **t-SNE (t-Distributed Stochastic Neighbor Embedding)**
    - **LDA (Linear Discriminant Analysis)**
    
- **Modelos de Mistura**: Usados para modelar distribuições de probabilidade.
    - **Gaussian Mixture Models (GMM)**

### 3. **Aprendizado por Reforço (Reinforcement Learning)**

No aprendizado por reforço, o modelo aprende interagindo com o ambiente. Ele toma ações e recebe recompensas ou punições baseadas nas suas escolhas. O objetivo é maximizar a recompensa total ao longo do tempo.

#### Tipos de Algoritmos de Reforço:
- **Q-learning**
- **Deep Q Networks (DQN)**
- **Algoritmos de Políticas (Policy-based algorithms)**
- **Algoritmos Actor-Critic**
- **Proximal Policy Optimization (PPO)**