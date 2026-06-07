# 🫀 Avaliação de Algoritmos de Machine Learning no Statlog Heart Dataset

## 📖 Sobre o Projeto

Este projeto tem como objetivo avaliar diferentes algoritmos de Machine Learning aplicados ao problema de diagnóstico de doenças cardíacas utilizando o **Statlog (Heart) Dataset**.

Ao longo do estudo foram realizados experimentos envolvendo:

* Árvores de Decisão;
* Análise de precisão e cobertura dos nós terminais;
* Avaliação por matriz de confusão;
* Curvas ROC e Precision-Recall;
* Ajuste de hiperparâmetros;
* Comparação entre múltiplos algoritmos;
* Avaliação utilizando validação cruzada.

---

## 📊 Dataset

O projeto utiliza o **Statlog (Heart) Dataset**, amplamente empregado em pesquisas de aprendizado de máquina para classificação de doenças cardíacas.

### Características

* 270 registros
* 13 atributos preditores
* 1 atributo alvo (`class`)
* Problema de classificação binária

### Variável Alvo

| Classe | Significado                 |
| ------ | --------------------------- |
| 0      | Ausência de doença cardíaca |
| 1      | Presença de doença cardíaca |

### Atributos

| Atributo                | Descrição                        |
| ----------------------- | -------------------------------- |
| age                     | Idade                            |
| sex                     | Sexo                             |
| chest pain type         | Tipo de dor no peito             |
| resting blood pressure  | Pressão arterial em repouso      |
| serum cholesterol       | Colesterol sérico                |
| fasting blood sugar     | Glicemia em jejum                |
| resting ECG             | Eletrocardiograma em repouso     |
| max heart rate          | Frequência cardíaca máxima       |
| exercise induced angina | Angina induzida por exercício    |
| oldpeak                 | Depressão do segmento ST         |
| slope                   | Inclinação do segmento ST        |
| number of vessels       | Número de vasos principais       |
| thal                    | Resultado do exame de talassemia |

---

## 🎯 Objetivos

* Construir modelos de classificação para diagnóstico cardíaco;
* Comparar diferentes algoritmos de Machine Learning;
* Avaliar desempenho através de métricas estatísticas;
* Analisar o impacto dos hiperparâmetros;
* Interpretar os resultados obtidos.

---

## 🛠 Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn

---

## 🌳 Experimento 1 – Árvore de Decisão

Foi construída uma Árvore de Decisão com profundidade máxima igual a 2.

### Análises realizadas

* Visualização da árvore
* Precisão dos nós terminais
* Cobertura dos nós terminais

### Resultado

Os nós terminais com maior precisão apresentaram aproximadamente 90% de classificações corretas, indicando regiões da árvore com padrões bem definidos para identificação de doenças cardíacas.

---

## 📈 Experimento 2 – Avaliação da Árvore de Decisão

O conjunto de dados foi dividido em:

* 70% Treinamento
* 30% Teste

### Métricas utilizadas

* Matriz de Confusão
* Acurácia

### Resultados

* 43 Verdadeiros Negativos
* 33 Verdadeiros Positivos
* 2 Falsos Positivos
* 3 Falsos Negativos

A acurácia obtida foi próxima de **94%**.

---

## 🔍 Experimento 3 – Curva ROC

Foi analisada a capacidade discriminativa do modelo através da curva ROC.

### Resultado

* AUC ≈ 0.938

O resultado indica excelente capacidade de separação entre pacientes com e sem doença cardíaca.

---

## 🤖 Experimento 4 – Comparação de Modelos

Os seguintes algoritmos foram avaliados:

| Modelo                    |
| ------------------------- |
| Decision Tree (DT)        |
| Random Forest (RF)        |
| k-Nearest Neighbors (kNN) |
| Logistic Regression (LR)  |

### Métricas Avaliadas

* Accuracy
* Precision
* Recall
* F1-Score
* AUC

### Conclusão

Os melhores resultados foram obtidos por:

1. Random Forest
2. Logistic Regression

Ambos apresentaram excelente equilíbrio entre precisão, recall e AUC.

---

## 📉 Experimento 5 – Curvas Precision-Recall e ROC

Foram geradas:

* Curva Precision-Recall
* Curva ROC

Também foram avaliadas árvores com diferentes profundidades:

```text
Depth = 1
Depth = 2
Depth = 3
Depth = 4
Depth = 5
```

A profundidade 3 apresentou o melhor desempenho em termos de AUC.

---

## ⚖️ Avaliação de Thresholds

Foram testados diferentes limiares de decisão:

```text
0.1
0.3
0.5
0.7
0.9
```

Observou-se o comportamento clássico:

* Threshold baixo → maior Recall
* Threshold alto → maior Precision

---

## 🔄 Experimento 6 – Validação Cruzada

Foi utilizada validação cruzada com 5 folds para avaliar a robustez dos modelos.

### Ranking Final

| Modelo              | Desempenho       |
| ------------------- | ---------------- |
| Logistic Regression | Melhor           |
| Random Forest       | Muito próximo    |
| Decision Tree       | Intermediário    |
| kNN                 | Menor desempenho |

---

## 🚀 Como Executar

### Instalar Dependências

```bash
pip install pandas numpy matplotlib scikit-learn
```

### Executar

```bash
python exercicioavaliacaoalgoritmos_tbs5.py
```

---

## 📚 Conceitos Aplicados

* Machine Learning
* Classificação Supervisionada
* Árvores de Decisão
* Random Forest
* kNN
* Regressão Logística
* Curva ROC
* Precision-Recall
* AUC
* Validação Cruzada
* Ajuste de Hiperparâmetros

---

## 👨‍💻 Autoria

Projeto desenvolvido para fins acadêmicos na disciplina de Avaliação de Algoritmos de Aprendizado de Máquina.

**Autores:**

* Tamyres Bezerra da Silva

---

## 📖 Referências

Statlog (Heart) Dataset

https://archive.ics.uci.edu/ml/datasets/statlog+(heart)

Scikit-Learn Documentation

https://scikit-learn.org/
