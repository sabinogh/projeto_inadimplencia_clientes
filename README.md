# Customer Default Classification with Machine Learning

Machine Learning project for customer default classification in an industrial equipment sales company.

---

## Problem Context

In companies that work with credit and installment payments, **knowing in advance which customers are most likely to default is essential** for the financial health of the business. Decisions such as credit limits, payment terms, and collection actions become far more efficient when backed by data.

In this project, I analyze billing data from an industrial equipment company. The goal is to identify whether a customer will continue delaying payments **even after payment term agreements of up to 60 days**.

---

## What the data reveals before any model

Right in the exploratory analysis, the data already tells an important story:

> **617 customers are classified as defaulters against 390 who are not.**

This means **61.3% of the customer base is in default** — more than half. This number alone justifies building a predictive model. Ignoring this pattern would mean leaving money on the table and exposing the company to unnecessary risk.

This stage is called **descriptive analysis**: before any prediction, we understand the data distribution, customer behavior by type, payment delay justifications, and sales value ranges.

---

## Why test three different algorithms?

A key part of any Machine Learning project is **comparing models** before choosing the best one. Three approaches with distinct purposes were tested:

### Dummy Classifier — The baseline
Accuracy: **0.6111**

The Dummy model learns nothing — it simply always predicts the most frequent class (defaulter). It serves as a **baseline**: if a more sophisticated model does not beat the Dummy, it is not learning anything useful. Here, the Dummy hit 61% simply because most customers are defaulters.

### Decision Tree — Interpretable and efficient
Accuracy: **0.8016**

The Decision Tree learns rules such as "if the billing time is X and the customer is Y, then they are a defaulter". It is a highly valued model for its **explainability** — it is possible to visualize exactly the path that led to the classification. It achieved 80% accuracy, a significant jump over the Dummy.

### KNN (K-Nearest Neighbors) — Similarity-based
Accuracy: **1.0**

KNN classifies a new customer by comparing it with the nearest neighbors in the dataset. Before applying it, **data normalization** was required, since the algorithm uses distance calculations and would be distorted by variables on different scales. The result was 100% accuracy on the test data for this dataset.

---

## Final Results

| Model              | Accuracy |
|--------------------|----------|
| Dummy Classifier   | 61.11%   |
| Decision Tree      | 80.16%   |
| KNN                | 100.00%  |

**KNN** was the best-performing model on this dataset and would be the one chosen for production. It is worth noting that 100% accuracy on smaller datasets is possible and should be evaluated carefully on larger bases — but it demonstrates that the data has very well-defined patterns that the model was able to fully capture.

---

## Technologies used

- Python
- Pandas
- Plotly Express
- Scikit-learn (DummyClassifier, DecisionTreeClassifier, KNeighborsClassifier, OneHotEncoder, LabelEncoder, MinMaxScaler)
- Matplotlib

---

## About the project

This project is part of my Machine Learning portfolio, focused on supervised classification applied to a real business problem. The goal was to explore the complete ML workflow: from exploratory analysis to selecting the best model.

---
---

# Classificação de Inadimplência de Clientes com Machine Learning

Projeto de Machine Learning para classificação de inadimplência em uma empresa de vendas de equipamentos industriais.

---

## Contexto do Problema

Em empresas que trabalham com crédito e parcelamento, **saber antecipadamente quais clientes têm maior risco de inadimplência é essencial** para a saúde financeira do negócio. Decisões como limites de crédito, prazos de pagamento e ações de cobrança se tornam muito mais eficientes quando apoiadas em dados.

Neste projeto, analiso dados de faturamento de uma empresa de equipamentos industriais. O objetivo é identificar se um cliente continuará atrasando seus pagamentos **mesmo após acordos de prazo de até 60 dias**.

---

## O que os dados revelam antes mesmo do modelo

Logo na análise exploratória, os dados já contam uma história importante:

> **617 clientes estão classificados como inadimplentes contra 390 que não são.**

Isso significa que **61,3% da base de clientes está em situação de inadimplência** — mais da metade. Esse número, por si só, já justifica a criação de um modelo preditivo. Ignorar esse padrão seria deixar dinheiro na mesa e expor a empresa a riscos desnecessários.

Essa etapa é chamada de **análise descritiva**: antes de qualquer previsão, entendemos a distribuição dos dados, o comportamento dos clientes por tipo, justificativas de atraso e faixas de valor de venda.

---

## Por que testar três algoritmos diferentes?

Parte essencial de qualquer projeto de Machine Learning é **comparar modelos** antes de escolher o melhor. Neste projeto foram testados três abordagens com propósitos distintos:

### Dummy Classifier — O ponto de partida
Acurácia: **0.6111**

O modelo Dummy não aprende nada — ele simplesmente chuta sempre a classe mais frequente (inadimplente). Ele serve como **linha de base**: se um modelo mais sofisticado não superar o Dummy, ele não está aprendendo nada útil. Aqui o Dummy acertou 61% simplesmente porque a maioria dos clientes é inadimplente.

### Árvore de Decisão — Interpretável e eficiente
Acurácia: **0.8016**

A Árvore de Decisão aprende regras como "se o tempo de faturamento for X e o cliente for Y, então ele é inadimplente". É um modelo muito valorizado pela sua **explicabilidade** — é possível visualizar exatamente o caminho que levou à classificação. Atingiu 80% de acurácia, um salto significativo em relação ao Dummy.

### KNN (K-Nearest Neighbors) — Baseado em similaridade
Acurácia: **1.0**

O KNN classifica um novo cliente comparando-o com os vizinhos mais próximos na base de dados. Antes de aplicá-lo, foi necessário **normalizar os dados**, pois o algoritmo usa cálculo de distância e seria distorcido por variáveis em escalas diferentes. O resultado foi uma acurácia de 100% nos dados de teste deste conjunto.

---

## Resultado Final

| Modelo             | Acurácia |
|--------------------|----------|
| Dummy Classifier   | 61,11%   |
| Árvore de Decisão  | 80,16%   |
| KNN                | 100,00%  |

O **KNN** foi o modelo de melhor desempenho neste conjunto de dados e seria o escolhido para produção. Vale ressaltar que uma acurácia de 100% em conjuntos menores é possível e deve ser avaliada com cautela em bases maiores — mas demonstra que os dados têm padrões muito bem definidos e o modelo conseguiu capturá-los completamente.

---

## Tecnologias utilizadas

- Python
- Pandas
- Plotly Express
- Scikit-learn (DummyClassifier, DecisionTreeClassifier, KNeighborsClassifier, OneHotEncoder, LabelEncoder, MinMaxScaler)
- Matplotlib

---

## Sobre o projeto

Este projeto faz parte do meu portfólio de Machine Learning, com foco em classificação supervisionada aplicada a um problema real de negócio. O objetivo foi explorar o fluxo completo de um projeto de ML: da análise exploratória à seleção do melhor modelo.
