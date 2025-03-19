#Fazer
Em **Machine Learning**, as **classificações** geralmente se referem a tarefas em que o modelo aprende a **atribuir rótulos** (ou classes) a dados de entrada. Existem alguns **tipos principais de problemas de classificação**, que variam de acordo com a quantidade de classes e a forma como o modelo deve lidar com elas:

---

## ✅ **1. Classificação Binária**

- **Definição:** Existem apenas **duas classes** possíveis para cada entrada.
- **Exemplos:**
    - Spam ou Não Spam (em e-mails)
    - Doente ou Saudável
    - Aprovado ou Reprovado
- **Técnicas comuns:** Regressão logística, SVM, Árvores de Decisão.

---

## ✅ **2. Classificação Multiclasse**

- **Definição:** Existem **mais de duas classes** e cada amostra só pode pertencer a **uma única classe**.
- **Exemplos:**
    - Classificar tipos de flores (Iris Setosa, Versicolor, Virginica)
    - Reconhecimento de dígitos (0 a 9)
- **Técnicas comuns:** Redes Neurais, Random Forest, KNN.

---

## ✅ **3. Classificação Multirrótulo (Multi-label)**

- **Definição:** Uma mesma entrada pode ter **mais de um rótulo associado**.
- **Exemplos:**
    - Tags de um vídeo ou artigo (Tecnologia, Esportes, Política ao mesmo tempo)
    - Diagnóstico médico com múltiplas doenças
- **Técnicas comuns:** Redes Neurais, Classificadores binários independentes por rótulo.

---

## ✅ **4. Classificação Hierárquica**

- **Definição:** As classes possuem uma **relação de hierarquia** ou estrutura de árvore.
- **Exemplos:**
    - Classificação de produtos: Eletrônicos → Computadores → Notebooks
    - Classificação biológica: Reino → Filo → Classe → Ordem
- **Técnicas comuns:** Árvores de decisão adaptadas, Redes neurais com múltiplas saídas hierárquicas.

---

## ✅ **5. Classificação Imbalanceada (Desequilibrada)**

- **Definição:** Quando uma ou mais classes têm **muito menos exemplos** que as outras, o que dificulta o treinamento.
- **Exemplos:**
    - Detecção de fraudes
    - Diagnóstico de doenças raras
- **Técnicas comuns:** Oversampling, Undersampling, SMOTE.

---

## 🎯 **Resumo Visual**

|Tipo|Característica Principal|Exemplo|
|---|---|---|
|Binária|2 classes|Spam ou Não Spam|
|Multiclasse|+2 classes, 1 rótulo por amostra|Reconhecimento de dígitos|
|Multirrótulo|+2 classes, múltiplos rótulos por amostra|Tags de um vídeo|
|Hierárquica|Classes organizadas em hierarquia|Classificação de produtos|
|Imbalanceada|Classes com distribuição muito desigual|Fraude bancária|

---

Quer que eu te explique algum tipo em mais detalhes ou te ajude a montar um exemplo prático?