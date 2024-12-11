English description below

Classificador de Spam vs Ham(Não Spam)

Eu criei este projeto com o objetivo de construir um modelo de aprendizado de máquina capaz de classificar mensagens de texto como "spam" ou "ham" (não spam). 

O conjunto de dados utilizado contém mensagens rotuladas, 
e o objetivo foi treinar um Classificador Random Forest para obter uma alta precisão na classificação de novas mensagens não vistas.

Visão Geral do Projeto

Carregamento e Exploração dos Dados:

O conjunto de dados foi carregado a partir de um arquivo CSV, que contém colunas para os rótulos das mensagens (spam ou ham) e o texto correspondente.

A minha inspeção inicial dos dados forneceu informações sobre o tamanho e a estrutura do conjunto de dados.

Pré-processamento de Texto:

Remoção de HTML: Implementei uma função para identificar e remover qualquer conteúdo HTML das mensagens.

Extração de URLs: Usei a biblioteca urlextract para identificar e extrair quaisquer URLs presentes nas mensagens.

Limpeza do Texto: O texto foi limpo convertendo-o para minúsculas, removendo caracteres não alfabéticos e filtrando palavras utilizando o nltk.

Visualização dos Dados:

A distribuição das classes (spam e ham) nas mensagens foi visualizada por meio de um gráfico de barras.

As 20 palavras mais frequentes no conjunto de dados limpo foram "plotadas" para dar uma visão geral dos termos mais comuns.

Vetorização de Texto:

Utilize o TfidfVectorizer para converter os dados de texto em características numéricas, o que obviamente os torna adequados para modelos de aprendizado de máquina. 
O conjunto de treinamento e teste foram divididos, e o vetorizador foi aplicado adequadamente.


Construção do Modelo e Ajuste de Hiperparâmetros:

Treinei um RandomForestClassifier para classificar as mensagens de texto.

Os hiperparâmetros do classificador, como o número de estimadores e a profundidade das árvores, foram ajustados utilizando o RandomizedSearchCV para encontrar a configuração ideal.
Depois ajustei manualmente os hiperparâmetros no "param_distributions" de forma a chegar nos melhores hiperparâmetros.

Avaliação do Modelo:

O desempenho do modelo foi avaliado no conjunto de testes, e métricas como precisão, recall, F1-score e a matriz de confusão foram calculadas.

O modelo ajustado obteve uma precisão de teste de 97,99%.

Métricas Principais:

Precisão de Teste: 97,99%

Precisão (Ham/Não-Spam): 99% | Precisão (Spam): 95%

Recall (Ham/Não-Spam): 98% | Recall (Spam): 99%

F1-Score: 98%

Spam vs Ham (Non-Spam) Classifier

I created this project with the goal of building a machine learning model capable of classifying text messages as "spam" or "ham" (non-spam).

The dataset used contains labeled messages, and the objective was to train a Random Forest Classifier to achieve high accuracy in classifying new, unseen messages.

Project Overview

Data Loading and Exploration:

The dataset was loaded from a CSV file, which contains columns for the message labels (spam or ham) and the corresponding text.

My initial inspection of the data provided insights into the size and structure of the dataset.

Text Preprocessing:

HTML Removal: I implemented a function to identify and remove any HTML content from the messages.

URL Extraction: I used the urlextract library to identify and extract any URLs present in the messages.

Text Cleaning: The text was cleaned by converting it to lowercase, removing non-alphabetic characters, and filtering words using nltk.

Data Visualization:

The distribution of classes (spam and ham) in the messages was visualized through a bar chart.

The 20 most frequent words in the cleaned dataset were "plotted" to provide an overview of the most common terms.

Text Vectorization:

I used TfidfVectorizer to convert the text data into numerical features, making them suitable for machine learning models. The training and test sets were split, and the vectorizer was applied accordingly.

Model Construction and Hyperparameter Tuning:

I trained a RandomForestClassifier to classify the text messages.

The classifier's hyperparameters, such as the number of estimators and the depth of the trees, were tuned using RandomizedSearchCV to find the optimal configuration. I then manually adjusted the hyperparameters in the param_distributions to arrive at the best parameters.

Model Evaluation:

The performance of the model was evaluated on the test set, and metrics such as accuracy, recall, F1-score, and the confusion matrix were calculated.

The tuned model achieved a test accuracy of 97.99%.

Key Metrics:

Test Accuracy: 97.99%

Precision (Ham/Non-Spam): 99% | Precision (Spam): 95%

Recall (Ham/Non-Spam): 98% | Recall (Spam): 99%

F1-Score: 98%
