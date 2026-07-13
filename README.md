# 🛡️ Credit Card Fraud Detection

## Machine Learning aplicado à detecção de fraudes em cartões de crédito

------------------------------------------------------------------------

# 📌 Contexto do Problema

Fraudes em cartões de crédito representam um dos maiores desafios
enfrentados por instituições financeiras, gerando perdas financeiras e
afetando a experiência dos clientes.

Este projeto utiliza técnicas de Ciência de Dados e Machine Learning
para detectar transações fraudulentas, buscando equilibrar dois
objetivos fundamentais:

-   Detectar o maior número possível de fraudes (alto Recall);
-   Reduzir bloqueios indevidos de clientes legítimos (alta Precision).

------------------------------------------------------------------------

# 🎯 Objetivo

Desenvolver e comparar modelos supervisionados para classificação de
transações financeiras em **fraudulentas** ou **legítimas**, avaliando
técnicas de balanceamento de classes e o impacto do **threshold de
decisão** nas métricas de desempenho.

------------------------------------------------------------------------

# 📂 Dataset

O conjunto de dados contém transações de cartões de crédito previamente
anonimizadas.

  Característica            Valor
  --------------------- ---------
  Total de transações     284.807
  Fraudes                     492
  Não fraudes             284.315
  Variáveis                    30
  Variável alvo             Class

------------------------------------------------------------------------

## 🧪 Metodologia

1. **Análise Exploratória (EDA)** — distribuição das classes, correlação com o
   alvo, distribuições de `Amount`/`Time`
2. **Pré-processamento** — remoção de duplicatas, padronização (`StandardScaler`)
   de `Amount`/`Time`, split treino/teste estratificado
3. **Balanceamento** — comparação entre `class_weight='balanced'`, `SMOTE` e
   `RandomUnderSampler`, sempre aplicados apenas ao treino
4. **Modelagem** — Regressão Logística (baseline), Random Forest e XGBoost,
   com `RandomizedSearchCV` + validação cruzada estratificada, otimizando
   `average_precision` (AUC-PR)
5. **Avaliação** — Precision, Recall, F1, AUC-PR, curva Precision-Recall e
   escolha de threshold
6. **Interpretação** — variáveis mais relevantes e recomendação de negócio

------------------------------------------------------------------------

# 📊 Análise Exploratória

Foram investigados:

-   Distribuição das classes;
-   Correlações entre variáveis;
-   Distribuição dos valores monetários;
-   Desbalanceamento do conjunto de dados.

------------------------------------------------------------------------

# ⚙️ Pré-processamento

-   StandardScaler
-   Divisão treino/teste
-   Balanceamento das classes
-   Preparação para modelagem

------------------------------------------------------------------------

# 🤖 Modelagem

Modelos desenvolvidos:

-   Random Forest
-   XGBoost
-   Logistic Regression

------------------------------------------------------------------------

# 📈 Avaliação dos Modelos

Métricas utilizadas:

-   Accuracy
-   Precision
-   Recall
-   F1-score
-   ROC-AUC
-   Matriz de Confusão

------------------------------------------------------------------------

# 🎯 Análise do Threshold de Decisão

Além das métricas tradicionais, foi realizada uma análise do impacto do
**threshold de decisão** sobre Precision, Recall e F1-score.

O melhor desempenho foi obtido com:

-   **Threshold:** 0,753
-   **Precision:** 98,67%
-   **Recall:** 77,89%
-   **F1-score:** 87,06%

Essa análise demonstra que o threshold padrão (0,5) nem sempre
representa a melhor estratégia para aplicações reais de detecção de
fraudes.

------------------------------------------------------------------------

# 💼 Aplicação em Negócio

O modelo pode apoiar instituições financeiras em:

-   Detecção de fraudes em tempo real;
-   Redução de perdas financeiras;
-   Diminuição de falsos positivos;
-   Apoio às equipes antifraude.

------------------------------------------------------------------------

## 🏆 Resultado

| Modelo | Precision | Recall | F1-Score | AUC-PR |
|---|---|---|---|---|
| **XGBoost (baseline)** | **0,9487** | 0,7789 | **0,8555** | **0,8277** |
| XGBoost (tuned) | 0,7333 | 0,8105 | 0,7700 | 0,8181 |
| Random Forest (tuned) | 0,9855 | 0,7158 | 0,8293 | 0,8136 |
| Random Forest (baseline) | 0,9857 | 0,7263 | 0,8364 | 0,8065 |
| Regressão Logística (baseline) | 0,8485 | 0,5895 | 0,6957 | 0,6935 |

**Modelo recomendado:** XGBoost com hiperparâmetros padrão. Um achado
interessante do projeto é que o tuning de hiperparâmetros **não** superou o
modelo baseline — atribuído à alta variância da validação cruzada quando há
poucos exemplos da classe minoritária (~394 fraudes no treino).

------------------------------------------------------------------------

# 🛠 Tecnologias Utilizadas

Python • Pandas • NumPy • Matplotlib • Seaborn • Scikit-learn • XGBoost
• Imbalanced-learn • Jupyter Notebook • Git • GitHub

------------------------------------------------------------------------
## 📌 Limitações

- Dataset de 2013 (cartões europeus) — padrões de fraude evoluem com o tempo
- Variáveis PCA-anônimas limitam a explicabilidade individual das decisões
- Ausência de teste em ambiente de produção real (volume/latência)

# 📁 Estrutura do Projeto

``` text
credit-card-fraud-detection/
│
├── images/
├── notebooks/
├── README.md
├── requirements.txt
└── .gitignore
```


------------------------------------------------------------------------

# 👨‍💻 Autor

**Marcos Vinícius**

Projeto de Conclusão de Curso/Cientista de Dados

GitHub \| LinkedIn
