**Detecção de Fraude em Cartões de Crédito**

Este projeto usa machine learning para identificar transações fraudulentas no dataset creditcard - menor balanceado.csv. O foco é otimizar o modelo para dados desbalanceados usando Seleção de Atributos.

**Bibliotecas**

O script requer pandas, scikit-learn, matplotlib e seaborn.

**Bash**

pip install pandas scikit-learn matplotlib seaborn

**Processo do Código**

Preparação: Os dados são carregados, padronizados (StandardScaler) e divididos em treino/teste (70/30). É usado stratify=y para manter a proporção de fraudes (28%) nos dois conjuntos.

**Seleção de Atributos**

Um RandomForestClassifier inicial é treinado para extrair a importância (feature_importances_) de cada feature. As 15 features mais importantes são selecionadas.

**Modelagem e Avaliação**

Modelo 1: Treinado com todas as 29 features.

Modelo 2: Treinado apenas com as 15 features selecionadas.

Ambos usam class_weight='balanced' para tratar o desbalanceamento.

Análise: Os modelos são comparados usando Acurácia, Macro Avg F1-Score e Matriz de Confusão para provar que o Modelo 2 (mais simples) é tão eficaz quanto o Modelo 1.
