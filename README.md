# Classificando Fake News

Neste projeto será aplicado um modelo de deep learning para classificar se um texto é fake news ou não. Inicialmente será feito uma análise exploratória, em seguida será feito a modelagem com **redes neurais artificiais (RNA)**.

O dataset foi retirado do kaggle que pode ser acessado [aqui](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset?select=Fake.csv)
A partir disso, o tratamento dos dados seguiu a estutura medallion, no qual pode ser acessado [aqui](https://drive.google.com/drive/folders/1FBQC7RHhEKVrVm61tA2Rea7omQcQKP7C?usp=sharing), no qual é dividido nas seguintes pastas:
- **Bronze**: Dataset original que foi extraido
- **Prata**: Tratamento inicial do dataset
- **Ouro**: Versão final que será utilizado para a modelagem ou para o dashboard

Se quiser mais informações sobre, clique [aqui](https://learn.microsoft.com/pt-br/azure/databricks/lakehouse/medallion)

Este trabalho do repositório é resultado de um trabalho, se quiser ler um resumo do tema leia o arquivo do notion [aqui](https://flint-texture-e2f.notion.site/Apresenta-o-de-Redes-Neurais-09020a6725774682b206dd4d089b7232?pvs=4)

O projeto seguiu o seguinte fluxograma que é como vai estar organizado nos tópicos, que será mostrado na imagem abaixo

![Fluxograma do Projeto2](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/106df216-3afd-432d-a873-1ad5ac036ff2)


## Tópicos

Temos dois arquivos, um com as noticias verdadeiras e outras com as falsas, nas quais tem-se os seguintes atributos:

- **title**: Título da noticia
- **texto**: texto da noticias
- **subject**: Tópico do que se trata a noticia
- **date**: data de publicação

Para ser mais fácil a leitura, os vão ser lançado em tópicos e vai se atualizando de acordo com o vai sendo feito

### Análise Exploratória

Clique no tópico para acessar

- [Análise Inicial](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/An%C3%A1lise%20Inicial.md)
- Análise por Ano
  - [Análise título](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/An%C3%A1lise%20por%20ano.md)
  - [Análise conteúdo](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/An%C3%A1lise%20de%20por%20ano%20(subject).md)
- Análise de Cluster
  - Titulo da Noticia
      - [noticicas verdadeiras](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/An%C3%A1lise%20de%20cluster%20noticias%20verdadeiras%20(titulo).md)
      - [noticias falsas](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/Analise%20de%20cluster%20noticias%20falsas%20(titulo).md)
  - Conteúdo da Noticia
    - [noticias verdadeiras](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/An%C3%A1lise%20de%20clusters%20das%20noticias%20verdadeiras%20(subject).md)
    - [noticias falsas](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/An%C3%A1lise%20de%20cluster%20das%20noticias%20falsas%20(subject).md)

### Pré-processamneto

Além de um pré-processamento feito anteriormente para a pasta prata que foi a remoção de stopwords e lematização, agora vai ser feita os seguintes tratamentos:

- selecionar as noticias dos anos de 2016 e 2017

pois eesse anos tem termos da época e é a maior parte das noticias

- inserindo a label nos dataframes
- juntar os dataframes

Pois veio em dois dataframes diferentes e tem que juntar para fazer a modelagem

- selecionar o campo titulo e label

Pois são apenas esses campos que vão ser utilizados na modelagem

### Modelagem

A modelagem vai ser feito primeiro utilizando os modelo de machine learning e usando os modelos como *baseline*, em seguida será feita a modelagem de redes neurais, sendo aplicado uma rede neural do zero e outro a partir de uma rede neural já existente e retreina-lo

### Modelo baseline

Clique [aqui](https://github.com/gustavoramos82/Classificando-Fake-News-/blob/main/Textos/Modelagem%20com%20algoritmos%20de%20machine%20learning.md) para saber mais

### Rede neural MLP (Multi Layer Percepton)
Foi construidio uma rede neural em que foi feito no seguinte esquema:
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/793acd25-62b2-4ffa-9470-69b922977bdb)


No qual se obteve as seguintes métricas

  - **Acuracia**: 0.9460992813110352
  - **Precisão**: 0.945361852645874
  - **Recall**: 0.9439864158630371
  - **F1-score**: 0.944673633598654

###  Rede Neural Recorrente (RNN)
Foi construidio uma rede neural RNN em que foi feito no seguinte esquema:
![image](https://github.com/gustavoramos82/Classificando-Fake-News-/assets/39843884/c46a7877-83a5-4b84-89c2-c2ca5bb3066b)

No qual se teve as seguintes méricas

  - **Acuracia**: 0.9522458910942078
  - **Precisão**: 0.9503632187843323
  - **Recall**:  0.951745867729187
  - **F1-score**: 0.9510540407308745


## Avaliação

Podemos ver que, comparando as métricas, que as redes neurais teve um desempenho melhor, mas se comparado como o Extra tree 
classifier, então dependo da situação, poderia mais preferência de um e do outro, por exemplo, se for levar em consideração
os custos, o Extra tree seria considerado, pois não usa gpu para treinamento, entretanto, se quiser levar a perfomace em consideração, poderia usar a rede neural RNN, que foi o melhor nas métricas, logo poderia haver certas mudanças para ver se o desempenho ser melhor,como:

- Usar o método embbeding para vetorizar o texto
- Testar outros tipos de arquiteturas (CNN, ou testar outros tipos de RNN, que se mostrou melhor)
- Usar redes pré-treinadas como BERT e RoBerta (não consegui fazer isso neste projeto, pois é um projeto muito demorado)

## Extras

Se quiser saber mais, esses seguintes tópicos pode ser interessante para se pesquisar

- **Método do Cotovelo**: acesse a página [aqui](https://medium.com/pizzadedados/kmeans-e-metodo-do-cotovelo-94ded9fdf3a9)
- **Índice Callinski-Harasbazs**: acesse a página [aqui](https://acervolima.com/indice-calinski-harabasz-indices-de-validade-de-cluster-conjunto-3/)
- **K-means**: acesse a página [aqui](https://medium.com/programadores-ajudando-programadores/k-means-o-que-%C3%A9-como-funciona-aplica%C3%A7%C3%B5es-e-exemplo-em-python-6021df6e2572)
- **Redução de Dimensionaliddade**: acesse a página [aqui](https://ealexbarros.medium.com/o-que-%C3%A9-a-redu%C3%A7%C3%A3o-de-dimensionalidade-em-machine-learning-cc2a89e3cdec)
- **Métricas de classificação**: acesse a página [aqui](https://medium.com/kunumi/m%C3%A9tricas-de-avalia%C3%A7%C3%A3o-em-machine-learning-classifica%C3%A7%C3%A3o-49340dcdb198)
- **Base onde fiz de base para cirar o modelo de rede neural**: acesse a página [aqui](https://realpython.com/python-keras-text-classification/#convolutional-neural-networks-cnn)
- Rede neural RNN: acesse a página [aqui](https://medium.com/@web2ajax/redes-neurais-recorrentes-lstm-b90b720dc3f6)



