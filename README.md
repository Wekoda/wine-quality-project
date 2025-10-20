# Classificação Multiclasse da Qualidade de Vinhos (Random Forest)

## 🍷 Visão Geral do Projeto

Este projeto tem como objetivo principal desenvolver um modelo de Machine Learning capaz de **prever a pontuação de qualidade de vinhos tintos** (variável `quality`). A tarefa é tratada como um problema de **classificação multiclasse**, utilizando o algoritmo **Random Forest**.

O modelo explora as características físico-químicas do vinho para entender quais fatores mais influenciam a percepção de sua qualidade sensorial.

## 💾 Fonte de Dados

O projeto utiliza o conjunto de dados **Wine Quality Red**, que contém 11 atributos de entrada e uma variável de saída (target).

### Variáveis (Features)

* `fixed acidity`: acidez fixa
* `volatile acidity`: acidez volátil
* `citric acid`: ácido cítrico
* `residual sugar`: açúcar residual
* `chlorides`: cloretos
* `free sulfur dioxide`: dióxido de enxofre livre
* `total sulfur dioxide`: dióxido de enxofre total
* `density`: densidade
* `pH`: nível de pH
* `sulphates`: sulfatos
* `alcohol`: teor alcoólico

### Variável Target

* `quality`: Pontuação do vinho (variando de 3 a 8 no dataset utilizado).

## 🛠️ Metodologia e Desenvolvimento

O desenvolvimento do projeto seguiu as seguintes etapas:

1.  **Pré-processamento e Análise Exploratória (EDA):**
    * Verificação de tipos de dados e tratamento de valores nulos (nenhum dado faltante encontrado).
    * Análise estatística descritiva (`.describe()`) para identificação de *outliers* e distribuição de dados.
    * Análise do balanceamento da variável `quality` (target).
    * Estudo da correlação entre as features e o target, e seleção das variáveis mais relevantes para o modelo.
2.  **Modelagem:**
    * Separação da base em conjuntos de treino e teste.
    * Treinamento inicial do classificador **Random Forest**.
3.  **Otimização do Modelo:**
    * Aplicação de **Randomized Search Cross-Validation (RandomizedSearchCV)** para otimização dos hiperparâmetros do modelo.
4.  **Avaliação:**
    * Cálculo de métricas de desempenho: Acurácia (`accuracy_score`), Relatório de Classificação (`classification_report`) e Matriz de Confusão (`confusion_matrix`).

## 💻 Tecnologias Utilizadas

O projeto foi desenvolvido em um ambiente Python com o uso das seguintes bibliotecas:

* **`pandas`**: Manipulação e análise de dados.
* **`matplotlib.pyplot`** e **`seaborn`**/**`plotly.express`**: Visualização e análise exploratória de dados.
* **`scikit-learn` (sklearn)**: Implementação do modelo Random Forest, divisão de dados e métricas de avaliação.
    * `RandomForestClassifier`
    * `train_test_split`
    * `accuracy_score`, `classification_report`, `confusion_matrix`
    * `RandomizedSearchCV`
