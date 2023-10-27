# LogisticRegression_Metricas.Churn

## Descrição Projeto


**Conjunto de dados:** Base de dados bancários referente a clientes churn.


**Arquivo:** .excel


**Objetivo:** Aplicar machine learning com o modelo Logistic Regression e, analisar métricas apresentadas após treino e teste com uma base de dados de clientes churn.
Regressão Logistica: A regressão logística é uma técnica de análise estatística baseada em classificação, usada para prever variáveis binárias, como 1 ou 0. É baseada em um modelo matemático que usa a função logística para modelar a relação entre as variáveis independentes e a variável dependente (target). O modelo resultante é então usado para prever a probabilidade de um evento ocorrer. 
Ela é comumente usada para prever a probabilidade de um evento ocorrer, como inadimplência, com base em um conjunto de variáveis independentes. No caso em análise é para prever a probabilidade de clientes serem considerados churn, com base de dados históricos.


**IDE:** Colab


**Linguagem:** Python


**Principais bibliotecas utilizadas:**

• Pandas, para manipulação e tratamento dos dados; 

• Numpy, para realizar cálculos numéricos; 

• Sklearn, para aprendizado de machine learning;

• Matplotlib, para criação e visualização de gráficos.


**Modelo Utilizado:**

• Logistic Regression, algoritmo de aprendizado de máquina com base em classificação. 

**Métricas Aplicadas:**

• Matriz de Confusão:  tabela que permite a visualização do desempenho de um algoritmo de classificação , é usada para descrever o desempenho de um modelo de classificação em um conjunto de dados de teste para os quais os valores verdadeiros são conhecidos .

• Acurácia: mede a proporção de previsões corretas em relação ao número total de previsões.

• Acurácia balanceada: definida como a média harmônica das taxas de verdadeiros positivos e verdadeiros negativos.

• F1:  definida como a média harmônica da precisão e recall, varia entre 0 e 1, sendo 1 o melhor resultado possível.


**Sequência de processos:**

1° Instalação bibliotecas;

2° Pré-processamento de conjuntos de dados;

3° Distribuir variáveis explicativas (X) e variável target (Y);
Obs: Nesse caso foi necessário aplicar *LabelEncoder* na variável target (y = churn), para transformá-la em tipo binária. E nas variáveis explicativas (x) foi necessário aplicar *get_dummies* para transformá-las também em tipo binárias.

4° Separar base de dados para treino e teste;

5° Aplicar o método .fit do modelo de machine learning na base de treino;

6° Aplicar o método .predict do modelo de machine learning na base de teste, para previsão;

7° Aplicado matriz  de confusão na base de dados utilizada para teste da variável target e no que o modelo previu;

8° Aplicado métricas de acurácia, acurácia balanceada e F1, na base de dados utilizada como treino e teste, e no que foi predito pelo modelo.


**Resultado:** Os resultados das métricas do modelo aplicado a base de dados em estudo não foram boas, podendo ser melhoradas. A acurácia teve um valor considerado ruim, em torno de 79%, porém, a acurácia balanceada, que é uma métrica mais robusta teve seus valores entre 71 e 72%. E o F1 score, ficou entre 57 e 60%. A sequência de percentuais é de modo treino e teste. A diferença da acurácia de treino e teste não é grande (79,6% e 79,8%), o que indica que não há overfitting (um cenário de overfitting ocorre quando, nos dados de treino, o modelo tem um desempenho excelente, porém quando utilizamos os dados de teste o resultado é ruim).
