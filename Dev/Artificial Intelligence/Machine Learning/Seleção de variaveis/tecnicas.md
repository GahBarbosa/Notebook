## 🔎 **1. Seleção Univariada (Ex: SelectKBest)**

Seleciona as melhores variáveis baseado em testes estatísticos independentes, como ANOVA, chi-quadrado ou correlação.

|✅ **Prós**|❌ **Contras**|
|---|---|
|Simples e rápida de aplicar|Avalia cada variável **isoladamente** (ignora interações)|
|Ajuda a eliminar variáveis irrelevantes cedo|Pode descartar variáveis que, combinadas, são importantes|
|Boa para datasets muito grandes|Limitação em casos de não-linearidade|

---

## 🔎 **2. Recursive Feature Elimination (RFE)**

Treina o modelo várias vezes removendo as menos importantes a cada rodada.

|✅ **Prós**|❌ **Contras**|
|---|---|
|Considera **interação entre variáveis**|Computacionalmente **pesado** em datasets grandes|
|Oferece um ranking de importância|Pode superestimar variáveis que o modelo escolhido favorece|
|Funciona bem com modelos lineares e não lineares|Sensível ao **overfitting** se não usado com validação cruzada|

---

## 🔎 **3. Feature Importance (Ex: Random Forest, XGBoost)**

Usa algoritmos de árvore para calcular a importância de cada variável durante o treinamento.

|✅ **Prós**|❌ **Contras**|
|---|---|
|Considera relações não-lineares e interações|Importância pode ser **enviesada** por variáveis categóricas com muitos níveis|
|Boa performance com grandes conjuntos de dados|Difícil interpretar a influência real de cada variável|
|Funciona direto com o modelo|Nem sempre a importância reflete impacto direto no target|

---

## 🔎 **4. Lasso (Regularização L1)**

Modelo de regressão linear com penalização que força coeficientes de variáveis menos relevantes a zero.

|✅ **Prós**|❌ **Contras**|
|---|---|
|Faz **seleção automática** de variáveis|Funciona só com **modelos lineares**|
|Reduz overfitting|Pode eliminar variáveis que, combinadas, são relevantes|
|Simples de implementar|Sensível a escala dos dados (requer normalização)|

---

## 🔎 **Resumo: Qual usar e quando?**

|Cenário|Melhor Opção|
|---|---|
|Dataset pequeno e linear|Lasso ou RFE|
|Dataset grande com muitas variáveis irrelevantes|SelectKBest ou Feature Importance|
|Muitos dados e busca de interações|Random Forest / XGBoost (Feature Importance)|
|Alta performance sem preocupação com explicação|Tree-based models ou RFE|

---

Se quiser, posso montar um fluxo ou te indicar a melhor técnica pro seu caso. Qual o tamanho do seu dataset e você pretende focar em modelos lineares ou de árvore?