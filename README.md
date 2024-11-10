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

Após o treinamento e avaliação do modelo, obtivemos os seguintes resultados de métricas:

* Acurácia: 0.80
* Precisão: 0.55
* Recall: 0.46
* F1 Score: 0.50
  
# Análise dos Pontos Fortes e Fracos do Modelo:

Pontos Fortes:

* Acurácia de 80% sugere que o modelo é razoavelmente eficaz em classificar jogos acima ou abaixo da média de vendas.
* Random Forest lida bem com os dados categóricos e variáveis correlacionadas, gerando um modelo inicial estável e relativamente robusto.
  
Pontos Fracos:

* Baixo Recall e Precisão indicam que o modelo ainda possui dificuldades em identificar jogos com vendas globais acima da média (classe positiva). Isso pode sugerir uma insuficiência de variáveis que realmente impactam nas vendas ou a necessidade de maior ajuste dos hiperparâmetros.
* F1 Score de 0.50 mostra que o equilíbrio entre precisão e recall ainda precisa ser aprimorado para aumentar a eficácia da classificação de jogos de alto desempenho.
