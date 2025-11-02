Projeto: Predição de cancelamento de planos em clientes de Telecom

Descrição do Problema
O objetivo deste projeto é prever se um cliente de uma empresa de telecomunicações irá cancelar seu serviço (churn). A identificação precoce de clientes propensos ao cancelamento é essencial para reduzir perdas e orientar estratégias de retenção.

Base de Dados
A base utilizada foi o Telco Customer Churn Dataset, disponibilizado pela IBM no Kaggle: https://www.kaggle.com/datasets/blastchar/telco-customer-churn

Metodologia
O processo envolveu as etapas de:

Análise exploratória e limpeza dos dados
Pré-processamento com Pipeline e ColumnTransformer
Balanceamento de classes com SMOTE
Normalização e redução de dimensionalidade com TruncatedSVD
Treinamento e validação com diversos modelos (KNN, Decision Tree, Random Forest, XGBoost, Naive Bayes)
Fine tuning de hiperparâmetros do XGBoost

Conclusão
Apesar do fine tuning e das técnicas de balanceamento, padronização e redução de dimensionalidade aplicadas para melhorar a generalização e evitar overfitting, o modelo final (XGBoost) apresentou alto desempenho em treino e validação, mas fracassou em generalizar nos dados de teste, classificando quase todos os clientes como não canceladores. Isso indica que o modelo não foi capaz de identificar corretamente os clientes que cancelam, possivelmente devido a ruído, desbalanceamento residual ou dependência excessiva de variáveis categóricas codificadas.
