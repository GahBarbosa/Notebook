Prometheus é uma solução de monitoramento e alertas que coleta e armazena métricas como séries temporais, com uma forte ênfase na simplicidade e facilidade de uso. Foi desenvolvido inicialmente pela SoundCloud e agora é um projeto da Cloud Native Computing Foundation (CNCF).

### **Como o Prometheus Funciona?**

1. **Coleta de Métricas:**
    
    - **Scraping:** O Prometheus coleta métricas de endpoints HTTP expostos por serviços e aplicativos. Esses endpoints geralmente fornecem métricas no formato Prometheus, que é uma linguagem de consulta específica para séries temporais.
    - **Pull Model:** Em vez de os aplicativos enviarem métricas para o Prometheus, o Prometheus periodicamente "puxa" ou "scrape" as métricas dos endpoints expostos.
2. **Formato de Métricas:**
    
    - As métricas são expostas em um formato de texto simples que o Prometheus pode entender. Cada métrica é identificada por um nome e pode ter rótulos (labels) que fornecem contexto adicional.
    - Exemplo de métrica:
        
        ```lua
		http_requests_total{method="POST", status="200"} 1027
```
        
3. **Armazenamento de Séries Temporais:**
    
    - O Prometheus armazena as métricas coletadas como séries temporais. Cada série é identificada por um nome e um conjunto de rótulos.
    - Ele utiliza um banco de dados de séries temporais em memória, com suporte para armazenamento local e em disco.
4. **Consultas e Visualização:**
    
    - **PromQL:** Prometheus utiliza uma linguagem de consulta chamada PromQL (Prometheus Query Language) para acessar e manipular dados de métricas.
    - **Visualização:** Prometheus não possui uma interface de visualização embutida, mas é frequentemente usado em conjunto com ferramentas como Grafana para criar painéis de visualização e gráficos.
5. **Alertas:**
    
    - O Prometheus possui um componente de alerta chamado Alertmanager. Ele gerencia e envia notificações baseadas em regras de alerta definidas.
    - As regras de alerta são definidas em Prometheus usando PromQL e especificam condições que, quando atendidas, disparam alertas.
6. **Arquitetura:**
    
    - **Serviço de Scraping:** O Prometheus é configurado para coletar métricas de vários endpoints HTTP.
    - **Banco de Dados:** Armazena as métricas como séries temporais com um modelo de dados eficiente.
    - **PromQL:** A linguagem de consulta usada para acessar e consultar as métricas armazenadas.
    - **Alertmanager:** Gerencia alertas e notifica equipes por e-mail, Slack, ou outras integrações.

### **Arquitetura Básica do Prometheus**

1. **Prometheus Server:** Faz o scraping dos endpoints e armazena as métricas.
2. **Exporters:** Programas ou bibliotecas que expõem métricas para o Prometheus. Por exemplo, o **Node Exporter** coleta métricas do sistema operacional.
3. **Alertmanager:** Gerencia e envia alertas baseados em regras definidas.
4. **Grafana:** Usado para criar painéis de visualização baseados em dados do Prometheus.

### **Benefícios do Prometheus:**

- **Flexibilidade e Escalabilidade:** Pode ser facilmente escalado e adaptado para diferentes necessidades.
- **Modelo de Dados Eficiente:** Utiliza um modelo de dados de séries temporais que é eficiente para consultas e armazenamento.
- **Consulta Poderosa:** PromQL permite consultas complexas e agregações de dados.
- **Foco na Simplicidade:** Design minimalista que facilita a configuração e o uso.

Prometheus é ideal para monitorar ambientes dinâmicos e escaláveis, especialmente aqueles que usam microservices e contêineres. Ele é amplamente adotado em ambientes de Kubernetes e outras arquiteturas baseadas em nuvem.