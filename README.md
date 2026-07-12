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

# 🔎 Pipeline do Projeto

``` text
Análise Exploratória
        ↓
Pré-processamento
        ↓
Padronização
        ↓
Balanceamento das Classes
        ↓
Random Forest
        ↓
XGBoost
        ↓
Avaliação
        ↓
Threshold de Decisão
        ↓
Conclusões
```

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

# 🚀 Principais Resultados

-   Comparação entre Random Forest e XGBoost;
-   Avaliação de estratégias de balanceamento;
-   Estudo do threshold de decisão;
-   Interpretação das métricas sob a perspectiva do negócio.

------------------------------------------------------------------------

# 🛠 Tecnologias Utilizadas

Python • Pandas • NumPy • Matplotlib • Seaborn • Scikit-learn • XGBoost
• Imbalanced-learn • Jupyter Notebook • Git • GitHub

------------------------------------------------------------------------

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

Cientista de Dados

GitHub \| LinkedIn
