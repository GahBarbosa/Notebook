### **Responsabilidade:**  
Colocar o modelo treinado em produção, tornando-o acessível para fazer previsões com dados reais em tempo de execução.

### **Técnicas utilizadas:**

- Serialização do modelo (pickle, joblib)
- Disponibilização via API (Flask, FastAPI)
- Criação de pipeline de CI/CD para reimplantar o modelo
- Monitoramento de latência e throughput

### **Exemplos práticos:**

- Disponibilizar um modelo preditivo de churn via API REST para o time de negócios
- Embutir um modelo de recomendação em um sistema de e-commerce