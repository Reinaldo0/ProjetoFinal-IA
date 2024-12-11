# ProjetoFinal-IA

* Instalar o arquivo vgsales.csv ou instalar pelo link: https://www.kaggle.com/datasets/gregorut/videogamesales
* Abrir o arquivo ProjetoA3.ipynb no colab 
* Adicionar o arquivo vgsales.csv em Arquivos no colab e executar

# Definição do Problema:

O objetivo deste projeto é prever o sucesso de vendas globais de jogos com base em informações de lançamento, plataforma, gênero e publicadora. Utilizando um conjunto de dados contendo informações sobre jogos e suas vendas globais, buscamos identificar os jogos mais vendidos de cada plataforma e gênero.

# Análise dos Dados:

O dataset inicial inclui as seguintes colunas principais:

* Nome do jogo
* Plataforma: especifica o console ou dispositivo
* Ano de Lançamento
* Gênero
* Publicadora
* Vendas Globais (em milhões de unidades)
  
Após a importação e limpeza dos dados, foram detectadas linhas com valores nulos e inconsistências, que foram removidas para evitar problemas no modelo de previsão. Posteriormente, os dados foram analisados visualmente para melhor compreensão:

* Distribuição de Jogos por Plataforma: identificamos quais plataformas possuem maior número de jogos lançados.
* Distribuição de Vendas Globais: análise da frequência de vendas entre diferentes jogos.

# Modelo Base Escolhido:

* Foi optado por utilizar um modelo de classificação com Random Forest Classifier. A Random Forest é escolhida por sua robustez em lidar com dados categóricos e sua habilidade de gerar classificações com base em múltiplas árvores de decisão.

# Resultados Iniciais e Análise do Modelo:

Após o treinamento e avaliação inicial do modelo, obtive os seguintes resultados de métricas:

* Acurácia: 0.80
* Precisão: 0.55
* Recall: 0.46
* F1 Score: 0.50

# Resultados do modelo Random Forest aprimorado:

Após realizar as melhorias, obtive as seguintes Métricas:

* Acurácia: 0.98
* Precisão: 0.97
* Recall: 0.94
* F1 Score: 0.96
  
# Análise dos Pontos Fortes e Fracos do Modelo:

Pontos Fortes:

* Melhoria Significativa nas Métricas:
O modelo Random Forest obteve uma alta acurácia (0.98), precisão (0.97), recall (0.94) e F1 Score (0.96), indicando um desempenho sólido em geral.
A alta precisão sugere que o modelo tem uma baixa taxa de falsos positivos, identificando corretamente os casos positivos.

* Capacidade de Generalização:
O uso de técnicas como validação cruzada (GridSearchCV) e divisão do conjunto de dados para treinamento e teste reduz o risco de overfitting.

* Feature Engineering Efetiva:
A inclusão da feature Regional_Sales_Ratio captura relações importantes entre vendas globais e regionais, melhorando o desempenho.

* Ajuste de Hiperparâmetros:
A otimização com GridSearchCV ajudou a encontrar os melhores hiperparâmetros para maximizar o desempenho.

* Robustez do Algoritmo:
O Random Forest é robusto a outliers e não requer grande pré-processamento, sendo apropriado para dados heterogêneos como os analisados.
  
Pontos Fracos:

* Complexidade Computacional:
O treinamento do modelo Random Forest pode ser computacionalmente caro, especialmente com muitos hiperparâmetros ajustados em GridSearchCV.

* Interpretação do Modelo:
Modelos baseados em árvores, como o Random Forest, podem ser difíceis de interpretar, apesar de permitirem a análise de importância das features.

* Possível Dependência do Conjunto de Dados:
A alta performance pode estar relacionada a algum viés ou limitação específica dos dados (e.g., baixa diversidade ou desequilíbrio de classes).

* Impacto das Features Categóricas:
Embora a codificação one-hot tenha sido usada, o número elevado de categorias pode ter aumentado a dimensionalidade do conjunto de dados, possivelmente dificultando a interpretação.
