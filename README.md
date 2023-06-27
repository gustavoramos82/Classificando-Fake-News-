# Classificando Fake News

Neste projeto será aplicado um modelo de deep learning para classificar se um texto é fake news ou não. Inicialmente será feito uma análise exploratória, em seguida será feito a modelagem com **redes neurais artificiais (RNA)**.

O dataset foi retirado do kaggle que pode ser acessado [aqui](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset?select=Fake.csv)
A partir disso, o tratamento dos dados seguiu a estutura medallion, no qual pode ser acessado [aqui](https://drive.google.com/drive/folders/1FBQC7RHhEKVrVm61tA2Rea7omQcQKP7C?usp=sharing), no qual é dividido nas seguintes pastas:
- **Bronze**: Dataset original que foi extraido
- **Prata**: Tratamento inicial do dataset
- **Ouro**: Versão final que será utilizado para a modelagem ou para o dashboard

Se quiser mais informações sobre, clique [aqui](https://learn.microsoft.com/pt-br/azure/databricks/lakehouse/medallion)

Este trabalho do repositório é resultado de um trabalho, se quiser ler um resumo do tema leia o arquivo do notion [aqui](https://flint-texture-e2f.notion.site/Apresenta-o-de-Redes-Neurais-09020a6725774682b206dd4d089b7232?pvs=4)

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

## Extras

Se quiser saber mais sobre o que foi tratado ao longo do que foi feito, esses seguintes tópicos pode ser interessante para se pesquisar

- **Método do Cotovelo**: acesse a página [aqui](https://medium.com/pizzadedados/kmeans-e-metodo-do-cotovelo-94ded9fdf3a9)
- **Índice Callinski-Harasbazs**: acesse a página [aqui](https://acervolima.com/indice-calinski-harabasz-indices-de-validade-de-cluster-conjunto-3/)
- **K-means**: acesse a página [aqui](https://medium.com/programadores-ajudando-programadores/k-means-o-que-%C3%A9-como-funciona-aplica%C3%A7%C3%B5es-e-exemplo-em-python-6021df6e2572)
- **Redução de Dimensionaliddade**: acesse a página [aqui](https://ealexbarros.medium.com/o-que-%C3%A9-a-redu%C3%A7%C3%A3o-de-dimensionalidade-em-machine-learning-cc2a89e3cdec)



