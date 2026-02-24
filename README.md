**Enterprise Challenge em parceira com ClickBus**

**Projeto Acadêmico (FIAP Enterprise Challenge) | Grupo 50 - Data Flow**
* **Equipe:** Leticia Mendes Ferreira, Silvielen Maynara Couto, Thales Yoshikawa
* **Parceiro de Negócios:** ClickBus
---

### 1. O Desafio de Negócios

Este projeto foi desenvolvido para resolver três desafios de negócios propostos pela ClickBus, utilizando um conjunto de dados anonimizados de suas operações:

1.  **Decodificando o Comportamento do Cliente:** Segmentar clientes em perfis distintos com base no histórico de compras para direcionar estratégias de Growth (promoções, e-mail marketing, etc.).
2.  **O Timing é Tudo:** Prever se um cliente realizará uma compra nos próximos 7 ou 30 dias (Classificação Binária) e, como extra, prever o número de dias até a próxima compra (Regressão).
3.  **A Estrada à Frente:** Prever qual o trecho (origem-destino) um cliente tem maior probabilidade de comprar em sua próxima viagem (Classificação Multi-classe).

O contexto de negócio é influenciado por fatores sazonais, como feriados e grandes eventos (ex: Carnaval, shows).

### 2. Nossa Solução: Da Análise à IA

Desenvolvemos um pipeline de dados ponta-a-ponta que não apenas resolve os desafios, mas também entrega valor contínuo através de uma plataforma de análise.

* **Análise e Segmentação:** Criamos perfis de clientes (RFM, KPIs, Coorte) para identificar grupos valiosos como "Campeões", "VIPs" e "Em Risco".
* **Modelagem Preditiva:** Treinamos modelos (`HistGradientBoostingClassifier`) para prever *quando* (7/30 dias) e *o quê* (próximo trecho) os clientes comprarão.
* **Visualização Estratégica:** Consolidamos todos os KPIs, segmentos e previsões em um **Dashboard no Grafana**, permitindo o monitoramento em tempo real.
* **Inovação (Extra):** Desenvolvemos um **Chatbot com IA** que consome os dados de predição (vetorizados com `pgvector`) para apoiar a tomada de decisão da equipe de marketing de forma interativa.

<img width="1887" height="728" alt="Image" src="https://github.com/user-attachments/assets/3b7adc02-ff6d-4083-89b2-51b4f72db783" />
<img width="1896" height="654" alt="Image" src="https://github.com/user-attachments/assets/5b6dd860-e095-4922-ba14-bcaa0daabdc8" />

### 3. Stack de Tecnologias

| Área | Tecnologias Utilizadas |
| :--- | :--- |
| **Análise e Modelagem** | Python, Pandas, NumPy, Scikit-learn (`KMeans`, `HistGradientBoostingClassifier`)
| **Engenharia de Dados** | PostgreSQL, PGVector, ETL |
| **Visualização (BI)** | Grafana |
| **IA (Chatbot)** | OpenAI Embeddings, SentenceTransformers  |

### 4. Impacto nos Negócios

A implementação desta solução fornece à ClickBus as ferramentas para:

*  **Aumentar a Receita:** Focando ações de marketing em clientes VIPs e recuperando clientes "Em Risco" (Meta: +15% na taxa de recompra).
*  **Reduzir Custos:** Diminuindo o desperdício com campanhas genéricas e focando em públicos com maior potencial de conversão.
*  **Aumentar a Satisfação do Cliente:** Enviando ofertas relevantes e personalizadas no *timing* correto (Meta: +20 pontos no NPS).

  
